## Project Tracker

### Description:
The "Project Tracker" spreadsheet is designed to provide a detailed log of project activities, assignments, timelines, and progress updates. The key columns included in the sheet are:

- **Activity:** Describes the specific task or activity within the project.
- **Assigned to:** Identifies the team member responsible for the activity.
- **Start:** The start date of the activity.
- **End:** The expected or actual end date of the activity.
- **Days:** The duration of the activity in days.
- **Status:** Current status of the activity (e.g., "In Progress").
- **% Done:** Percentage completion of the activity.

### Formulas Used in Conditional Formatting:

#### 1. Activity Duration Highlight:
This formula highlights cells that fall within the duration of a task.
```excel
=AND(K$4>=$E6-(WEEKDAY($E6,2)+1),K$4<=$F6)
```

#### 2. Ongoing Activity Progress Highlight:
This formula highlights cells representing the progress of an ongoing task based on the percentage completion.
```excel
=AND($I6>0,K$4<=($E6+($F6-$E6)*$I6)-WEEKDAY(($E6+($F6-$E6)*$I6),2)+1,K$4>=$E6-WEEKDAY($E6,2)+1)
```

#### 3. Completed Activity Highlight:
This formula highlights the end date of completed tasks.
```excel
=AND($H6="Completed",K$4=$F6-WEEKDAY($F6,2)+1)
```

#### 4. Blocked Activity Highlight:
This formula highlights the duration of tasks that are currently blocked.
```excel
=AND($H6="Blocked",$I6>0,K$4<=($E6+($F6-$E6)*$I6)-WEEKDAY(($E6+($F6-$E6)*$I6),2)+1,K$4>=$E6-WEEKDAY($E6,2)+1)
```

#### 5. Current Week Highlight:
This formula highlights the cell representing the current week.
```excel
=K$4=(TODAY()-WEEKDAY(TODAY(),2)+1)
```

### How the Project Is Helpful:

#### 1. Clear Visualization:
Conditional formatting provides a visual representation of task timelines, progress, and statuses, making it easier to track and manage projects.

#### 2. Accountability:
By assigning tasks to specific team members and tracking their progress, the tool ensures accountability and helps in identifying any bottlenecks or delays.

#### 3. Real-Time Updates:
The tracker allows for real-time updates on the status and completion percentage of tasks, providing an up-to-date overview of the project.

#### 4. Enhanced Coordination:
The tool facilitates better communication and coordination among team members, ensuring that everyone is aligned with the project goals and timelines.

### Conclusion:
The Project Tracker is a comprehensive tool designed to streamline project management by providing a clear and structured way to track activities, assignments, timelines, and progress. Leveraging advanced Excel techniques, including conditional formatting, it enhances the visualization of task statuses and timelines, ultimately making project management more efficient and effective.
