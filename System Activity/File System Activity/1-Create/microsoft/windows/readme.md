
# Event Dossier: Windows Security 4656
### Windows Security 4656
- **Event Code: 4656
- **Event Title: A handle to an object was requested
- **Description: Logs the start of every file activity but does not guarantee that it succeeded
- **Event References:
- **Data It Provides: The name of the file
  - https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/event.aspx?eventid=4656
  - https://learn.microsoft.com/en-us/windows/security/threat-protection/auditing/event-4656 

 ### OCSF Version: 0.50.0
 - `category_uid`: `1` `(System Activity)`
 - `class_uid`: `1001` `(File System Activity)`
 - `activity_id`: `1` `(Launch)`
 - `metadata.profiles`: `[host]`

 ### Mapping:
 
| OCSF                       | Raw                                                                                                                      |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| `actor.process.file`       | `Process Information.Creator Process Name`                                                                               |
| `actor.process.pid`        | `Process Information.Creator Process ID`                                                                                 |
| `actor.user.domain`        | `Subject.Account Domain` *(MSFT event version 0-1)*<br>_OR_<br>`Creator Subject.Account Domain` *(MSFT event version 2)* |
| `actor.user.name`          | `Subject.Account Name` *(MSFT event version 0-1)*<br>_OR_<br>`Creator Subject.Account Name` *(MSFT event version 2)*     |
| `actor.user.session_uid`   | `Subject.Logon ID` *(MSFT event version 0-1)*<br>_OR_<br>`Creator Subject.Logon ID` *(MSFT event version 2)*             |
| `actor.user.uid`           | `Subject.Security ID` *(MSFT event version 0-1)*<br>_OR_<br>`Creator Subject.Security ID` *(MSFT event version 2)*       |
| `device.name`              | `ComputerName`                                                                                                           |
| `message`                  | `Message`                                                                                                                |
| `process.cmd_line`         | `Process Information.Process Command Line`                                                                               |
| `process.file`             | `Process Information.New Process Name`                                                                                   |
| `process.pid`              | `Process Information.New Process ID`                                                                                     |
| `process.user.domain`      | `Target Subject.Account Domain`                                                                                          |
| `process.user.name`        | `Target Subject.Account Name`                                                                                            |
| `process.user.session_uid` | `Target Subject.Logon ID`                                                                                                |
| `process.user.uid`         | `Target Subject.Security ID`                             

File activity audit flow
<img width="1491" alt="image" src="https://user-images.githubusercontent.com/122571503/214717883-11600fd8-843f-4908-866a-516a817c6a5e.png">


![image](https://user-images.githubusercontent.com/122571503/214717579-b1932d43-661e-43e8-9e3b-f87f1aa2d19b.png)

 </Event>


                                                                |