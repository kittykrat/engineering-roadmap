# 

Script:

```
DetectiveCases
| where Timestamp between (datetime(2022-01-01)..datetime(2022-12-31 23:59:59.9))
| extend Properties
| where EventType == 'CaseOpened'
| extend bountyInt = toint(Properties.Bounty)
//| summarize arg_min(Timestamp, *) by CaseId
| join kind=leftouter
(
    DetectiveCases
    | where EventType == 'CaseAssigned'
    //| summarize arg_min(Timestamp, *) by CaseId
) on CaseId
| join kind=rightouter
(
    DetectiveCases
    | where EventType == 'CaseSolved'
    //| summarize arg_min(Timestamp, *) by CaseId
) on CaseId
| where DetectiveId2 == DetectiveId1
| summarize arg_min(Timestamp, *) by CaseId2
| summarize totalBounty = sum(bountyInt) by DetectiveId2
| sort by totalBounty desc
```
