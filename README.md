# Climate `change event : 7-9th Feb 2020

## Get an IBMId and IBM Cloud login

Create your IBM ID account on http://ibm.biz/OxAI-2020-hack. Your username is your Oxford University email address ending in ox.ac.uk and a password of your choice. You will need to verify your account through the email your receive in your Inbox.

Your IBM ID can nbe enabled to a large number of facilities - for now you will have had an IBM Cloud instance created for you and linked to your IBM ID.

Login to the https://cloud.ibm.com/login with your IBM ID you just created.

## Introductions

### Architecture

![](https://github.com/kwiatks/climate-change-setup-oxford/blob/master/images/ox-architecture.png)

### Introductions to Physical Analytics Integrated Data Repository and Services (PAIRS)

IBM PAIRS (Physical Analytics Integrated Data Repository and Services) GEOSCOPE is a platform, specifically designed for massive geospatial-temporal data (maps, satellite, weather, drone, IoT), query and analytics services. It frees up data scientists, developers from the cumbersome processes that dominate conventional data preparation and provides search-friendly access to a rich, diverse, and growing catalog of continually updated geospatial-temporal information.  See https://www.ibm.com/uk-en/marketplace/geospatial-big-data-analytics

There is both a Graphical User Interface (GUI) to PAIRS as well as a PAIRS API.

### Introduction to The Weather Company (TWC)

### Introduction to Watson Studio

Test changes from local clone

## Detailed steps for this Event

## Overview

<Diagram>

## PAIRS

There are two modes for using PAIRS, Graphical User Interface (GUI) and via API calls.  When using the GUI version you are presented with Datalayers and DataSets.  This is a one to many relationship (one datalayer contains many datasets).  Datalayers that you have access to are ih this -> ???? file and datasets are here -> ???.

### GUI
All you need to do is register your IBM ID against the PAIRS system - this is carried out as follows :
- Go to https://ibmpairs.mybluemix.net/
- Click "Get Started"
- Click "Sign in using IBMid"
- Enter your IBMid and then click Continue
- Login with your IBMid password
- Read the Terms and conditions and click "I accept the terms"
- You will be presented with the GUI of PAIRS
- Click the circular symbol to the top right of the screen and check your username is shown

There are a few short videos here -> https://www.youtube.com/playlist?list=PL0VD16H1q5IO3sP-i667TVyn4OsSP6kPc that you can look at to understand how to use the GUI version of PAIRS.

You can pick the Clone icon on the Example to have your own version which you can manipulate as required.  For example, scroll down to "UK crop map" and click the clone icon.   

In the Data Explorer view if you know the ID of your dataset then you can enter it's ID in the Search filter field and click enter and the corresponding dataset will be shown.

Once you have decided on the dataset and have shown it on the GUI display you can click anywhere on the map and (if available) a more detailed view of the data *at that point* will be shown.  <need diagram>.  Also, if the Download option is picked the you are presented with some curl commands which can be used to fetch the data from PAIRS directly and stored locally if required.

### APIs
There are APIs to access a wide range of interface and are documented here ->  https://pairs.res.ibm.com/tutorial/documentation/api/core_api_v2.html and the Swagger link -> https://pairs.res.ibm.com/manual/api-doc/


###

<steps on registering your IBM ID so you can call PAIRS>

## TWC

### APIs
The full set of TWC APIs is shown here -> https://docs.google.com/document/d/15Ru_3wdMgpbM4aOCm-4qNAnRfjx2w-Ruw3lnr8Hnodk/edit.  To access them you will need an API key - this is supplied to you in the hackathon material.

Some useful information on using TWC APIs is contained in this PDF -> ???

## Calling PAIRS and TWC within Watson Studio

We will be using IBM Watson Studio and Jupyter Notebooks to call both PAIRS and TWC APIs for this event.  

Before setting up Watson Studio you need to initialise some Cloud Object Store (COS) to hold any data or artifacts you wish to use.

## handy cheat sheets and tutorials
HTML, CSS, JSON, bootstrap, colours, SQL, and more
+ https://www.w3schools.com/

## Markdown documentation
for github, essential Markdown cheat sheet
+ https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
