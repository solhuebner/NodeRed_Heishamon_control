<a id="top"></a>
<a id="flow"></a>
## Flow installation<br/>
In short, the steps you need to perform are:<br>
1 - Download flow.json file<br>
2 - Import the file<br>
3 - Adjust settings<br>
4 - Deploy<br>

> [!IMPORTANT]
> These steps assumes this is a clean installation / deployment. 
> If you are **updating**, please start with the [update instructions](update_instructions.md)

*******

### 1 Download
- On the main page you will find the latest file version **"flows.json"**. This file contains all the flows.<br>
- **Download** it and save it on your local drive.<br>

[Top](#top) / [Back](../readme.md)

------------

### 2 Import the file
Go to your Node-Red flow editor. `http://<host-IP>:1880/#flow` (or `http://<host-IP>:1880/endpoint/ui` in HomeAssistant)<br>
- Click the **hamburger icon** in the top right corner
- Select **Import**
- **Select** a **file** to import and select flow.json
- Click on **Import**
- Do **NOT** press [Deploy] yet

> [!IMPORTANT]
> When you are **UPDATING** the flow, you might be prompted there are duplicates.<br>
> - Click **[View nodes...]** 
> - Scroll down in the list to verify **MQTT (x.x.x.x)** is **unticked**
> - Click **Import selected**

[Top](#top) / [Back](../readme.md)

-----------
### 3 Adjust settings
There are some mandatory settings need to be adjusted. <br>
Additionally there are some optional things to change.<br>

-----------

#### 3.1 MQTT `(mandatory)`
The flow is not aware yet of your MQTT broker. You need to adjust the settings of the MQTT configuration node.<br>
- In the upper right corner, click the **hamburger icon** again<br>
- Click **Configuration nodes**<br>

You will see a list of configuration nodes appear below it.<br>
<br>
- Find and **edit** MQTT (x.x.x.x) (double click)<br>
- Change/correct all settings of this node.
	- Name: Rename x.x.x.x to a name of your own preferred name<br>
	- Server: (if not present, add) IP address of your MQTT broker<br>
	- Fill in the MQTT broker username and password
	- Port: 1833 (default)<br>
	- Protocol: MQTT v3.1.1 (maximum for heishamon)<br>
 	- QOS: 0 (maximum for heishamon)<br>

> [!IMPORTANT]
> If you see one MQTT config node with **x.x.x.x**, you still need to modify it<br>
> If you see multiple MQTT config nodes, there is a high chance you need to remove one

---------

#### 3.2 Theme `(optional)`
Node-Red allows you to personalize your dashboard.
Just below the hamburger icon in the upper right corner, you might see a small drop-down box.
- Click the **drop-down** and select **Dashboard**
- Click on **Theme** <br>
  Set everything to your preferrence.

----------

#### 3.3 Menu style `(optional)`
Node-red allows you to modify some menu behaviour of the dashboard.
Just below the hamburger icon (from chapter 3.1 MQTT) you see a small drop-down box.
- Click the **drop-down** and select **Dashboard**
- Click on **Site** <br>
  Here you can modify the Dashboard Title, the sidebar look and feel, swiping behavior. 

[Top](#top) / [Back](../readme.md)

**********

### 4 Deploy the flow
If you make changes in Node-Red, the changes are not instantly live. You still need to deploy the changes. 
- Click on **Deploy** in the upper right corner.<br>

> [!TIP]
> Click the **drop-down** icon on the [Deploy] button and select **Modified Nodes**<br>
> <br>
> Selecting this deploy method, makes deploying small changes to a flow a lot less impactful for the entire system. It only deploys nodes that have been changed. So if you make a small modification somewhere, only those changes will be re-initialized. 

[Top](#top) / [Back](../readme.md)

******
