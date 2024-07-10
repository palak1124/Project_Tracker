# Project_Tracker
Description:
The Project Tracker is a comprehensive tool designed to manage and monitor project activities, assignments, timelines, and progress. This tool facilitates effective project management by providing a clear and structured way to track each task from inception to completion.

Features:

Activity Logging: Detailed descriptions of all project activities.
Assignment Tracking: Identifies responsible team members for each activity.
Timeline Management: Start and end dates for each task, along with duration.
Progress Monitoring: Current status and percentage completion of activities.

## Project Tracker Conditional Formatting:

This Project Tracker includes advanced conditional formatting to enhance visualization of task statuses and timelines. Below are the key conditional formatting rules used in this tracker:

-> Activity Duration Highlight =AND(K$4>=$E6-(WEEKDAY($E6,2)+1),K$4<=$F6)

-> Ongoing Activity Progress Highlight: =AND($I6>0,K$4<=($E6+($F6-$E6)*$I6)-WEEKDAY(($E6+($F6-$E6)*$I6),2)+1,K$4>=$E6-WEEKDAY($E6,2)+1)

-> Complete Activity Highlight= AND($H6="Completed",K$4=$F6-WEEKDAY($F6,2)+1)

-> Blocked Activity Highlight =AND($H6="Blocked",$I6>0,K$4<=($E6+($F6-$E6)*$I6)-WEEKDAY(($E6+($F6-$E6)*$I6),2)+1,K$4>=$E6-WEEKDAY($E6,2)+1)

-> Current Week Highlight = =K$4=(TODAY()-WEEKDAY(TODAY(),2)+1)

