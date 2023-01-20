## Requirements for Group Project
[Read the instruction](https://github.com/STIW3054-A221/class-activity-soc/blob/main/GroupProject.md)

## Group Info:


| No | Full Name  | Matrix Number  | Phone Number  | Email  | Photo                                                               |
| ---- | --- | --- | --- | --- |---------------------------------------------------------------------| 
| 1 | Woon Zhun Ping (Leader) | 279144  | 017-4313479  | acping3@gmail.com  | <img height="120" src="/images/1.jpg" width="85" max-width="100%"/> |
| 2 | Ibtihal Hasmad  | 274790  | 011-28084876  | hal.hasmad@gmail.com  | <img height="95" src="/images/2.jpeg" width="75" max-width="100%"/> |
| 3 | Wong Zi Qing  | 279199  | 011-11463110  | 2020decwzq@gmail.com  | <img height="95" src="/images/3.jpg" width="75" max-width="100%"/>  |
| 4 | Yeap Shu Qi  | 280038  | 010-3171266  | shuqiyeap@gmail.com  | <img height="95" src="/images/4.jpg" width="75" max-width="100%"/>  |
| 5 | Anushiya A/P Irrulappen  | 280956  | 01116550117 | anushiya0117@gmail.com  | <img height="95" src="/images/5.jpeg" width="75" max-width="100%"/> |


## Title of your application
## Introduction

The group project’s main goal is to create a telegram bot, that aims to provide a convenient way for users to book and manage meeting rooms in University Utara Malaysia . The program stores all data in an SQLite database and automatically deletes data after a week. A daemon thread is also implemented to monitor the data every day. The telegram bot has been specifically designed for the purpose of booking rooms within the University Utara Malaysia (UUM), is directed towards two main user groups, namely school administrators and users.
The capacity to update existing rooms' unique identification numbers, descriptions, room types, and maximum capacities is given to school administrators in addition to the ability to build new rooms. The accommodation booking procedure is made simpler and more effective for frequent users thanks to this feature, which guarantees that the data provided by the bot is correct and current.
To further facilitate the booking process, the bot also offers a thorough list of rooms that are available and are accessible to users. Before confirming their bookings, users can also edit their personal information through the bot, as well as adjust the specifics of their reservations, like the type of rooms they're booking and the time and date of their reservation.This bot is designed to accommodate a wide range of room sizes, from small ones to large ones, meeting the various needs of the user community. The bot can also produce a list of every user's information who reserved a room.This feature allows for easy management and tracking of room bookings. This Telegram bot aims to improve the booking process and provide a more user-friendly experience for school administrators and users.


## Flow Diagram of the requirements

![flow diagram](https://user-images.githubusercontent.com/104670097/212495101-0b75d06d-e602-4782-a470-e42a6b3de159.jpg)

## User manual for installing your application on Microsoft Azure

The step-by-step guidelines to deploy a Java Telegram bot to Heroku:

1.First we have to sign up for a Microsoft Azure account.

2.Then we have to Install the Azure Functions Core Tools on our local machine by following the instructions on the page: https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local

3.Then in the terminal, navigate to the root directory of our Telegram bot application.

4.Create a new Azure Functions app by running the command "func init".

5.Create a new function for your Telegram bot by running the command "func new --language java --template "HTTP trigger""

6.Replace the generated code in the function with your Telegram bot code.

7.Create a new application setting for the Telegram bot token by running the command "func azure functionapp config appsettings set TELEGRAM_TOKEN=your_token_value"

8.Deploy the function to Azure by running the command "func azure functionapp publish your_function_app_name".

9.Use the Azure portal or Azure CLI to configure the function to run on an HTTP trigger.

10.In the Azure portal, under your function app, go to "Platform Features" and open "Application settings", set the "FUNCTIONS_WORKER_RUNTIME" to "java"

11.Add the dependencies to your pom.xml file, and make sure you have the required dependencies installed.

12.In the Azure portal, under your function app, go to "Platform Features" and open "Deployment Center" and select "Maven" and set the "Maven POM file path" to the path of your pom.xml file

13.Push the code to the Azure repository by running the command "git push azure main"

14.Use the Azure portal or Azure CLI to configure the function to run on an HTTP trigger.


## User manual/guideline for testing the system

When a user initiates a conversation with the bot by sending the command "/start", they will be greeted with a welcoming message. They will then be presented with two options to choose from: option 1 for registration, and option 2 for login. To proceed, the user simply has to reply to the bot with their desired choice.


**If the user chooses to reply with "1" for registration** <br>

1.First, they will be asked to enter their Identity card number.<br> 
2.After inputting their Identity card number, the user will be asked to insert their staff id.<br> 
3.They will then be prompted to enter their name.<br> 
4.Once their name is entered, the user will be asked to enter their phone number.<br> 
5.Finally, the user will be asked to enter their email address.<br> 


**If the user chooses to reply with "2" for login**<br> <br> 

1.The process for login is simpler compared to registration<br> 
2.The user will be prompted to enter their staff ID as the only required information for login<br> 
3.After entering their staff ID and submitting the information, the system will verify the user's credentials<br> 
4.If the information is accurate, the user will be granted access<br> 
5.The user can proceed with their intended task or request after successful login.<br> <br> 


Once the user has completed the registration or login process successfully, the chatbot will send a welcome message and present a few options for the user to choose from. These options include Apply as School Admin, Make a Booking, Display Booking, Cancel Booking, Edit Booking and Update Personal Info.

**If the user chooses the option to "Make a Booking"**<br> 

1.They will be prompted to complete a series of steps to finalize their booking<br> 
2.The user will first be asked to enter the purpose for their booking<br> 
3.After entering the purpose, the user will be presented with a list of rooms to choose from<br> 
4.Once the user has chosen a room, they will be prompted to select a date for the booking<br> 
5.After selecting the date, the user will have the option to choose an available session<br> 
6.Finally, the user will be asked to select a specific time for the booking.<br> <br> 


Once the user has completed the steps for making a booking, the system will display the user's booking details and prompt the user to confirm their choice of booking based on the provided details.

**If the user chooses the option to "Display Booking"**<br> 

1.The system will display again the room that the user has booked<br> 
2.This will provide the user with an opportunity to verify and review the details of their booking, such as the date, time, and purpose of the booking<br> 
3.This feature will enable the user to have a clear understanding of their booking<br> 
4.Ensure that they have made the correct booking<br> 
5.Also give them the chance to edit or cancel their booking if they find any errors or decide to change their plans.<br> 



**If the user chooses the option to "Edit Booking"**<br> 

1.The system will show the booking details again and then require the user to enter their booking ID to edit.<br> 
2.Users will have to enter their Booking ID.<br> 
3.The system will display four options to edit, Room, Date, Time, and Purpose.<br> 
4.User can choose any of the options, for example, if they choose Purpose.<br> 
5.The system will prompt the user to re-state their purpose of booking the room.<br> 
6.Then the system will re-display their booking for that Booking ID.<br> 


**If the user chooses the option to "Booking Cancel"**<br> 

1.The system will show the booking details again and then require the user to enter their booking ID to cancel.<br> 
2.Users will have to enter their Booking ID.<br> 
3.Once the user enters the booking ID, the system will delete the booking and send a message to confirm that the booking has been successfully deleted.<br> 

This feature will enable the user to cancel a booking that they no longer require or change plans. It will also give them the chance to verify and review the details of the booking that they want to cancel and ensure that it is the correct booking before they confirm the cancellation.


**If the user chooses the option to "Update Personal Info"**<br> 

1.The system will display four options for the user to choose from, which include ICNo, Name, StaffId, and Phone No.<br> 
2.The user can click on any of the options. For example, if the user clicks on Name.<br> 
3.The system will prompt the user to re-enter their name.<br> 

This feature will allow the user to update their personal information, such as their name, staff ID, IC number, or phone number. It will also give them the chance to verify and review their personal information and ensure that it is accurate before they confirm the changes. It will also give them the chance to update their contact information in case they have a new phone number or email address.


**If the user chooses the option to "Apply as School Admin"**<br> 

1.The system will require the user to insert their office number.<br> 
2.The user will then be prompted to choose the school they are from.<br> 
3.The user's email will be processed and approved later by the system or the relevant authorities.<br> 

This feature will allow the user to apply for the role of a school administrator by providing their office number and the school they are from. The system or the relevant authorities will then process the user's email for approval. This will enable the user to have access to the school administrator's portal and perform administrative tasks such as creating and managing bookings, managing users and other administrative tasks.


## Result/Output (Screenshot of the output)
## Use Case Diagram
<img src="/images/UseCaseDiagram.png"/>

## UML Class Diagram
<img src="/images/umlClassDiagram.png"/>

## Database Design
<img src="/images/DatabaseDesign.png"/>

## Youtube Presentation
## References (Not less than 20)

Vaghela, V. (2020, December 22). How to create a Telegram bot using java? - Viral Vaghela - Medium. Medium; Medium. https://vaghelaviral.medium.com/how-to-create-a-telegram-bot-using-java-5710bed16c0f

‌

rubenlagus. (2022, November 8). Getting Started · rubenlagus/TelegramBots Wiki. GitHub. https://github.com/rubenlagus/TelegramBots/wiki/Getting-Started

‌

sprkv5. (2014, November 14). JDBC SQLite PreparedStatement update and delete. Stack Overflow. https://stackoverflow.com/questions/26940149/jdbc-sqlite-preparedstatement-update-and-delete

‌

SQLite Java: Deleting Data. (2022, August 28). SQLite Tutorial. https://www.sqlitetutorial.net/sqlite-java/delete/

‌

cc. (2009, October 3). JDBC - prepareStatement - How should I use it? Stack Overflow. https://stackoverflow.com/questions/1515043/jdbc-preparestatement-how-should-i-use-it

‌

Sanjar Suvonov. (2020). Java Telegram Bot. Lesson 3: InlineKeyboardButton [YouTube Video]. In YouTube. https://www.youtube.com/watch?v=jUiHPVR-IYg&list=PLAU9HciqfTIn1UuSYKqo0-UKqvAltacoG&index=4&ab_channel=SanjarSuvonov

‌

Fizz. (2020). Configuration JDBC drive with intlij IDEA || No suitable driver found for jdbc [YouTube Video]. In YouTube. https://www.youtube.com/watch?v=duHgwpYLKZE&ab_channel=Fizz

‌

sairumi. (2022). STIW3054 Assignment 2 - 277838 (Telegram Bot) [YouTube Video]. In YouTube. https://www.youtube.com/watch?v=_EK5Xd8rkgM&ab_channel=sairumi

‌

Azamat Ordabekov. (2021). How to create Telegram Bot in Java [YouTube Video]. In YouTube. https://www.youtube.com/watch?v=XjOnp8TVNSQ&t=146s&ab_channel=AzamatOrdabekov

‌

Lesson 1. Simple echo bot - Java Telegram Bot Tutorial. (2022). Gitbook.io. https://monsterdeveloper.gitbook.io/java-telegram-bot-tutorial/chapter1


Choo, A. (2019, August 14). Build a Serverless Telegram Bot with Firebase Functions. Medium; Medium. https://medium.com/@aaroncql/build-a-serverless-telegram-bot-with-firebase-functions-267d251e4e46

‌

Akhromieiev, R. (2021, January 14). Building a Telegram Bot With Firebase Cloud Functions and Telegraf.js. Akhromieiev.com. https://akhromieiev.com/building-telegram-bot-with-firebase-cloud-functions-and-telegrafjs/

‌

Comparing Telegram Bot Hosting Providers - Code Capsules. (2023). Codecapsules.io. https://codecapsules.io/docs/comparisons/comparing-telegram-bot-hosting-providers/

‌

Deploying with Git | Heroku Dev Center. (2022). Heroku.com. https://devcenter.heroku.com/articles/git

‌

Isakovinc. (2022, June 22). Deploy Java Telegram Bot on Heroku Server - Isakovinc - Medium. Medium; Medium. https://medium.com/@learntodevelop2020/deploy-java-telegram-bot-on-heroku-server-42bfcfc311d3

‌

‌
## JavaDoc
