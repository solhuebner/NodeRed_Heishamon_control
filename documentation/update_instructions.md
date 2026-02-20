## Updating the flow

To update the flow to a newer version, you need to perform the next steps:<br>
1. Create a backup<br>
2. Download the latest flow.json<br>
3. Remove current version<br>
4. Import new version<br>
5. Adjust settings<br>
6. Deploy<br>

The steps will be described in more details below

**************

### 1 - Create a backup
This step is actually only required if you have made modifications to the current flow. <br>
- In the flow editor **Select** all the **tabs** with [WP ...] in the name. 
- Click the **hamburger icon** in the upper right corner
- Press **Export**<br>
Make sure "Selected nodes" is active
- Click **[Download]**
- Save the file to your local drive with a useful prefix / postfix, like "backup" and the date. 

> [!TIP]
> - To multi-select specific tabs, use [CTRL] + click
> - To multi-select a row of tabs, use [SHIFT] + click

> [!IMPORTANT]
> The exported file (backup) does not contain any of your settings. It is only the flow.

*********

### 2 - Download the latest flow.json
Go to the github page and save the flow.json file to your local drive.

*************

### 3 - Remove current version

#### 3.1 - Remove all tabs
In the Node-Red flow editor, you need to:
- **Select** all flow-tabs which start with [WP ] on the top of the screen
- Press **[DEL]**
- Wait until it is finished

> [!WARNING]
> Do **NOT** remove your personal **[WP Personal]** tab.

> [!TIP]
> - To multi-select specific tabs, use [CTRL] + click
> - To multi-select a row of tabs, use [SHIFT] + click

> [!CAUTION]
> If you select too many tabs and press [DEL], the **browser** might **timeout**.
> This Process just takes a long time depending on your resources.
> Wait or select "Wait for browser" a number of times for it to finish. If that does not work, reduce the amount of selected tabs for deletion.


#### 3.2 - Remove dashboard items

In the flow editor:
- Click the **hamburger icon** in the upper right corner
- Select **Configuration Nodes**
- The config sidebar appears on the right
- Click on **[unused]** in the top of the window

**[ui_group]**
On the top you should see "ui_group"
- Select the first node in the list
- Press **[CTRL] + A** to select all of them at once
- Press **[DEL]**

**[ui_tab]**
On the top you should now see "ui_tab"
- Select the first node in the list
- Press **[CTRL] + A** to select all of them at once
- Press **[DEL]**

Then:
- Do **NOT** press Deploy yet
- [Continue with the flow installation instruction](flow_installation.md)  

********

[Back](../readme.md)

