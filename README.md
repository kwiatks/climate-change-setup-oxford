# Climate Change event : 7-9th Feb 2020

## Where the IBM team will be

We will be in the Large Meeting Room (LMR) upstairs in the Foundry.  Please come along to it to ask any questions you may have.  We will also be going round to each team if you have made a specifc request.

For people who wish to use the PAIRS GUI or PAIRS APIs we need to know your IBM ID by 8:20pm on Fri 7th Feb 2020 so that we are able to add you to a special access that has been arranged for this event.

## 1. MUST DO : Get an IBM ID

Go to http://ibm.biz/cloud-account and fill in the form using your Oxford University email address ending in *ox.ac.uk* and a password of your choice. You will need to verify your account through the email your receive in your Inbox.  An IBM Cloud account would have been provisioned for you.

Once you have confirmed that an IBM ID has been created login to the https://cloud.ibm.com/login with your IBM ID you just created - you will use this account later.

## 2. MUST DO : Register your IBM ID to get access to PAIRS GUI

- Go to https://ibmpairs.mybluemix.net/
- Click "Get Started"
- Click "Sign in using IBMid"
- Enter your IBMid and then click Continue
- Login with your IBMid password
- Read the Terms and conditions and click "I accept the terms"
- You will be presented with the GUI of PAIRS
- Click the circular symbol to the top right of the screen and check your username is shown
- You are now part of the Trial group

- IMPORTANT : Notify the IBM team of your IBM ID (your email) since we have arranged for special access to some datasets that are not usually available.  They will add you to the Oxford Group.

## 3. MUST DO : Register your IBM ID to get access to PAIRS APIs

In order to allow your IBM ID access to the PAIRS APIs you will need to register your IBM ID by going to this website http://ibm.biz/pairs-api-register.  

- Enter your IBM ID (email) and for the password enter 'pairs' (lowercase, without quotes)
- You will see an ID on the screen. (like 80889d27-e42a-4e13-8f37-4829659620cc) , save the reply to your own text editor of choice but you do not need it again
- Refresh your browser to go to the same link and you should get a reply which contains your IBM ID email, this confirms you are registered to call the PAIRS API (example : {"_id":"pairs-youremail","_rev":"1-c7a7500961d845a7ce0f8ea8a430295a","token":"80889d27-e42a-4e13-8f37-4829659620cc"})
- You will test access to the APIs within a Watson Studio Notebook

## Overviews

### Architecture

An overview of the architecture is shown below. We have introduced a PAIRS Proxy just for this event so as to be able to hide access to the details of a special username/password which gives us more rights then a standard user would be given.  In a normal architecture this Proxy is not present and an end users access rights are control but which PAIRS group they are assigned to.

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/ox-architecture.png)

### Introductions to Physical Analytics Integrated Data Repository and Services (PAIRS)

IBM PAIRS (Physical Analytics Integrated Data Repository and Services) GEOSCOPE is a platform, specifically designed for massive geospatial-temporal data (maps, satellite, weather, drone, IoT), query and analytics services. It frees up data scientists, developers from the cumbersome processes that dominate conventional data preparation and provides search-friendly access to a rich, diverse, and growing catalog of continually updated geospatial-temporal information.  See https://www.ibm.com/uk-en/marketplace/geospatial-big-data-analytics

There is both a Graphical User Interface (GUI) to PAIRS as well as a PAIRS API.

### Introduction to The Weather Company (TWC)

The Weather Company, delivers personalized, actionable insights to consumers and businesses across the globe by combining the world’s most accurate weather data with industry-leading AI, Internet of Things (IoT) and analytics technologies. See https://www.ibm.com/weather.

### Introduction to Watson Studio

IBM Watson Studio is a data science and machine learning platform built from the ground up for an AI-powered business. It helps simplify the process of experimentation to deployment, speed data exploration and model development and training, and scale data science operations across the lifecycle.  See https://www.ibm.com/uk-en/cloud/watson-studio

### PAIRS

There are two modes for using PAIRS, Graphical User Interface (GUI) and via API calls.  When using the GUI version you are presented with Datalayers and DataSets.  There is a one to many relationship (a dataset contains many datalayers). A CSV file showing the datasets/datalayers will be shared with you during the Event.  We recommend you take some time looking at the contents before using the GUI and/or APIs to determine if there are already some datalayers available that are relevant to your idea.

#### PAIRS GUI

Video and documentation for PAIRS GUI :

- There are a few short videos https://www.youtube.com/playlist?list=PL0VD16H1q5IO3sP-i667TVyn4OsSP6kPc
- Online PAIRS GUI Tutorial https://pairs.res.ibm.com/tutorial/tutorials/gui/index.html
- Detailed steps are described in ???? below

#### PAIRS APIs

Documentation :
-  Online PAIRS GUI Tutorial https://pairs.res.ibm.com/tutorial/documentation/api/core_api_v2.html
- Swagger https://pairs.res.ibm.com/manual/api-doc/.  NOTE : you will not be able to use the 'Try it' option in the Swagger website - contact one of the IBMers if you need to run the Swagger functionality.
- Detailed steps are described in ??? below

### TWC

#### APIs
The full set of TWC APIs is shown [here](https://docs.google.com/document/d/15Ru_3wdMgpbM4aOCm-4qNAnRfjx2w-Ruw3lnr8Hnodk/edit).  To access them you will need an API key - this is supplied to you during the Event by the IBM team.

Some useful information on using TWC APIs is contained in this [PDF](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/TWC%20Data%20Package%20Summary.pdf).

## Details

### PAIRS GUI

This section shows how to use the PAIRS GUI functionality in a sample datalayer over Winchester in Hampshire.

Make sure you are logged in
![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-001.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-002.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-003.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-004.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-005.png)


![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-006.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-007.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-008.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-009.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-010.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-011.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-012.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-013.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-014.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-015.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-016.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-017.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-018.png)


![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-019.png)


![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-020.png)


![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-021.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-022.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/p-gui-023.png)

## Calling PAIRS and TWC APIs within Watson Studio

We will be using IBM Watson Studio and Jupyter Notebooks to call both PAIRS and TWC APIs for this event.  Once teams have been formed, emails of the technical representatives in each team will be collected and detailed instuctions shared with them.

### Setting up Watson Studio for the first time

Go to https://cloud.ibm.com/login and login with your IBM ID

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/001-cc-dash.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/002-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/003-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/004-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/005-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/006-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/007-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/008-ws.png)



![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/009-ws.png)
