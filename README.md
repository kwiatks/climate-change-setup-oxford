# Climate Change event : 7-9th Feb 2020

## Where the IBM team will be

We will be in the Large Meeting Room (LMR) upstairs in the Foundry.  Please come along to it to ask any questions you may have.  We will also be going round to each team if you have made a specifc request.

## Important : must do by 8:40pm on Friday 7th Feb

For people who wish to use the PAIRS GUI or PAIRS APIs we need you to have carried out steps 1 to 3  by **8:40pm on Fri 7th Feb 2020** so that we are able to add you to a special access group that has been arranged for this event.  This cannot be carried out on Saturday or Sunday.

## 1. MUST DO : Get an IBM ID

Go to http://ibm.biz/cloud-account and fill in the form using your Oxford University email address ending in **ox.ac.uk** and a password of your choice. You will need to verify your account through the email your receive in your Inbox.  An IBM Cloud account would have been provisioned for you.

Once you have confirmed that an IBM ID has been created, login to the https://cloud.ibm.com/login with it - you will use this account later.

## 2. MUST DO : Register your IBM ID to get access to PAIRS GUI

You must have done item 1 above before doing this step, you need an active IBM ID.

- Go to https://ibmpairs.mybluemix.net/
- **NOTE** we have seen issues that a blank page is returned the first time you go to this link.  Just Refresh and all should be OK
- Click "Get Started"
- Click "Sign in using IBM ID"
- Enter your IBM ID and then click Continue
- Login with your IBMid password
- Read the Terms and conditions and click "I accept the terms"
- You will be presented with the GUI of PAIRS
- Click the circular symbol to the top right of the screen and check your username is shown
- You are now part of the Trial group

- **VERY IMPORTANT** : Pass on your IBM ID to one of the IBM team (who will be in the Large Meeting Room (LMR) upstairs from 6:45pm) since we have arranged for special access to some datasets that are not usually available.  They will add you to the Oxford Group.  We MUST carry this out by 8:40pm or so on Fri 7th Feb 2020.

## 3. MUST DO : Register your IBM ID to get access to PAIRS APIs

You must have done item 1 above before doing this step, you need an active IBM ID.

In order to allow your IBM ID access to the PAIRS APIs you will need to register your IBM ID.

- Go to http://ibm.biz/pairs-api-register 
- At the username/password prompt, enter your IBM ID (your email)
- **DO NOT** put your IBM password for password field, just type 'pairs' (lowercase, without quotes)
- You will see long string of characters returned (example 80889d27-e42a-4e13-8f37-4829659620cc, your text will be different to this example), save the reply to your text editor of choice
- Refresh your browser to go to the same link and you should get a reply which contains your IBM ID email (example : {"_id":"pairs-**your IBM ID (ie. your email)**","_rev":"1-c7a7500961d845a7ce0f8ea8a430295a","token":"80889d27-e42a-4e13-8f37-4829659620cc"}), this confirms you are registered to call the PAIRS APIs
- Save away the reply
- You will not need to use the reply text but it will be useful to have to show IBMers that you have followed the above steps for any debug steps

## OVERVIEW

### Architecture

An overview of the architecture is shown below. We have introduced a PAIRS Proxy just for this event so as to be able to hide access to the details of a special username/password which gives us more rights then a standard user would be given.  In a normal architecture this Proxy is not present and an end users access rights are control but which PAIRS group they are assigned to.

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/ox-architecture.png)

### Useful background links

- PAIRS - IBM PAIRS GEOSCOPE is a platform, specifically designed for massive geospatial-temporal data (maps, satellite, weather, drone, IoT), query and analytics services. It frees up data scientists, developers from the cumbersome processes that dominate conventional data preparation and provides search-friendly access to a rich, diverse, and growing catalog of continually updated geospatial-temporal information. See https://www.ibm.com/uk-en/marketplace/geospatial-big-data-analytics

- TWC - The Weather Company, delivers personalized, actionable insights to consumers and businesses across the globe by combining the world’s most accurate weather data with industry-leading AI, Internet of Things (IoT) and analytics technologies. See https://www.ibm.com/weather. See https://www.ibm.com/weather

- IBM Watson Studio is a data science and machine learning platform built from the ground up for an AI-powered business. It helps simplify the process of experimentation to deployment, speed data exploration and model development and training, and scale data science operations across the lifecycle.  See https://www.ibm.com/uk-en/cloud/watson-studio and  https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=analytics

### PAIRS

There are two modes for using PAIRS, Graphical User Interface (GUI) and via API calls.  When using the GUI version you are presented with Datalayers and DataSets.  There is a one to many relationship (a dataset contains many datalayers). A CSV file showing the datasets/datalayers will be shared with you during the Event (it will be emailed to you).  We recommend you take some time looking at the contents **before** using the GUI and/or APIs to determine if there are already some datalayers available that are relevant to your idea.

#### PAIRS GUI

Video and documentation for PAIRS GUI.  We recomend quickly going through the video to become familiar withh the interface and then go to the step by step instructions :

- There are a few short videos https://www.youtube.com/playlist?list=PL0VD16H1q5IO3sP-i667TVyn4OsSP6kPc
- Online PAIRS GUI Tutorial https://pairs.res.ibm.com/tutorial/tutorials/gui/index.html
- Step by step instructions for this event are shown [here](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/README.md#pairs-gui)

#### PAIRS APIs

Documentation for PAIRS APIs.  We recomend quickly going becoming familiar with the APIs and then go to the step by step instructions :

-  Online PAIRS GUI Tutorial https://pairs.res.ibm.com/tutorial/documentation/api/core_api_v2.html
- Swagger https://pairs.res.ibm.com/manual/api-doc/.  NOTE : you will not be able to use the 'Try it' option in the Swagger website against the API you wish to investigate - contact one of the IBMers if you need to run this feature in the Swagger webpage
- Step by step instructions for this event are shown [here](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/README.md#calling-pairs-and-twc-apis-within-watson-studio) below

### TWC

#### APIs
We have arranaged for you to have access to Historic and Forecast APIs.  The full set of TWC APIs is shown [here](https://docs.google.com/document/d/15Ru_3wdMgpbM4aOCm-4qNAnRfjx2w-Ruw3lnr8Hnodk/edit).  To access them you will need an two API keys - this is supplied to you during the Event by the IBM team (will be emailed to you using whatever email you used in steps 1 to 3 at the top of this README).

Some useful information on using TWC APIs is contained in this [PDF](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/TWC%20Data%20Package%20Summary.pdf)

### Watson Studio

Documentation : 

- https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/overview-ws.html?context=analytics&linkInPage=true

## DETAILS

### PAIRS GUI

This section shows how to use the PAIRS GUI functionality on a datalayer over Winchester in Hampshire.  It shows how we can use a satellite image to identify an abmormally high value of heat being generated at a specific date in 2019.

Make sure you are logged in
![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-001.png)

Click on the "Data Explorer" option

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-004.png)

Enter 49687 and click Search.  On the Search result click "Data Layers"

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-005.png)

Scroll down the pop up and find 49687 and then click "New query using this layer"

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-006.png)

Click Next

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-007.png)

Zoom the map to the Winchester area (north of Southampton in the South of the UK).  Make sure Rectangle is select and click your mouse once (and then let go) on the map to indicate the start of the rectangle and then drag a rectangle similar to what you see below

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-008.png)

Enter the exact date shown below.  You need to click on each date item to change it. **NOTE** : there is a hint on page indicating for what date ranges this datalayer has data for.  This is important since not all datalayers have data for all dates.  We (IBM) asked for specific data to be created to cover IBM Hurlsey which is close to Wiinchester.  Click Next.

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-009.png)

Do not change an item.  Click Next

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-010.png)

Give youe Query a meaningful name so you can remember what it was doing.  Click "Run query"

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-011.png)

In the Query tab your request is shown running.  Time to get a drink or a bite to eat !!  Come back after a few minutes to check on the status

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-012.png)

Once completed your query will be shown in the "Recent Queries" section of the Queries tab/. Click on the image

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-013.png)

You might just be able to see a red dot in the centre of the image.  Zoom in. to take a closer look.  In the below image, we have clicked on the map just to the left of the red dot - a graph is shown of some historic values at this point.  This shows the value of data at this point as defined in the Legend.  Note the value.

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-015.png)

Click on the red area with your mouse and look at the value again - you will see that it is higher then the previous click that was carried out

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-016.png)

Zoom further into the map and change the Opacity so you can see the map a little more clearly

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-018.png)

Click on the image and press the "Download CSV" button

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-022.png)

A CSV file is created with the values of the point for a range of dates

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-023.png)

From the PAIRS GUI there are a range of option when you click the Actions option on the top left of the page

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-019.png)

Click "Download data".  This will download a zip file to your local machine and this can be viewed in applications like QGIS.

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-020.png)

Click on "Developer tools".  This gives the curl command to create exactly the same query you created manually and another curl command to check the query has finished

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-021.png)



## Calling PAIRS and TWC APIs within Watson Studio

We will be using IBM Watson Studio and Jupyter Notebooks to call both PAIRS and TWC APIs for this event.  

A sample Project file is [here](???) and will be Imported to your Watson Studio instance.

### Setting up Watson Studio for the first time

Go to https://cloud.ibm.com/login and login with your IBM ID.  You should see the Dashboard page

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/001-ws.png)

Type 'watson studio' in the Search field, the icon with auto filter.  Click on the Watson Studio icon

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/002-ws.png)

Make sure the Lite Plan is picked and click Create

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/003-ws.png)


![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/004-ws.png)

Click the Get Started button

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/005-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/006-ws.png)

We are now going to Import a Project file that contains two Notebooks.  One show how you can get the same data (for the Winchester area) as shown in the PAIRS GUI steps above.  The other Notebook is from the external PAIRS github of https://github.com/IBM/ibmpairs/tree/master/tutorials and shows a wide range of PAIRS API calls.



