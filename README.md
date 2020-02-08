# Climate Change event : 7-9th Feb 2020

## Where the IBM team will be

Saturday/Sunday :  We will be downstairs - please  book a formal 15 min mentoring session or just catch one  of us if you see we are free.

## 0.1 Datasets and DataLayers

We have arranged enhanced access to some Datasets/DataLayers for this event.  Datasets contain one or more DataLayers.  Datasets have an ID number and short names and DataLayers have the same (ID + short names).  We are providing a spreadsheet which decribes the mapping and availability of Datasets vs DataLayers.  

Spreadsheet file is here -> [Spreadsheet : It has 410 datalayers for you to look at](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/Oxford%20University%20Hackathon%20Data%20Layer%20Report%20w%20Ratings.xlsx?raw=true)

## 0.2 New Notebooks

Please got to https://github.com/IBM/ibmpairs/tree/master/examples where we have published some Notebooks very relevant to the Climate Change theme of the weekend.  Please see Notebook file ending in .ipynb in each example.

**NOTE** : Do not cut/paste from this github README since there are control characters that get copied across that you can't see and the Python notebook does not like and so execution stop.  Go [here](https://raw.githubusercontent.com/kwiatks/climate-change-setup-oxford/master/pairs-credentials.txt) for tested version of the text you need.

Where you see the following line in any of the Notebooks :

```
PAIRS_SERVER='https://pairs.res.ibm.com'
PAIRS_USER=<username>'
PAIRS_CREDENTIALS = (
    PAIRS_USER, paw.get_pairs_api_password(PAIRS_SERVER, PAIRS_USER, passFile= os.path.expanduser('~/ibmpairspass.txt'))
)
```
  
Replace it with the following lines from [here](https://raw.githubusercontent.com/kwiatks/climate-change-setup-oxford/master/pairs-credentials.txt) :

```
PAIRS_USER=‘<your IBM ID>’
PAIRS_SERVER=’https://oxaihack2020.eu-gb.mybluemix.net'
PAIRS_PASSWORD=‘pairs’
BASE_URI=‘/’
PAIRS_CREDENTIALS=(PAIRS_USER, PAIRS_PASSWORD)
```
## 0.3 TWC API-keys

TWC API-keys are [File in this github](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/twc-api-keys-oxford.txt)
APIs : https://docs.google.com/document/d/15Ru_3wdMgpbM4aOCm-4qNAnRfjx2w-Ruw3lnr8Hnodk/edit

## Important : must do by 9pm on Friday 7th Feb

For people who wish to use the PAIRS GUI or PAIRS APIs we need you to have carried out steps 1 to 3 by **9pm on Fri 7th Feb 2020** so that we are able to add you to a special access group that has been arranged for this event.  This cannot be carried out on Saturday or Sunday.

## 1. MUST DO : Get an IBM ID and IBM Cloud account

- Go to https://ibm.biz/Bdzwwi and fill in the form using your Oxford University email address ending in **ox.ac.uk** and a password of your choice
- An IBM ID and IBM Cloud account will be automatically provisioned for you.  The IBM ID is your email
- Verify your account through the email you receive in your Inbox
- Login to the https://cloud.ibm.com/login to check that you see the initial Dashboard page -  you will use this account when using Watson Studio

## 2. MUST DO : Register your IBM ID to get access to PAIRS GUI

You must have done step 1 above before doing this step, an active IBM ID is required.

- Go to https://ibmpairs.mybluemix.net/
- **NOTE** we have seen issues in the Safari browser that a blank page is returned the first time you go to this link.  Just Refresh and all should be OK
- Click "Get Started"
- Click "Sign in using IBM ID"
- Enter your IBM ID and then click Continue
- Login with your IBMid password
- Read the Terms and conditions and click "I accept the terms"
- You will be presented with the GUI of PAIRS
- Click the circular symbol to the top right of the screen and check your username is shown
- You are now part of the Trial group.  The PAIRS team will monitor all users with **ox.ac.uk** in their email and move them to the Oxford group to give you access to a large number of datalayers in PAIRS

## 3. MUST DO : Register your IBM ID to get access to PAIRS APIs

You must have done step 1 above before doing this step, an active IBM ID is required.

In order to allow your IBM ID access to the PAIRS APIs you will need to register your IBM ID.

**NOTE** When you click on the link below you will be asked to fill in your IBM ID and a password.  Do **NOT** enter your IBM ID password in the Password field - put 'pairs' (lowercase, without quotes) instead.

- Use Firefox or Safari browsers and go to https://oxaihack2020.eu-gb.mybluemix.net/api-auth

- At the username/password prompt, enter your IBM ID.  **DO NOT** use your IBM password for password field, just type 'pairs' (lowercase, without quotes). Click OK
- You will see long string of characters returned (example 80889d27-e42a-4e13-8f37-4829659620cc, your text will be different to this example), save the reply to a text editor of your choice
- Refresh your browser to go to the same link and you should get a reply which contains your IBM ID email (example : {"_id":"pairs-**your IBM ID**","_rev":"1-c7a7500961d845a7ce0f8ea8a430295a","token":"80889d27-e42a-4e13-8f37-4829659620cc"}), this confirms you are registered to call the PAIRS APIs initerface
- Save away the reply to a text editor of your choice



## OVERVIEW

### Architecture

An overview of the architecture is shown below. 

For this event, we have created a PAIRS Proxy to provide more rights than a standard User would be given.  In a normal architecture this Proxy is not present and an end users access rights are controlled by the PAIRS group they are assigned 
to.

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/ox-architecture.png)

### Useful background links

- PAIRS - IBM PAIRS GEOSCOPE is a platform, specifically designed for massive geospatial-temporal data (maps, satellite, weather, drone, IoT), query and analytics services. It frees up data scientists, developers from the cumbersome processes that dominate conventional data preparation and provides search-friendly access to a rich, diverse, and growing catalog of continually updated geospatial-temporal information. See https://www.ibm.com/uk-en/marketplace/geospatial-big-data-analytics

- TWC - The Weather Company, delivers personalized, actionable insights to consumers and businesses across the globe by combining the world’s most accurate weather data with industry-leading AI, Internet of Things (IoT) and analytics technologies. See https://www.ibm.com/weather. See https://www.ibm.com/weather

- IBM Watson Studio is a data science and machine learning platform built from the ground up for an AI-powered business. It helps simplify the process of experimentation to deployment, speed data exploration and model development and training, and scale data science operations across the lifecycle.  Watson Studio can exist in the IBM Cloud as well as locally within your own in-premise data centre or even be installed in other Cloud providers solutions.  See https://www.ibm.com/uk-en/cloud/watson-studio and  https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=analytics

### PAIRS

There are two modes for using PAIRS, Graphical User Interface (GUI) and via API calls.  There are "Datasets" and "DataLayers". There is a one to many relationship (a dataset contains one or more datalayers). A CSV file showing the datasets/datalayers will be shared with you during the Event (see Step 2 above).  We recommend you take some time looking at the contents **before** using the GUI and/or APIs to determine if some DataLayers are relevant to your idea.

#### PAIRS GUI

We recomend quickly going through the videos (they are each very short) to become familiar with the interface and then go to the step by step instructions while also looking at the online tutorial :

- There are a few short videos https://www.youtube.com/playlist?list=PL0VD16H1q5IO3sP-i667TVyn4OsSP6kPc
- Online PAIRS GUI Tutorial https://pairs.res.ibm.com/tutorial/tutorials/gui/index.html
- Step by step instructions for this event are shown [here](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/README.md#pairs-gui)

#### PAIRS APIs

Documentation for PAIRS APIs.  We recomend quickly going becoming familiar with the APIs and then go to the step by step instructions :

-  Online PAIRS API Tutorial https://pairs.res.ibm.com/tutorial/documentation/api/core_api_v2.html
- Swagger https://pairs.res.ibm.com/manual/api-doc/.  NOTE : you will not be able to use the 'Try it' option in the Swagger website against the API you wish to investigate - contact one of the IBMers if you need to run this feature in the Swagger webpage. You can of course call the APIs when within Watsoon Studio (see below).

- Step by step instructions for this event are shown [here](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/README.md#calling-pairs-and-twc-apis-within-watson-studio)

### TWC

#### APIs
We have arranaged for you to have access to Historic and Forecast APIs.  The full set of TWC APIs is shown [here](https://docs.google.com/document/d/15Ru_3wdMgpbM4aOCm-4qNAnRfjx2w-Ruw3lnr8Hnodk/edit)

Some additional useful information on using TWC APIs is contained in this [PDF](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/TWC-Data-Package-Summary.pdf)

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

We are now going to Import a Project file that contains two Notebooks : 

- Winchester-datalayer-sample : Replicates the same data as shown in the PAIRS GUI steps above
- External-github-pairs-example : A wide range of calls to multiple datalayers

The Project zip file is located [here](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/Sample-climate-change-project-final-v1.zip).  Please click on this link and download it to your local machine and then follow the steps below.

### Setting up Watson Studio for the first time

Go to https://cloud.ibm.com/login and login with your IBM ID.  You should see the Dashboard page

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/001-ws.png)

Type 'watson studio' in the Search field, the icon with auto filter.  Click on the Watson Studio icon

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/002-ws.png)

Make sure the Lite Plan is picked and click Create

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/003-ws.png)

Click the Get Started button

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/004-ws.png)

Click the Get Started button again

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/005-ws.png)

Click the. New. Project button

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/006-ws.png)

Click on Create a project from a sample or file

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/017-ws.png)

We now need to create a Cloud Object Store for Watson Studio to use.  On the right of the screen in the Definie storage section click Add

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/008-ws.png)

You will see the Cloud Object Storage page

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/009-ws.png)

Scroll down and click Create

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/010-ws.png)

Click Confirm

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/011-ws.png)

Click Refresh and make sure ann entry appears under the Storage section

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/031-ws.png)

In the Upload file section click on **browse** and locate the zip file you downloaded

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/018-ws.png)

Make sure the zip filename is shown.  Name the project (a suggestion is to use your team name in the name somewhere in the project name).  Click Create

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/019-ws.png)

Wait for the Import

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/020-ws.png)

Wait for the successfully created prompt.  Click View all projects

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/021-ws.png)

Click on Assets. You should see two Notebooks

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/022-ws.png)

Click on Winchester-datalayer-sample.  And then click on the Pencil icon

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/023-ws.png)

Check that "1vCPU and 4 GB RAM and is free" is shown.  This is important since if anything else is shown then you will start consuming resources in the Lite account and could possibly run out of the 50 vCPU hours allocated to free accounts.

**If you create a new Notebook always pick "1vCPU and 4 GB RAM and is free" for the environment** otherwise your Lite IBM Cloud account will use it's resources and there will become a point where the Notebook will be locked unless  you revert back to the "1vCPU and 4 GB RAM and is free" level.

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/024-ws.png)

**VERY IMPORTANT** Change <enter your IBM ID here> to your IBM ID leaving all other parameters As-is
  
![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/025-ws.png)

Save the Notebook. **IMPORTANT** Please regularly click this icon when making changes so that any changes are saved

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/026-ws.png)

Click the Restart Kernel and run the whole Notebook icon

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/027-ws.png)

Click Restart and Run All Cells

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/028-ws.png)

The page will jump to the end of the Notebook to show that all Cells will be run in sequence

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/029-ws.png)

Scroll to the top and you will see various Cells being executed.  Ones that have a " * " indicate that the Cell is still running.  Once the Notebook has completed then you can see the outputs from each Cell

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/030-ws.png)

Look at the Notebook to see how various PAIRS APIs are used.  Good luck on your teams activities !!!







