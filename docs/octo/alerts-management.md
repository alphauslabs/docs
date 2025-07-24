# Alerts Management

As of this writing, Octo has four types of alerts: **cost**, **anomaly detection**, **discount expiration** and **budget alert** . We'll be discussing how to create alerts on each type. Before this, make sure you have at least one channel created in the Channel Management page.

## Navigate to the Alerts Management Tab

![Alert Management](https://drive.google.com/uc?export=view&id=1zVO5isuW9cVdJYIUmetStjX4_yQaqAx5)

- Locate the gear or cog icon on the top right corner of the app header, just beside your profile picture. You will see a curation of tabs
- Under the the `NOTIFICATION` section, click `Alerts Management`
## Creating an Alert

### Cost Alert

Cost alerts aide in monitoring your cost groups' daily spend. You can monitor multiple cost groups and send alerts to multiple channels per alert. There are two types of threshold available: **fixed cost** and **percentage compared to previous day**. For the fixed cost, you supply the amount you want to be the limit for the cost group/s' daily spend and Octo will send an alert to the designated channel once your spend exceeds this limit. As for the percentage compared to the previous day's spend, the number you input will be used to measure if the day's spend exceeds the specific percentage of the previous day's spend.

![Cost](https://drive.google.com/uc?export=view&id=1PdrfMBUwAwzQ3UJLE9C6OXhz_KihQ3Cq)

- Navigate to the `COST` tab
- Click `CREATE NEW ALERT` and a popup dialogue box should appear
- Supply the alert name
- Choose one or multiple cost groups and click `NEXT`

![Create Cost Alert](https://drive.google.com/uc?export=view&id=1kZdnalPzuo3s79rdN-OZP9Lngky5ekxI)

- Select if you would opt for the fixed or percentage type of alert
- Supply the fixed amount or percentage
- Select which channels you would like the alerts to be sent to
- Click `CREATE ALERT`

<!-- ### Anomaly Detection Alert -->
### Anomaly Detection Alert

Anomaly detection alerts are used to monitor a cost group if there is an anomaly and alert you if there is a significant deviation from the usual spending based from your historical data. You can monitor single cost group and send alerts to multiple channels. 

![Anomaly](https://drive.google.com/uc?export=view&id=136JtdAOnqaLhWkPhxESHEEW4N8Bkwnfs)

- Navigate to the `ANOMALY DETECTION` tab
- Click `CREATE NEW ALERT` and a popup dialogue box should appear
- Supply the alert name
- Choose one cost group and click `NEXT`

![Create Anomaly ALert](https://drive.google.com/uc?export=view&id=1qJa-26r-aLhQqOPTe6D_QjnJOUO2vfDE)

- Choose the frequency of the alert (weekly,monthly)
- Select which channels you would like the alerts to be sent to
- Click `CREATE ALERT` 

### Discount Expiration Alert

The Discount Expiration Alert feature allows you to monitor the expiration dates of your purchased discounts, such as Reserved Instances and Savings Plans in AWS.
Currently, this feature supports **AWS** only. To create a new alert, follow the steps below.

![Discount Alert](https://drive.google.com/uc?export=view&id=176bfQnzeSdaEgJPkKnKjwh2r5fqbgxm1)

- Navigate to the `DISCOUNT EXPIRATION` tab
- Click `CREATE NEW ALERT` and a popup dialog box should appear
- Supply the alert name
- Choose one cost group. This tracks the discount plans associated with this cost group. Then, click `NEXT`

![Create Discount Alert](https://drive.google.com/uc?export=view&id=1rSX8dmInKuFTDLb5jf4rTupGIAD4p5pm)

- Select frequencies. You can choose as many as needed.
- Select which channels you would like the alerts to be sent to
- Click `CREATE ALERT`

### Budget Alert

The Budget Alert feature allows you to receive notifications when your spending exceeds your budget. These alerts help you stay informed about any budget overruns.

**Note:** To create a budget alert, make sure you have already created a budget.

![Budget Alert](https://drive.google.com/uc?export=view&id=1Nd1DjslUmNQrgodp1bny3Mts26hnqotW)

- Navigate to the `BUDGET ALERT` tab  
- Click the `View Details` of an existing budget  

![Create Budget Alert](https://drive.google.com/uc?export=view&id=1-DMIjzO89_XEXUVen7L3gfcbmgMfq0ug)
![Create Budget Alert](https://drive.google.com/uc?export=view&id=1rXHbcfHKUgJkIQ1XsaTsJQZGTRFBVkzi)

- Click `CREATE BUDGET ALERT` and a popup dialog box should appear  

![Create Budget Alert](https://drive.google.com/uc?export=view&id=1IM9AXLCOfGlCoApBFi_fz44U9qMQG7ON)

- Set both a cost value and a percentage of your total budget to define when the alert should be triggered. The alert will notify you once your spending reaches either the specified amount or the specified percentage of your budget. 
- Select which channels you would like the alerts to be sent to  
- Click `CREATE ALERT`


## Editing an Alert

![Edit](https://drive.google.com/uc?export=view&id=1ayjfEX2NSF-p4LWCBfbKKEdzeeEcW8eq)

- Editing alerts are pretty similar to creating one
- Navigate to the tab of the desired alert type
- Locate the specific alert you want to edit and click the pen icon on the far right side just beside the transh icon
- A popup dialogue box should appear and you can edit the information as you wish

## Deleting an Alert

![Delete](https://drive.google.com/uc?export=view&id=1HeENZzvSmN6nl81eS9eiNPy6hsIhMnzS)

- Navigate to the tab of the desired alert type
- Locate the specific alert you want to delete and click the trash icon on the far right side
- Confirm the deletion

## Enable/Disable an Alert (Anomaly Detection and Discount Expiration Alerts)

- Navigate to the actions column of the specific alert
- Click the toggle switch to enable or disable the alert