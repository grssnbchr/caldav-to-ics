## Caldav-to-ICS

This little script can be run as a cronjob, for example. 
It converts a CalDAV calendar (found on a specific URL) into an .ics file and uploads this to an FTP server.

The URL can then be fed to Google Calendar. I haven't found another way to regularly sync my CalDAV calendar with Google.

### Installation

`pip install caldav icalendar`

### Config

Make sure you have a `.env` file in the main directory with the following variables:

* `CALDAV_URI`: The URI of your CalDAV calendar
* `CALDAV_USR`: User name for your CalDAV calendar
* `CALDAV_PWD`: Corresponding password
* `FTP_URI`: The URI of your FTP server where the `.ics` file will be uploaded to
* `FTP_USR`: The user for the server
* `FTP_PWD`: Corresponding password
* `FTP_PATH`: The actual path to the file you want to store (should end in `calendar.ics`)
