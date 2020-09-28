# Ayna

## Abstract
This project aims to combine some of the currently emerging trends in Computer Science; [Internet of Things](https://en.wikipedia.org/wiki/Internet_of_things) (IoT) and [Speech Recognition](https://en.wikipedia.org/wiki/Speech_recognition), in order to create a higher level of interactivity. This heightened interactivity enables new experiences in a number of applications that make use of Speech Recognition. In this project, we focus on the creating a Smart Mirror in which user can interact with the mirror directly with the voice command.  
IoT is the interconnection of hardware and software through the medium of internet. IoT has helped to better the technology and lives of people. Speech Recognition refers to the process of understanding the natural voice of a person and generating a text out of it. Speech Recognition is one of the simplest method that can be explored interactively using a [personal computer](https://en.wikipedia.org/wiki/Personal_computer) or any other [smart devices](https://en.wikipedia.org/wiki/Smart_device). Using these two, we can enable a computer to understand user voice and extract meaningful information from them. This technology has made many of the current trends like [Siri](https://en.wikipedia.org/wiki/Siri), [Home Automation](https://en.wikipedia.org/wiki/Home_automation), etc. possible. The use of Speech Recognition in this project facilitates users to interact with the smart mirror by their voice rather than using their bare hands, without the need for any external hardware like keyboard and mouse.  
Instead of expensive multiple smart devices like the [Tablet](https://en.wikipedia.org/wiki/Tablet_computer), [iPad](https://en.wikipedia.org/wiki/ipad), [Desktop](https://en.wikipedia.org/wiki/Desktop_computer), etc. this project makes use of a [Raspberry PI](https://en.wikipedia.org/wiki/Raspberry_Pi) mounted on a [monitor](https://en.wikipedia.org/wiki/Computer_monitor) (LCD/LED) and a USB Mic to create a one device for your assistance and one place for all your internet needs.

Keywords: [Raspberry Pi](https://en.wikipedia.org/wiki/Raspberry_Pi), [IOT](https://en.wikipedia.org/wiki/Internet_of_things), [Voice Processing](https://en.wikipedia.org/wiki/Speech_processing), [Bot](https://en.wikipedia.org/wiki/Internet_bot), [Smart Mirror](https://en.wikipedia.org/wiki/Virtual_mirror)

## 1. INTRODUCTION

### 1.1 Background
Ayna is a web application which will be a hub for all your daily online needs. It is a personal assistance bot which takes command from your voice and keeps you updated on your daily activities. You can create an account and log in our system through which you can customize the display of the modules.  
This system is your personal assistant which will be one place for all of your daily app that can be controlled via voice commands.  

It can have two modes:   

**Default**  
This mode will be viewed if the no user have been logged into the system, it displays the modules which are predefined in our system.  

**User Defined**  
This mode will be viewed when the user is logged into the system and will display the modules according to the user customization.  

### 1.2 Problem Statement
The field of AI and IOT is gaining momentum today but this field still lacks interaction techniques that feel natural and are affordable. Not only is the hardware expensive but there is not adequate amount of applications that can fully utilize these hardware and technologies. APIs and documentations related to AI bots is very limited. AI is being used today in many domains, one of which is the field of learning.
Current population have a very busy schedule and have many apps and devices to use internet from. Over 1 million selfies are taken every day with 30% of photos taken by people between the ages of 18 and 24 being a selfie. In total, 28% of time spent online is on social media [1]. According to a TODAY/AOL survey, women spend an average of 6.4 hours/week while men spend 4.5 hours/week working on their appearances.  
The Smart Mirror is a system that combines these tasks in an efficient and enjoyable way to provide time savings for the user.

### 1.3 Objectives
The objectives that this application intends to achieve are:
- To create a smooth interaction using natural voice command to the mirror.
- o make one stop for all the apps and your online inquiry we created ayna.

### 1.4 Scope and Limitations

#### 1.4.1 Scope
The system can be given command through voice. It can also integrate several applications into a common platform and will keep you updated on the daily activities. User can login to the dashboard to expand the module and which is a remote controlled app which can be accessed through phone.

#### 1.4.2 Limitation
Currently our system can’t do activities like learn from it and act accordingly. Users need to use mobile devices to login to the system because users cannot login directly from the mirror without connecting an external keyboard.

#### 1.5 System Environment
For our system to run, there are some basic criteria that needs to be satisfied first.
- Steady internet for the modules and speech recognition.
- Quiet surrounding or less noisy environment for speech recognition to work effectively.
- Browser should be allowed to access the microphone.
- Google Chrome or Chromium browser should be used to operate the system.

## 2. REQUIREMENT ANALYSIS AND FEASIBILITY ANALYSIS

### 2.1 Study of Existing System

### 2.2 Data Collection Methods and Sources
It is very important to collect data from lots of sources in order to make a project possible. Many researchers have documented their work on smart mirror in various journals. These papers were studied in order to gain knowledge on the techniques currently being used for these purposes as well as to gain a clear understanding of the performance complexity of the project. The different algorithms and techniques discussed in the papers were compared and studied in order to decide the best approach. The internet was searched for information regarding software applications, voice APIs and libraries which could help in implementing the voice command system required for voice analysis and processing. The website that we have visited for data collection are listed on Reference.

### 2.3 Software Requirement Specifications

#### 2.3.1 Functional Requirement
The system allows user to authenticate themselves and customize their mirror accordingly and add or remove modules. It also allows them to feed data from the API onto their mirror.  Ayna allows user to do perform limited query through speech recognition system.    
Some major functional requirements are:  

##### 2.3.1.1 Authorization
Here authorization is necessary in our system for the privacy of the user’s profile. So no other person except the user can alter the mirror with their fake credentials. Authorization starts at first when the user inputs on the user login form and the required value are then compared to our database. So if the user is genuine, the person will get access to the dashboard of our system. Or if is a new user, the person can simply go to the register page and fill in the required information and can login to the system.

##### 2.3.1.2 Data Parser
Data parser is one of the major requirement in our system since all our modules rely on fetching data from many different sources concurrently. Either it be from our own ayna API or from JSON feed from the internet or the system time, we need to parse data from various sources and then present it on the screen. For this purpose we will be using axiom for most of our data parsing activity for modules like news, weather and greetings. It is very affective and faster while executing the data parsing task for our modules.

##### 2.3.1.3 Speech Recognition
Speech Recognition is the core part of our system since it is responsible for interaction with the mirror and manipulating the modules. For Speech Recognition we will be using an online API called annyang. It helps us to identify the instruction or command given by the user and turn them into action resulting the change in the current state of mirror.

**Speech Recognition Process**  
<small>*Figure 1: Speech Recognition Process*</small>

**Component of Speech Recognition System**  

**Audio Input**  
With the help of microphone audio is input to the system, the sound card produces the equivalent representation of the received audio [2].  

**Digitization**  
The process of converting the analog signal into a digital form is known as digitization [2], it involves the both sampling and quantization processes.  

**Acoustic Model**  
An acoustic model is created by taking audio recordings of speech, and their text transcriptions, and using software to create statistical representations of the sounds that make up each word. It is used by a speech recognition engine to recognize speech [2].  

**Language Model**  
Language modeling is used in many natural language processing applications such as speech recognition tries to capture the properties of a language and to predict the next word in the speech sequence [2].  

**Speech Engine**  
The job of speech recognition engine is to convert the input audio into text [3]; to accomplish this it uses all sorts of data, software algorithms and statistics. Its first operation is digitization as discussed earlier, that is to convert it into a suitable format for further processing. Once audio signal is in proper format it then searches the best match for it. It does this by considering the words it knows, once the signal is recognized it returns its corresponding text string.

#### 2.3.2 Non-Functional Requirement
Some of our key non-functional requirement for our smart mirror will be:  

##### 2.3.2.1 Performance
The system works smoothly without any kind of bug interrupting it. Response time of the modules were very fast and initial load time for entire system from start was about 30 seconds but poor internet can affect the performance of the system.

##### 2.3.2.2 Scalability
Our system ayna is highly scalable. New features can be added or deleted from the system. Also in future user can add modules created by him into the system. Since it is being hosted online, ayna’s hardware requirement can be scaled up or scaled down according to need.

##### 2.3.2.3 Usability
Our system is very easy to use in both ways via voice control or other devices. The commands are very simple and so is the UI.

#### 2.3.2.4 Security
Our system is JWToken based system which is secure. Without the token user cannot access or cannot request any services. When we login in our page, we will get the token and with that token, we can do any request we want to the server just by giving it our token.  
A JWToken is self-contained, so when we create one, it will have all the necessary pieces needed inside of it. It is divided into three parts Header, Payload and Signature. If you don't have the token, you can't do anything. We store these token in session storage or local storage (depending if you want to force a login the next time the user opens the browser or not).

### 2.4 Hardware Requirement Specifications
The minimum hardware requirements to run the project are as follows:  

#### 2.4.1 For Normal Smart Mirror (without touch)
- Raspberry pi 3B
- LED Monitor
- 2 way mirror (reflecting mirror)
- Wooden mirror frame
- Speaker
- USB web camera with Mic

#### 2.4.2 With Touch facility
All the hardware are same but we need LED Monitor with touch function to use this touch facility in Smart Mirror.

### 2.5 Feasibility Analysis
Our project team have carried out the following feasibilities studies:

#### 2.5.1 Economical feasibility
The project aims to create a cost-effective solution for interaction. The current tools and technology in the market like the, Microsoft Smart mirror or the Apple Smart mirror and the Samsung Smart mirror costs thousands of dollars. This project utilizes a Raspberry pi and a LED monitor which costs around $120 combined. The system utilizes cost effective hardware while providing maximum functionality.

#### 2.5.2 Technical feasibility
The technical feasibility study assesses the details of how the project delivers a product or service. This study defines if a project can be feasible in terms of technical requirements or not. After a detailed feasibility study, following conclusions were obtained:
- There exists libraries for Voice processing which can be easily implemented.
- Upgrading of the project to add new API features is easy.
- This system easily adapts the latest technology.  

#### 2.5.3 Operational feasibility
Any project that can be implemented in real world remains beneficial. If it cannot be implemented, it exists only in theoretical approach. This project is feasible operationally. The interaction is done using voice commands. This will require user to learn some few commands but most people already use voice commands like- Siri, Cortana etc. They can also interact with the ayna remotely using mobile devices or any other computer by being on same network.

### 2.6 Structure System Requirement 

#### 2.6.1 Use Case Diagram
A use case diagram is a simple written description of how users perform tasks and interact with a system. It shows the system from a user’s point of view and the system’s behavior as it responds to a request [4]. It is basically a type of textual requirements specification that captures how a user will interact with a system to achieve a specific goal. The use case diagram usually contains an actor, basic flow, post conditions and processes [5]. The Use Case diagram of the system is shown in figure 2.  
*Figure 2: Use Case Diagram*  

#### 2.6.2 Activity Diagram
An activity diagram visually presents a series of actions or flow of control in a system similar to a flowchart or a data flow diagram. Activity diagrams are often used in business process modeling [6]. The activity diagram of the system is shown in figure 3.  
*Figure 3: Activity Diagram*  

## 3. SYSTEM DESIGN  

### 3.1 System Architecture  
> *Figure 4: System Architecture*  

#### 3.1.1 User Interface
User interface manages the interaction with the user. It takes data from the internet for the modules and displays to the user. User Interface can be changed and modified according to user needs if the user is logged in the system. That’s why it has two views:  
- Default View
- User Defined View  

##### 3.1.1.1 Default View  
This is the view which will be first loaded on the screen of ayna when it is started. If it is opened for the first time or when the user logs out of the system, this view is automatically loaded with the predefined default modules.  

##### 3.1.1.2 User Defined View  
This is the customized view preferred by the user to display on the screen of ayna. It is loaded whenever the user is logged in to the system and it changes back to the default view when user logs out. You can change the view through the user profile.  

#### 3.1.2 Default Modules  
These are the predefined modules by the system. They include modules such as clock, weather, news and greetings. They request for data from the API on the internet like annyang API and news API. They are automatically displayed on the user interface if no user is logged in.  

#### 3.1.3 User Authentication  
This process checks weather the user trying to log in the system is genuine or not. It checks data like user id and user password to verify them. These data for authentication are provided by the database.  

#### 3.1.4 User Defined Modules  
Here the system will deploy the modules that have been defined by the user. After logging in the system, the personalized view of module is displayed on the user interface. It can have more extra modules than the default modules or less than default modules. 

#### 3.1.5 Customize Modules  
After logging in, you can enter the user dashboard. In user dash board you can customize the modules in following ways. Some of the changes you can make on the modules are:
- Add/remove module  
- Change position 
- Module configuration  

You can customize your module through two ways
- Voice Input  
- Other Devices  

##### 3.1.5.1 Voice Input  
You can customize your module using voice commands by giving certain commands to the ayna.  

For example: ``'position clock right'``.  
> Input: ``position clock right``  

> Command Recognized: ``position <module_name> <position>``  

Here, ``<module_name>`` and ``<position>`` are variable when user command ``"position clock right"``, then **Annyang** will detect the variables value and does the further processing. In this case, if the user is logged in and the clock is visible in the screen either in left or center position then the clock will move to the right position otherwise it will display the error in the screen accordingly.  

##### 3.1.5.2 Other Devices
You can log into the user profile from other device and change the modules.  

#### 3.1.6 API  
API is a set of functions and procedures that allows the creation of applications which access the features or data of an application or other services. We will be using following API’s for our modules.  
- Ayna API (Designed for Ayna)
- API (Internet third-party packages)

##### 3.1.6.1 Ayna API  
Ayna API is used to route between the modules, for user authentication and module customization. Routes are switched between modules when either the user is logged into the system or when no one is logged in. It gives path for the modules to display it on the user interface.   
Ayna API checks whether the user is genuine or not by cross checking the user credentials from the input with our data in the database.  

It also allows user to change the modules as required. Some of the changes user can make to the modules through dashboard are: hide/display modules, change location of modules and add modules.  

##### 3.1.6.2 API (Internet)
These are the data provided by the API available on the internet for some of our modules to function. They take data from news API and other API. These data include news, weather, speech recognition, etc.  

#### 3.1.7 MongoDB
**MongoDB** as our database which stores data in flexible, JSON-like documents, fields can vary from documents to document and data structure can be changed over time. It will store information about user like user name, email id, user id and password and information about modules like module id, position, surface area, visible, default modules, category.

### 3.2 Sequence Diagram
> *Figure 5: Sequence Diagram of the System*

### 3.3 ER Diagram 
> *Figure 6:  ER Diagram of the System*

### 3.4 Class Diagram
> *Figure 7: Class Diagram of the System*

### 3.5 Modules

#### 3.5.1 User Login
It is the form through which user can log into the ayna for personalizing their UI and other customization.

#### 3.5.2 User Profile
It displays the dashboard of user when logged in, where user can customize the modules.

#### 3.5.3 Module Profile
It displays the information regarding the selected module.

#### 3.5.4 User Authentication
User authentication is done through JWToken. Without the token user cannot access or cannot request any services. When user logs in our system, user will get the token and with that token, user can do any request they want to the server by just giving it the token.

#### 3.5.5 Display Modules
Here it shows what modules to display on the screen of ayna. It can be the default modules or the user customized modules. The modules which are currently available to use are: clock, greeting, news, quotes, music player and wiki search.

#### 3.5.6 Customization 
Here user can customize the modules like install the module or not, hide/display the module and change the position of modules. It is done in the user profile.

#### 3.5.7 Register
New user can get into the system through the form provided by the register module. Basic information are needed to register.

## 4. SYSTEM DEVELOPMENT AND TESTING

### 4.1 System Development Model
We used Agile Model (AM) as a software development model. Agile SDLC model is a combination of iterative and incremental process models with focus on process adaptability and customer satisfaction by rapid delivery of working software product. Agile Methods break the product into small incremental builds. These builds are provided in iterations, each iteration typically lasts from about one to three weeks.  

Every iteration involves cross functional teams working simultaneously on various areas like:
- Planning
- Requirement Analysis
- Design
- Coding
- Unit Testing
- Acceptance Testing  

By using agile model, we broke down our project into numbers of modules and started working on those modules iteratively. On each iteration the compatibility and flexibility of modules were checked and improved. Each modules were passed through requirements, design, implementation and testing phases. The process continues till the completed system is achieved. Using this model made our software development process easier and efficient. After the system was developed it was then further adjusted according to the hardware specification, so it could run on the hardware efficiently.

### 4.2 Tool Used
#### 4.2.1 HTML
HTML (Hypertext Markup Language) is used to create webpage and properly structuring the webpage contents.

#### 4.2.2 CSS
CSS (Cascading style sheets) are used to format the layout of Web pages and properly style the contents of the HTML.

#### 4.2.3 Axios
We have used axios for xmlhttp request and response. It works efficiently with react and is fast. It is used to parse data from different sources to our smart mirror.

#### 4.2.4 React JS
React is front end library developed by Facebook. React makes it painless 	to create interactive UIs so we use this in our project as a main Front end development kit. It is used for designing different modules and to develop a module management interface. Main core script for displaying dynamic modules either it is Ayna default modules or User defined modules is written in React JS.  

Introducing React’s Component-Based feature, it is used to build encapsulated components that manage their own state, then compose them to make complex UIs. We have developed different components for this system such as, home screen is one component we call it MainSurface in project and inside that component we have to load SurfaceArea component. There are five surface areas which we have defined and they all need to be render at first in MainSurface because Modules (Clock, Greetings, News Feed, Quotes, etc.) are going to be rendered in SurfaceArea according to data store in database for every modules. We have defined five surface area as shown in the figure below:  

> *Figure 8: Illustrating Ayna Components*

In above figure, there are five surface area but we have designed only one SurfaceArea component that dynamically rendered required modules in five surface areas according to user database or default ayna database. We let the user to define their modules as their requirement. For accurate position of modules, we have defined three positions (Left, Center and Right). User need to log in to set position and can give voice command as well from home screen or from dashboard section user can define the position for their modules.
In Dashboard section after log in user can install the modules from ayna modules and also can remove by uninstalling it or if they don’t want to display in their home screen user can make their module offline from dashboard or simply from home screen they can give a voice command to make module offline.

#### 4.2.5 Express
Express is a fast, assertive, essential and moderate web framework of Node.js. Express is a layer built on the top of the Node.js that helps manage a server and routes. We use this framework for making REST API for the project. API provide user and module routes and services to the client from where client can perform CRUD operation. It provides a robust set of features to develop web application. Some of the core features are:
- It can be used to design single-page, multi-page and hybrid web applications.
- It allows to setup middleware's to respond to HTTP Requests.
- It allows to dynamically render HTML Pages based on passing arguments to templates.
- It defines a routing table which is used to perform different actions based on HTTP method and URL.  

#### 4.2.6 Node JS
Node JS is an open source, cross-platform runtime environment for developing server-side and networking applications. Node.js applications are written in JavaScript, and can be run within the Node.js runtime on OS X, Microsoft Windows, and Linux.  

We use Node JS because it provides a rich library of various JavaScript modules which simplifies the development of web applications using Node.js to a great extent. Node JS is asynchronous in nature and uses single threaded model with event looping.

#### 4.2.7 MongoDB
**MongoDB** is an open source that uses a document-oriented data model. Choosing MongoDB would be one of the easier option instead of tables and rows as in relational databases, it is built on an architecture of collection and documents. Documents comprise sets of key-value pairs and are the basic unit of data in MongoDB. It is also easy to use and implement. It is faster than relational database and we want our data in JSON format so that MongoDB is the best choice for us and it perform more accurately when there are many concurrent processes.

#### 4.2.8 Annyang
Annyang is a tiny Javascript library that lets your visitors control your site with voice commands. In this project user can interact with the mirror using their voice command and they can command the mirror by which mirror will perform some action to make some changes into the mirror. User can change the position of modules, can navigate from home screen to dashboard, and can interact with some queries with voice commands.

### 4.3 Testing Methods
System has been tested and errors have been identified by using unit testing, system testing and integrated testing approaches.

#### 4.3.1 Functional Testing
##### 4.3.1.1 Unit Testing
Each unit of the system has been tested individually to verify that they function properly.  

**Test Case Id: *1***    
**Test Case description: *Proper functioning of modules***
- Show clock
- Show news feed
- Show greetings
- Show quotes
- Receive voice input and display text

> *Table 2: Test Case: Proper Functioning of Modules*

##### 4.3.1.2 Integration Testing
After completing the unit testing, the modules are integrated for integration testing. So after combining the modules tests like user login, register and default/user-defined view were tested.

**Test Case Id: *2***  
**Test Case description: *Login/Register Page***

> *Table 3: Test Case: Login/Register Page*

**Test Case Id: *3***  
**Test Case description: *Module display (default and user defined)***

> *Table 4: Test Case: Module display (default and user defined)*

##### 4.3.1.3 System Testing
Finally the entire system is put together and system testing is done. Following tests were conducted after putting together our software and hardware.  

**Test Case Id: *4***    
**Test Case description: *Manipulating modules (through voice or remotely)***  

> *Table 5: Test Case: Manipulating modules (through voice or remotely)*


#### 4.3.2 Non Functional Testing
##### 4.3.2.1 Load Testing

**Test Case Id: *5***  
**Test Case description: *Load testing***  

> *Table 6: Test Case: Load testing*

## 5. IMPLEMENTATION AND MAINTENANCE

### 5.1 System Implementation

#### 5.1.1 Hardware Implementation
The core of the Ayna consists of Raspberry-pi Model 3 B. Figure 9 shows the integration of electronic components into the Raspberry-pi. The electronic components that we have used are:
- Raspberry-pi Model 3 B
- Power supply for Raspberry Pi
- LED Monitor
- Microphone
- VGA to HDMI converter

> *Figure 9: Electronic Component with Raspberry Pi*

#### 5.1.2 Software Implementation
The software that we developed and used in this work concerns the Electron based web application as well as the main server. As operating system we choose Raspbian which is based upon the Debian Wheezy Linux operating system and has been optimized for use with Raspberry Pi.

#### 5.1.3 Web Application
For the development of the web application, as regards the client’s part, HTML and React JS were used where JSX makes React a lot more elegant. JSX is a preprocessor steps that adds XML syntax to JavaScript. On the server side, we have the JavaScript REST API build on Express framework using Node JS, which request and response with appropriate data in JSON like format that are stored in the Mongo DB database.  

For the implementation of the Web application we have used Visual Studio Code. We have published a repository on GitHub for collaboration.  

The Web application has 7 main interfaces:  
- **Ayna** ``(Figure 10)``  
The Ayna is the main interface which contains a script to load default modules or user defined modules in their respective surface area.
> *Figure 10: Ayna Interface*

- **Login Form** ``(Figure 11)``  
The Login interface is a simple JavaScript which in turn is connected to a Mongo DB database. Upon successful entry of a user, comes up the Dashboard interface ``(Figure 13)``.
> *Figure 11: Login Interface*

- **Register Form** ``(Figure 12)``
The Register interface is a simple form which lets user to register in ayna using their username, email and password they provide, it connects to Mongo DB database to store the user data after registration and then comes up the Login interface to login.  
> *Figure 12: Register Interface*

- **Dashboard Interface** ``(Figure 13)``  
The Dashboard interface is for viewing the stats of ayna i.e., It shows number of default modules, user modules and total registered users. User most logged in to route here.  
> *Figure 13: Dashboard Interface*

- **Modules Interface** ``(Figure 14)``  
In Modules interface, user need to sign in first and can install their desired modules from default modules so that they can view their module in Ayna. User also can uninstall the user modules or they can set visible property of the user modules by visiting module profile interface ``(Figure 16)``.
> *Figure 14: Modules Interface*

- **Profile Interface** ``(Figure 15)``  
In Profile interface, user can view their profile details and can change the details if they required.
> *Figure 15: Profile Interface*

- **Module Profile** ``(Figure 16)``  
In Module Profile interface, there we can view module profile and user can install or uninstall module.
> *Figure 16: Module Profile Interface*

### 5.2 Maintenance

#### 5.2.1 Adaptive Maintenance
Here the modules are checked and maintained regularly. According to the need of user, the modules can be added or modified.

#### 5.2.2 Corrective Maintenance
The fully tested version of application is deployed. If users find issues and complains about issues the proper corrective maintenance will be done as soon as possible.
 
## 6. CONCLUSION AND FUTURE PLANS

### 6.1 Conclusion
This project aims to provide an interactive and informative environment in a mirror which is fully voice controlled. System can run multiple modules in a single screen. Our system is available to the wider public because it is affordable as compared to other models of smart mirror.

### 6.2 Future Plans
We are going to add more features for both registered and unregistered users. This app will detect the face emotions and will use machine learning to interact with the user. Currently it only supports English language but in further development of this system we may integrate Nepali language.

## References
[1] 	E. Z. M. F. T. L. Suzanne Reed, "Smart Mirror," 2016.  

[2] 	J. Kirriemuir, "Speech recognition technologies," 30 March 2003. [Online].   

[3] 	L. R. &. B. Juang, "Fundamentals of Speech Recognition," 1993.   

[4] 	"Use Cases," [Online]. Available: https://www.usability.gov/how-to-and-tools/methods/use-cases.html.  <br />

[5] 	Laura Brandenburg, "How to Write a Use Case," [Online]. Available: http://www.bridging-the-gap.com/what-is-a-use-case/. [Accessed 26 08 2017].  

[6] 	"Activity Diagram," [Online]. Available: https://www.smartdraw.com/activity-diagram/. [Accessed 26 08 2017].  

[7] 	Techtarget, "HTML," September 2005. [Online]. Available: http://searchmicroservices.techtarget.com/definition/HTML-Hypertext-Markup-Language.  

[8] 	2017. [Online]. Available: https://techterms.com/definition/css.  

[9] 	S. Technologies, 12 March 2013. [Online]. Available: http://www.seguetech.com/ajax-technology/.  

[10] 	April 2005. [Online]. Available: http://www.theserverside.com/definition/Java-Server-Page-JSP.  

[11] 	2010. [Online]. Available: http://docs.oracle.com/javaee/5/tutorial/doc/bnafe.html.  

[12] 	September 2013. [Online]. Available: http://searchoracle.techtarget.com/definition/MySQL.  

[13] 	A. P. A. S. Siksha Gupta, "A STUDY ON SPEECH RECOGNITION SYSTEM: A LITERATURE REVIEW," International Journal of Science, Engineering and Technology Research, 2014.   

[14] 	hackerhouse, "smart-mirror," [Online]. Available: https://github.com/HackerHouseYT/Smart-Mirror.  

[15] 	"SDLC Agile Model," [Online]. Available: https://www.tutorialspoint.com/sdlc/sdlc_agile_model.htm.  

[16] 	S. W. Ambler, "An Introduction to Agile Model," [Online]. Available: http://www.agilemodeling.com/essays/introductionToAM.htm.  
