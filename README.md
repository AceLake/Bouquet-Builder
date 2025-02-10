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


## **Physical Solution Design**  

<img width="734" alt="image" src="https://github.com/AceLake/Assemblage-Flutter/assets/96988100/e9422bfe-7091-4182-b059-7360ffc8db3d">  

### **Description**  

#### **Physical Solution Design**  
The Physical Solution Design provides an overview of the actual development environment used to build **Bouquet Builder**. The code is developed using **Visual Studio Code (VS Code)** on the host device, ensuring an efficient and robust cross-platform development workflow. This setup allows for thorough testing on both simulated and physical devices, ensuring a seamless experience across different platforms.  

#### **Android Testing**  
Android testing is performed on a **Windows PC** using **Android Studio** to run the Android emulator. VS Code detects the active simulator, allowing for efficient deployment and debugging within the Android environment.  

#### **iOS Testing**  
iOS testing is conducted on a **MacBook**, utilizing the iPhone simulator via **Xcode**. VS Code seamlessly integrates with the simulator, enabling deployment and testing throughout the development cycle.  

#### **Physical Testing**  
For wired testing on real devices, **Xcode** builds the application and deploys it onto a physically connected iPhone. This process ensures the app functions as expected on actual hardware.  

---

## **Detailed Technical Design**  
This section outlines the **architectural and technical considerations** necessary to build **Bouquet Builder** to industry standards. It includes diagrams and descriptions to provide clear guidance on the app’s structure and implementation.  

### **General Technical Approach**  
**Bouquet Builder** is designed with **adaptability** in mind, allowing for flexible data structures while maintaining a user-friendly experience. The app is built to **handle large datasets efficiently**, making it well-suited for florists managing extensive inventories of flowers, vases, and bouquet designs.  

### **Key Technical Design Decisions**  
- **Framework:** Flutter  
- **Programming Language:** Dart  
- **Database:** Firebase (NoSQL)  

#### **Why These Choices?**  
- **Flutter** was chosen for its cross-platform capabilities, allowing the app to run seamlessly on both iOS and Android with a single codebase.  
- **Dart** provides an **object-oriented structure**, making the app scalable and maintainable.  
- **Firebase** is a **NoSQL database**, which enables the app to handle vast amounts of data efficiently while allowing for flexible data storage and retrieval.  

---

## **Database Structure Diagram**  

![Database Structure Diagram drawio](https://github.com/user-attachments/assets/8e6f84c2-137d-46b7-be92-d76b9fbad887)


This diagram illustrates the **relationship between different data entities in Firebase**. Given that Firebase is a **NoSQL database**, traditional table-based relational models aren’t used. Instead, a **NoSQL Entity Relationship Diagram (ERD)** helps visualize how **users, bouquets, flowers, and orders** interact within the system.  

Each **user** can create and manage multiple **bouquets**, each bouquet contains a list of **flowers and vases**, and orders track bouquet purchases or reservations.  

---

## **Sitemap**  
![BB_Sitemap drawio (1)](https://github.com/user-attachments/assets/a6aabb87-fe1a-45ea-8b41-2f7720cfa7ed)

### **Description**  

- 🟢 **Green:** Create operations (e.g., adding a new bouquet, flower, or vase).  
- 🟣 **Purple:** Read operations (e.g., viewing available bouquets, order history).  
- 🟠 **Orange:** Update operations (e.g., editing bouquet details, updating flower prices).  
- 🔴 **Red:** Delete operations (e.g., removing a bouquet or flower from the inventory).  
- 🔵 **Blue:** Non-CRUD features (e.g., static pages, settings, and navigation).  

### **Navigation Flow**  
When the app launches, users are directed to the **login page**. New users can register directly from this screen. Once logged in, they are taken to the **home page**, where they can browse, create, or manage bouquets.  

The app maintains a **consistent navigation structure**:  
- A **bottom navigation bar** provides quick access to core pages.  
