## Overview


BigQuery is Google's fully managed, NoOps, low cost analytics database. With BigQuery you can query terabytes and terabytes of data without managing infrastructure or needing a database administrator. BigQuery uses SQL and takes advantage of the pay-as-you-go model. BigQuery allows you to focus on analyzing data to find meaningful insights.

We have a newly available dataset for NCAA Basketball games, teams, and players. The game data covers play-by-play and box scores back to 2009, as well as final scores back to 1996. Additional data about wins and losses goes back to the 1894-5 season in some teams' cases.

In this lab we will find and query the NCAA dataset using BigQuery.

What you'll learn
Using BigQuery

Query the NCAA Public Dataset

Writing and executing queries

What you'll need
A Google Cloud Project

A Browser, such Chrome or Firefox

Setup and Requirements
Before you click the Start Lab button
Read these instructions. Labs are timed and you cannot pause them. The timer, which starts when you click Start Lab, shows how long Google Cloud resources will be made available to you.

This Qwiklabs hands-on lab lets you do the lab activities yourself in a real cloud environment, not in a simulation or demo environment. It does so by giving you new, temporary credentials that you use to sign in and access Google Cloud for the duration of the lab.

What you need
To complete this lab, you need:

Access to a standard internet browser (Chrome browser recommended).
Time to complete the lab.
Note: If you already have your own personal Google Cloud account or project, do not use it for this lab.

Note: If you are using a Chrome OS device, open an Incognito window to run this lab.

How to start your lab and sign in to the Google Cloud Console
Click the Start Lab button. If you need to pay for the lab, a pop-up opens for you to select your payment method. On the left is a panel populated with the temporary credentials that you must use for this lab.

Open Google Console

Copy the username, and then click Open Google Console. The lab spins up resources, and then opens another tab that shows the Sign in page.

Sign in

Tip: Open the tabs in separate windows, side-by-side.

If you see the Choose an account page, click Use Another Account. Choose an account
In the Sign in page, paste the username that you copied from the Connection Details panel. Then copy and paste the password.

Important: You must use the credentials from the Connection Details panel. Do not use your Qwiklabs credentials. If you have your own Google Cloud account, do not use it for this lab (avoids incurring charges).

Click through the subsequent pages:

Accept the terms and conditions.
Do not add recovery options or two-factor authentication (because this is a temporary account).
Do not sign up for free trials.
After a few moments, the Cloud Console opens in this tab.

Note: You can view the menu with a list of Google Cloud Products and Services by clicking the Navigation menu at the top-left. Cloud Console Menu
Open BigQuery Console
In the Google Cloud Console, select Navigation menu > BigQuery:

BigQuery_menu.png

The Welcome to BigQuery in the Cloud Console message box opens. This message box provides a link to the quickstart guide and the release notes.

Click Done.

The BigQuery console opens.

bq-console.png

BigQuery opens, but there's nothing in here! Luckily, there are tons of Open Datasets available in BigQuery for you to query, and of course you can upload your own data, which you'll do in the next section.

Find the NCAA public dataset in BigQuery
In this section, you pull in some public data so you can practice running SQL commands in BigQuery. Click on the + ADD DATA link then select Explore public datasets:

BQ_UI_Add_Data.png

Type "ncaa basketball" in the searchbar and press Enter.

Click on the NCAA Basketball tile, then View Dataset.

A new browser tab opens, you now have a new project called bigquery-public-data added to the Explorer panel, opened to ncaa_basketball:

BQ_UI_2_proj.png

Click on the dataset name to view the tables you can explore.

BQ_ncaa_tables2.png

Click on mbb_teams_games_sr (men's NCAA game results table) and then click Preview tab to see sample rows of data. Click the Details tab to get metadata about the table.

BQ_UI_Details_Preview.png

How many games does the dataset contain? How big is the table?

BQ_UI_ncaa-table-size.png

Answer: The table is about 50 MB and there are over 29k games for us to explore.

But how many individual plays can we analyze?

Hint: click on the mbb_pbp_sr (play-by-play) dataset:

ncaa_mbb_pbp_rs_table.png

Then click Details:

BQ_UI_ncaa_MBB-PBP-SR.png

Answer: Over 4 million individual basketball plays.

Let’s write some SQL to see what types of plays are there for us to explore.


# Congratulations!


You've learned how to query the NCAA basketball dataset inside of BigQuery. We encourage you to modify the above queries and write your own to further your understanding. Looking for more NCAA query practice? Checkout the GitHub repo here.
