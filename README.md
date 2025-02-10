# Bouquet-Builder
Bouquet Builder is a user-friendly app designed for florists who want to craft beautiful floral arrangements effortlessly. Whether you're designing a bouquet for a special occasion or using standard recipes, this app simplifies the process with intuitive tools and customization options.

### Problem and Background

The company's workers brought the initial problem to my attention. Their old method of pricing bouquets involved manually writing down flower names and quantities on paper and then using a calculator app on their phone to determine labor percentages. This process was highly inefficient, time-consuming, mentally exhausting, and often led to inaccurate pricing. Since they had to do this almost daily when making arrangements, it gradually took the joy out of crafting beautiful floral pieces.

Now, the workers can’t stop talking about how fun and addictive it is to use the app. The convenience of the app compared to doing mental math or using pen and paper is incredible. Needless to say, gone are the days of miscalculated arrangements and outdated flower prices now, pricing is effortless and accurate. Bouquet Builder has truly transformed the way this business operates, eliminating stress and making floral design enjoyable again.


## Challenges
- The first and biggest challenge in developing this app was identifying the exact problem and figuring out how to build a solution. While this might sound simple, it required me to gain a deep understanding of how bouquets are made and priced, especially on something I had no prior knowledge of. I had to learn the entire process from scratch to ensure the app effectively addressed the issue.
- The next challenge involved people skills. I had to negotiate the app’s price while also estimating the number of work hours required to implement all the necessary features. Determining the full list of requirements was its own challenge, and translating the client’s vision into functional code proved to be far more complex than expected.
- Finally, publishing the app to the app stores was another hurdle. While I had experience deploying applications to cloud providers, mobile apps were a completely different challenge. I wouldn’t say it was harder, just unfamiliar, which added an element of risk.


## Risks
### Handling Images in the App
- Before developing this app, I had no prior experience managing images in a Flutter application. I needed to find an efficient way to store images while minimizing storage usage to keep the app lightweight and scalable.
  
### Publishing the App

- I had never officially published an app to an app store before. One of the biggest challenges was figuring out how to set up internal testing so that the client could test the app during its early stages without exposing it to a large number of unexpected users. Navigating the publishing process was a learning experience, but it was crucial for ensuring a smooth rollout.

### Hardware and Software Technologies
Here are all of the technologies used within the development of the application along with their versions so that if someone is brought onto the development team they will know what they need to help in development.


- Microsoft Windows Version 10.0.19045.3693
- Android Studio Version  2022.3
- Android SDK version 34.0.0
- Google Pixel 3 34GB (simulator)
- Google Pixel C 34GB (simulator)
- MacOS 13.5
- Xcode 15.0
- iPhone 15 (simulator)
- iPhone 14 (physical)
- iPhone 8+ (physical)
- Flutter Version 3.5.0
- Firebase
- Visual Studio Community Version 2022 17.3.6
- VS Code Version 1.84.2

### Why Flutter, Dart, and Firebase?
Putting on my developer hat, Dart is the main programming language that I wanted to use for my app and Flutter is an amazing framework for it.
I chose Firebase as my database mainly because of its compatibility with Flutter apps as well as easy storage of images and Google authentication and the fact that they are Google technologies which means they will have a lot of support and documentation to learn from.


## Physical Solution Design

<img width="734" alt="image" src="https://github.com/AceLake/Assemblage-Flutter/assets/96988100/e9422bfe-7091-4182-b059-7360ffc8db3d">


### Description

#### Physical Solution Design
The Physical Solution Design provides a representation of the actual physical development environment for the app. The code is created using Visual Studio Code (VS Code) on the host device. This setup ensures a robust testing and development environment, allowing for efficient cross-platform development and thorough testing on both simulated and physical devices.

#### Android testing
Currently, Android testing is conducted on a Windows PC, utilizing the Android Studio for running the Android simulator. VS Code seamlessly detects the running simulator and facilitates deployment onto the simulated Android environment.

#### IOS testing
Similarly, iOS testing is performed on a MacBook, employing the iPhone simulator through Xcode. VS Code efficiently recognizes the simulated iOS device, enabling deployment during the development process.

#### Physical testing
For wired connections, Xcode builds the application and deploys it onto a physically connected iPhone, streamlining the testing process on real iOS devices.

## Detailed Technical Design
This section will hold all of the diagrams to help the development team understand what is needed to develop the application to industry standards. This is conveyed through the use of diagrams and descriptions surrounding the given diagrams to help with interpretation.
 
### General Technical Approach
The structure of Bouquet Builder should be built for adaptability for different types of data as well as an overall structure to create a multi-platform experience. Also, Bouquet Builder should be built with ease of use in mind. The application should be set up to store massive amounts of data

### Key Technical Design Decisions:
Bouquet Builder will use the Flutter framework with Dart as its primary programming language. The database is Firebase which is a Non-relational database. 

The reason why I wanted to use Flutter for the framework for my application was to support cross-platform to give more users the ability to find and use the app. Flutter's main hook is that it allows for the app to be used with a variety of different platforms.

Dart was chosen for its object-oriented nature which allows the app to be more scalable.

Firebase was chosen because of its NoSQL structure. Having NoSQL within the app will allow it to be able to store massive amounts of data while also being adaptable to store different types of data.

### Document Structure Diagram 
<img width="595" alt="image" src="https://github.com/AceLake/Assemblage-Flutter/assets/96988100/8b76ca12-4b43-43bc-9cce-2596910c8034">

Here is how each document relates to each other in my Firebase database. Firebase is a NoSQL Database so they are not documented the same but I used a UML class diagram to create a NoSQL Entity Relational diagram. Each User holds a list of Groups they are a part of and also has a list of messages they have sent as a list of message objects. Each group has a list of message objects that represent all of the messages in that group.



## Sitemap
![Assemblage Site Map drawio (1)](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/6cc9b906-e596-4f17-ac66-e2fa8cd68c99)

### Description

- Green: all of the create operations in the application.
- Purple: all of the read operations in the application.
- Orange: all of the update operations in the application.
- Red: all of the delete operations in the application.
- Blue: all of the non-CRUD features. Usually, it’s a static page or an action not connected to the database.

When the application is initially launched, users will be seamlessly directed to the login page. If they are new to the platform, they can easily navigate to the registration page directly from the login page. Once users successfully log in or complete the registration process, they will be immediately redirected to the home page.

Throughout the application, excluding the login and registration pages, users have 5 common pages they can navigate to. At the bottom of the screen, a navigational bar provides access to 4 core pages of the app, ensuring easy and convenient navigation from any point within the application. Additionally, an app bar positioned at the top of the page allows users to access their profile information effortlessly.

## Widget layout design
### Description 
Purple: Stateless Widget 
<br>
Red: List Widget 
<br>
Green: List Item Widget
<br>

<details>
  <summary>App Bar Widget</summary>
  <p>
   
![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/5a49d9e3-d49f-4060-9c27-954cf515ccfd)
- This is the default App bar view but it has many states 
- Pulls out a drawer that logs the user out
- Pulls out a drawer that navigates to the details page or leaves the group.
  </p>
</details>
<details>
  <summary>NavBar</summary>
  <p>
   
![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/449ead43-3670-4eed-b100-f005b2471f06)

- Holds Page navigation to different pages in the app. Each Icon is clickable.
- Home Page navigation as the first icon to the left
- Find Group navigation as the second icon to the left
- Group Creation navigation as the 3rd icon to the left
- Chats as the last icon furthest to the right
- Each item in the nav bar displays the name when clicked on, so the search tab isn't the only one like that
  </p>
</details>
<details>
  <summary>Login</summary>
  <p>
   
   #### GIF

   ![Loggingin-ezgif com-video-to-gif-converter](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/3f2af8b3-9b08-49db-a1f5-62f72c8da03a)
   
   #### Component Design
   
   ![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/32c97ef9-9e15-455d-8b46-b5ab97d5e452)


#### Login Body
- This widget is a stateless widget 
- It acts as an entire page for logging in a user
#### Username Input Text Feild
- This widget uses a text input widget that will take in text from the user
- For this specific widget, it will take in the text that will be compared to a username field in the user document in Firebase
#### PasswordInput Text Feild
- This widget uses an input widget that will take in text from the user
- For this specific widget, it will take in the text that will be compared to a username field in the user's document in Firebase
#### Submit Button
- This is a button widget
- This button initializes the login and checks if the user with that username and password exists.
#### Go to Register
- This is a link widget
- It will route the user to the registration page if clicked
  </p>
</details>

<details>
  <summary>Registration</summary>
  <p>
   
   #### GIF
   
  ![Registration-ezgif com-video-to-gif-converter](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/76ff12cd-65d4-4754-8336-f625f271767e)
  
  #### Component Design
   ![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/1d2c17bc-2fd8-4b96-b470-dc730b5fb10d)

#### Registration body
- This is a stateless widget
- It holds all of the widgets needed for registering a user
#### Username Input
- Text input widget
- The username entered will check if that is usable
- If it isn't usable it will not allow the user to use that username
- It will add a user with the given username when submitted
#### Password input
- Text input widget
- The password entered will check if that is usable
- If it isn't usable it will not allow the user to use that password 
- It will add a user with the given password when submitted
#### Confirm Password Input
- Text input widget
- Checks if the given password matches the initial given password
#### Register Button
- This is a button widget
- This button initializes the registration and adds the user to the user's list
#### Go to Login HyperLink
- This is a link widget
- It will route the user to the login page if clicked
</p>
</details>

<details>
  <summary>Home</summary>
  <p>
   
  #### GIF
   
  ![Loggingout-ezgif com-video-to-gif-converter](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/bd91a73e-78ce-4812-b886-c923d8b472be)

  #### Component Design
  ![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/693cd8f8-8755-475c-a625-2135a24f0079)
 

  #### App Bar
  - The description is given in the App Bar section
  - This App bar pulls out a drawer that allows the user to logout

  #### Nav Bar
  - The description is given in the Nav Bar section
  </p>
</details>

<details>
  <summary>Find a group</summary>
  <p>
   
  #### GIF
   
  ![JoiningLeaving-ezgif com-video-to-gif-converter](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/bdd0df00-3a95-4ebb-a124-03bad47300e0)

  #### Component Design
  ![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/faf3f75c-1254-46ef-b65e-abb6facd54dd)

#### App Bar
- The description given in the App Bar section
#### Group Search Body
- Stateless widget
- Holds all of the widgets that are needed on the Find a Group page
#### Search Text Input 
- Text input widget
- The text entered will search if the group name or location matches the text given
#### List of Groups
- List Widget
- Contains a list of groups that have visibility to the public
#### Group Box 
- Item Widget
- Each group box contains important info
- Group Name
- Group Location
- Only City and state
- Meeting time
- Then the concept or book the group is currently studying
- When the see more link is clicked then it will navigate to the specific group info
#### Nav Bar
- The description given in the Nav Bar section

  
  </p>
</details>

<details>
  <summary>Group Creation</summary>
  <p>
   
  #### GIF
   
  ![GroupCreation-ezgif com-video-to-gif-converter](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/4af1f759-9462-4901-a917-728921425748)

  #### Component Design
  ![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/b901216b-488b-4c95-848d-2363c7ff5a13)

#### App Bar
- The description is given in the App Bar section
#### Create Group Body
- Stateless Widget
- contains all of the widgets that are needed in the Create Group Page 
#### Group Name Input
- Text Input Widget
- The name given in the input relates to the group name in the database
- on submission, this name will be set for the group
#### About Group Input
- Text Input Widget
- The text given in the input relates to the group’s About section in the database
- on submission, this About section will be set for group
#### Group Info Input
- Text Input Widgets
- allows the user to input text for each section
- Location
- Meeting time
- Concept or book the group is currently studying
#### Set Group Public/Private
- Check Box Widget
- When checked sets the group to public
#### Create Group Button
- Button Widget
- On click creates the group
#### Nav Bar
- The description given in the Nav Bar section

  
  </p>
</details>

<details>
  <summary>Group Details</summary>
  <p>

  #### Component Design
  
  ![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/b2c14379-3f8a-4f85-b55a-e9a41980eaac)

#### App Bar
- The description given in the App Bar section
#### Group Details Body
- This is a stateless widget
- It contains all of the widgets that are needed
#### Join Button
- Button Widget
- Once the button is clicked it will send a request to join
#### Group Details
- This displays more info about the group
- Group Name
- About the Group
- Location
- Meeting time
- Then the concept or book the group is currently studying
#### Group Members List
- List Widget
- Contains every member of the group
#### Group Member
- List Item Widget
- Contains info about the user
- Name
#### Nav Bar
- The description is given in the Nav Bar section

  
  </p>
</details>

<details>
  <summary>My Groups</summary>
  <p>
   
  #### GIF
  ![Mygroups-ezgif com-video-to-gif-converter](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/b621cadf-87ff-4da9-ac9a-f75e114aee3d)

  #### Component Design
  ![image](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/fc699328-0938-44d6-9826-d996ae9db46f)

#### App Bar
- The description is given in the App Bar section
#### My Groups Body
- Stateless Widget
- contains all of the widgets that are needed in Your Groups
#### My Group List
- List Widget
- Lists off all of the groups the current user is a part of
#### My Group List Item
- List Item Widget
- Displays the last message sent as well as the group name
- On click it navigates to the messaging for that specific group
#### Nav Bar
- The description is given in the Nav Bar section


  </p>
</details>

<details>
  <summary>Chat Page</summary>
  <p>

  #### GIF
  
  ![Real-Time Messaging GIF](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/7b275b29-c144-4e4e-aaed-90322da00a3d)
  
  #### Component Design
  
  ![Chat Page Component Design](https://github.com/AceLake/Assemblage-Flutter/assets/96988100/00891cb7-c5ff-42e3-ac5d-6e75babced6d)

#### App Bar
- Description given in the App Bar section
#### Group Messages Body
- Stateless Widget
- contains all of the widgets that are needed in Create Group Page 
#### Group Settings 
- Link Widget
- On click navigate to the edit group page
#### List of Group Messages
- List Widget
- This is where all of the group messages are displayed for all users in the group to see. The current user sees their messages apart from the other members in the group.
#### Your Sent Messages
- List Item Widget
- These are the messages sent by the current user of the app.
- If the message is held down allow the user to edit or delete the message
#### Other group members' messages
- List Item Widget
- These are the messages sent by the other members in the group excluding the current user.
#### Messaging Text Input
- Text Input Widget
- When the text in this input is sent it adds a new message to the group.

  
  </p>
</details>
