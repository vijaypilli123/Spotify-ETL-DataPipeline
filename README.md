# Spotify-ETL-DataPipeline
INTRODUCTION
Project Aims in Extracting the top 50 globally played songs in Spotify Application through Spotipy API and transform it in AWS Lambda Environment to desired format and load it to AWS S3 and then crawls the csv data to table data using AWS Glue crawler and the table data can be visualized using Amazon QuickSight.
PROJECT FLOW
1.Open https://developer.spotify.com/dashboard for connecting spotify API
2.Login with spotify credentials
3.Create app (name:python-spotify,des:python-spotify,url:anything)
4.Open settings to view client and secret key
5.Create "spotify-data-engineering" bucket & spotify-raw-data/to-process/ folder to store json data extracted from spotify api
6.Create lambda function "spotify-lambda" to extract data from spotify api.
7.Save client id & client secret in Environment variables of a specific lambda function.
8.Whenever creating lambda file error:no module named spotipy so create a virtual environment
********
create a folder in some directory
open cmd
$python3 -m venv venv
$venv\Scripts\activate
$pip install spotipy
save lambda file to bin\sitepackages 
convert sitepackages to .zip file
 
********
9.Upload zip file to lambda function
##json file saved into s3://spotify-data-engineering/spotify-raw-data/processed/
10.Transform json to csv using lambda function
11.Create crawlers for each loaded csv file
12.Preview table data using Athena
12.Connect to Amazon QuickSight and visualize.
