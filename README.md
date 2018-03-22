# Week8-liveAttack
the is the week8 assignment for CodePath.
# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL injection.

Steps:

Go to the blue website without loging in click on find a sales person, open Sqlmap and run it against the given URL

sqlmap --url https://35.224.228.84/blue/public/salesperson.php?id=4 --dbs to check for Databases, the Sqlmap revealed 

7, available databases [7]. One of them is globitek_blue, run the command in Sqlmap against the given database 

sqlmap --url https://35.224.228.84/blue/public/salesperson.php?id=4 -D globitek_blue

Sqlmap found it vulnerable to SQL Injection with this given syntax id=4' OR SLEEP(5) AND 'ZAWi'='ZAWi

GIF Walkthrough:
![sqliblue](https://user-images.githubusercontent.com/30760006/37753372-c5a18d72-2d59-11e8-80e8-74fd7e36a817.gif)



Vulnerability #2: __________________


## Green

Vulnerability #1: XSS Cross-Site Scripting

steps 

click on the contact us tab which gives an option to send a feed back fill out the form and include the Java Scipt alert script

when the admin logs in and click to see the feedback the script will be trigerred

GIF Walkthrough:
![xssgreen](https://user-images.githubusercontent.com/30760006/37758809-c8c695e6-2d6e-11e8-949b-0b8cdcfb3a43.gif)

Vulnerability #2: __________________


## Red

Vulnerability #1: __________________

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work
