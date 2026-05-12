

- FortiSIEM uses XML-based parser framework to parse events, means to teach the system to understand the incoming data.

- Examples of what a parser does:
  - Recognizes the type of device or application that sends the data and determines which parser to use.
  - Extracts and stores data from specific fields in the log source (Source IP, Source Port, Malware Name, File Name, and so on) as attributes.
  - Maps each incoming log to an event type.
 
- If no parser exists for an incoming log, FortSIEM stores the information but doesn't understand how to interpret the data; therefore, FortiSIEM creates what is called as an Unknown Event.
- You can still query these events using the raw event message attribute


*Terminology Reminder*

<img width="400" alt="{8486DC16-9A66-4B5A-8B82-4AC90442D984}" src="https://github.com/user-attachments/assets/e62fd591-753e-4859-a190-04a62a734f81" />
