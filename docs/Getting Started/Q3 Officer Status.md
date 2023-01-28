# Dispatching Logic - Jason TBC
:::info
For Q3 in Dispatch Module, there are 2 types of statuses, which are "Dispatchable Status" and "Non Dispatchable Status"

:::

| Dispatchable Status | Non Dispatchable Status |
|--|--|
| On Duty | Lunch |
| Posted | Break |
| Screen | Busy |
| Training | Fire Watch |
| (Other statuses) |  |

## Officer Status - Assign an event with "Dispatchable Status"
1. If officer A's status is "On Duty", and a dispatcher assigns a dispatch event to him, then the first assigned event's status in Q4 will be **"Enroute"** automatically
2. Officers with any assigned events with **"Enroute"** or **"On Scene"** status, they **CANNOT** be put to `Non Dispatchable Status`, such action will trigger a dialog with "Please clear Officer [  xxx ] from assigned events, or update assigned events to On Hold"

## Officer Status - Assign an event with "Non Dispatchable Status"
1. If officer A's status is "On Duty", and a dispatcher assigns a dispatch event to him, then the first assigned event's status in Q4 will be **"On Hold"** automatically; If the dispatcher tries to change the event status in Q4 to **"Enroute"** or **"On Scene"**, the system will not allow it and display a dialog with "Please change the officer to a dispatchable status to perform this action"
2. The second and the following dispatch events assigned to that officer will be **"On Hold"** automatically
3. 