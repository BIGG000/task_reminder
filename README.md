# task_reminder
Plain text reminder 
Reminders in your plain text notes and to-do lists

This application is at prototype stage. It doesn't yet have a GUI, so it's usability is limited. It hasn't been thoughtfully tested and should not be used on any valuable data. Bug reports and feature suggestions are welcome.

!R continuously scans plain text files and makes specifically composed text (reminder tags) to show you a pop-up reminder.

@!10:00 Star Plain text reminder somewhere in plain text file will remind you with text "Star Plain text reminder" next time it's 10 o'clock.

Reminder tags can set time:

by full date and time or by almost any part of it
in 24H format or in 12H format
as absolute or as delta to current time
Support for recurring reminders is planned.

There are many ways to compose a reminder tag. Read more about reminder tag syntax.

!R tries to be:

Minimalistic
Customizable
Expandable
Plain text
Installation
!R requires Python 3.3+, watchdog and dateutil modules.

Windows
Download and install latest Python 3 distribution;
Open cmd/terminal and run pip install watchdog python-dateutil;
Place and name plain-text-reminder folder any way you want.
Mac OS
Install Python 3 using homebrew or Python 3 distribution;
Open cmd/terminal and run pip3 install watchdog python-dateutil;
Place and name plain-text-reminder folder any way you want.
GNU/Linux distributions
Install "python3" (or equal) package by your distribution package manager;
Install "python3-watchdog" and "python3-dateutil" packages (or equal) packages by your distribution package manager. If there are no such packages for your distribution, install "python3-pip" (or equal) package and run sudo pip3 install watchdog python-dateutil in terminal;
Place and name plain-text-reminder folder any way you want.
Easier installation bundles will appear at the next stages of development.

Usage
Currently there's only a limited CLI interface available.

You can practice with reminder tags syntax by running
python3 run.py -d for Mac OS and GNU/Linux distributions or
python run.py -d for Windows.

You can test !R by running
python3 run.py -s path/to/folder_with_text_files/ for Mac OS and GNU/Linux distributions or
python run.py -s C:\path\to\folder_with_text_files\ for Windows.

At the first run !R will create reminder.cfg file for its settings.

!R will start parsing text files in provided path (relative or absolute).
List of found reminders, messages for triggered reminders and available user actions will appear in cmd/terminal.

What !R really does:

Parses plain text files in set folder for reminder tags;
Watches set folder and reparses changed files;
Replaces found reminder tags with ones that are independent of current time;
Otherwise @!10:00 will always be next 10 o'clock, rather than a single tomorrow 10'clock;
Waits for a time of set reminders;
Shows a pop-up with ability to postpone or dismiss a reminder;
Changes reminder tags in text files accordingly.
