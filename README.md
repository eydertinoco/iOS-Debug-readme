# iOS-Debug-readme

But what if we want to debug a website opened in a Safari browser inside a iPad/iPhone ??. Its look pretty difficult right  as you don't find any option like F12 to inspect the elements.

But these  is not impossible .There is a way using which you can achieve it and debug the site like in Windows/mac machine and identify the cause if the functionality is not working in Mobile devices.

Below are the steps which you need to follow to do a complete setup before you start debugging your site.

1. Install Node Js

Nodejs downlaod Link

2. Install I-tunes on windows 10 PC

Install i-tunes link

3.Open Windows Power-shell as a administrator

4.Execute below commands

npm install remotedebug-ios-webkit-adapter -g

“updated 1 package in Xs” is displayed once completed

5.Connect your iOS device to your Windows 10 PC via USB.

6.Establish trust

7.Install Scoop using below command-Scoop is a command line installer that you will be using to install other tools.
To install it make sure you have PowerShell 3 or later, installed in your machine and .NET Framework 4.5 or later.

To know Power sheel version
$PSVersionTable.PSVersion

To install scoop
iex (new-object net.webclient).downloadstring('https://get.scoop.sh')


if you get error during installation ,update the policy
Set-ExecutionPolicy RemoteSigned -scope CurrentUser

8.Scoop Extras is an extra bucket that will allow you to install the remaining dependencies. To do it, go on the PowerShell console and run:

scoop bucket add extras

9.Install Git so you can access the WebKit debugger Proxy and the Adapter. In the PowerShell console, run the following command:

scoop install git


10.iOS WebKit Debug Proxy allows debugging in iOS by managing the requests from the Adapter. To install it, run the following command in the PowerShell:

scoop install ios-webkit-debug-proxy

11.The libimobiledevice library. This is the tool that will help you communicate with any iOS device that you are using in your debug. To install it, just go on the PowerShell console and run:

npm install -g vs-libimobile

12.To install it, open the PowerShell console and install the package for the WebKit Adapter by running the following command:

npm install remotedebug-ios-webkit-adapter -g

13.Start the webkit adapter plugin listening on port 9000.
Paste the following command into PowerShell:
remotedebug_ios_webkit_adapter --port=9000

14.Open up the Chrome browser and browse to chrome://inspect/#devices.

15. click on configure and set localhost:9000

16. In ipad goto setting--Safari--- Advance--Enable web inspector

17. Open any website in safari

18.Now you an see the website in chrome under Remote target

These Video will help you to debug your website from Ipad/Iphone safari browser using windows 10 and without a mac machine
Debugging Website from iPad/iPhone safari browser using windows 10. 

Fonte: https://developingtestingskills.blogspot.com/2021/01/debugging-website-from-ipadiphone.html
