# P-Set2-Creating-a-Windows-Service
I'll explain what a windows service is show you how to create one by creating a windows service with my name to launch calc.exe

# What are Windows Services?

Windows services are very important computer program that operates in the background of the windows operating system. They ensure that processes are able to be created and run continously which provides an efficiently functioning operating system. 

Below is picture of serivices I currently have running after putting up my computer. I'll highlight the steps I used to get to the service application and  give a few explanations of the important things to take note of.   

First things first, search for Services on your home screen search bar

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws1.png)

You will be presented with an interface that shows the services running on the system as shown in the image below

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws2.png)

Now time for some bried explanations

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws3.png)

According to the image above, the Name shows the name tab which lists all of the available services for the operating system.

The "Description" tab gives a detailed description of each service. Clicking on a service shows the description at the left hand side of the screen as seen in the image above.

The "Status" tab shows if the service is runnung or not.

The "Startup Type" shows if it starts up automatically or manually. with the service highlighted "Credential Manager", we need to start it up manually.

# I'll create a service with my name "Stormy" to launch an application "calc.exe" using CMD

First of all, we'll need to get the file path of calc.exe, check the images below to understand the process I took

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws6.png)

Next, I searched for calc.exe

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws7.png)

I double-clicked it and got an error message. (It's a program file, an ordinary user with little or no administrative priviledge cannot access program files)

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws8.png)

I double clicked on it and clicked on "Open file location"

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws9.png)

I double-clicked on the file path bar and selected "Copy address as text"

https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws10.png

I searched for "Command Prompt" and opened it

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws5.png)

I inputed this command:

```

sc create “stormy” binPath= “C:\Program Files\WindowsApps\Microsoft.WindowsCalculator_11.2210.0.0_x64__8wekyb3d8bbwe\setup.exe”

```

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws11.png)

Understanding the Command Prompt code used:

"sc" is a command that is used to install services

"create" tells the computer to create the service "stormy"

"binPath" shows the file path to follow

"\setup.exe" tells the computer to set it up as an exe file

N.B.; There is a space between "binPath=" and the file path. Don't miss it!

We got a "createService RESPONSE" response as shown in the image above.

I headed over to services application by searching for "services" and clicking on it from the result. I scrolled down to look for the service i just created.

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws12.png)

I double-clicked on it and clicked on "properties" and was shown the image below

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws13.png)

Clicking on the "Startup type" option, I could choose to start it uusing the following options: 
- Automatic (Delayed start) : it starts up after the system has completed its booting process.
- Automatic : It starts up when the computer is powered on. 
- Manual : I have to click on the service before it starts to run 
- Disable : Disable the service. 

![](https://github.com/xst0rmy/P-Set2-Creating-a-Windows-Service/blob/main/Images/ws14.png)

That is the comprehensive process I used in creating a windows service.

















