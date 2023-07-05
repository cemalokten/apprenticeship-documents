
# LIFECYCYLE / PROCESS

## Describes all stages of the software development lifecycle 

1. **Research:**
   - Conduct stakeholder interviews to clarify project purpose, requirements and expectations.
   - Speak to subject area experts to gain more insight and understanding.
   - Conduct user interviews to learn how users interact with existing tools, their motivations and behaviours.

2. **Planning:**
   - Use information gathered in the research stage to plan sprints, tech-stack and what will be delivered.

3. **Design:**
   - Based on research and planning, define the look and feel of the site and how users will interact with it.

4. **Content creation:**
   - Write copy, headlines, source images and graphics.

5. **Development:**
   - After client approves the design, front-end and back-end development can begin.
   - Use agile framework

6. **Testing:**
   - Test the code and conduct user testing to identify bugs or features that are difficult to understand.

7. **Deployment:**
   - The product goes live and can be used by its intended users.

8. **Maintenance:**
   - On-going maintenance is necessary to fix new bugs, security issues or add new features to keep the product up to date.
   
## Describes the roles and responsibilities of the project lifecycle within their organisation, and their role

1. **Research**:
   - Project managers coordinate stakeholder and user interviews to define the project's purpose, requirements, and expectations.
   - I may assist with conducting user interviews, analysing data, and providing insights to the team.

2. **Planning:**
   - Senior developers plan sprints, define the tech-stack, and what will be delivered.
   - I work with the team to estimate timelines and assist with choosing the tech stack and sprint planning

3. **Design:**
   - UX and UI designers create wireframes, prototypes, and user flows that define the look and feel of the site and how users will interact with it.
   - I sometimes contribute to the design process by providing input on the feasibility of certain features or designs

4. **Content creation:**
   - Content writers and product owners create headlines, text, and other content for the site.
   - I may help write copy, headlines, source images, and graphics for the site.

5. **Development:**
   - Front-end developers implement the visual design, create interactive features, and ensure that the site is responsive and accessible.
   - Back-end developers build the server-side functionality, data storage, and APIs.
   - I assist with front-end and back-end development tasks under the guidance of senior developers.

6. **Testing:**
   - Quality assurance (QA) engineers test the site and ensure that it meets the requirements and standards.
   - User experience (UX) researchers may conduct user testing to identify usability issues and provide feedback to the development team.
   - I participate in testing within the code with expected outcomes, as well as user testing to identify bugs or features that are difficult to understand.

7. **Deployment:**
   - DevOps engineers configure the servers, deploy the code, and ensure that the site goes live smoothly.
   - I often assist with the deployment process

8. **Maintenance:**
   - Project managers coordinate ongoing SLA maintenance tasks such as fixing new bugs, addressing security issues, or adding new features to keep the site up to date.
   - I may be responsible for assisting with ongoing maintenance tasks such as fixing new bugs, addressing security issues, or adding new features to keep the site up to date.

---

# COMMUNICATION

## Describes methods of communicating with all stakeholders that is determined by the audience and/or their level of technical knowledge

### Explains how they have communicated effectively in a variety of situations to both a technical and non-technical audience.

- When communicating with stakeholders, I use different methods that are appropriate for their level of technical knowledge.

-   For **other developers on my team**, I use **technical language** to describe issues **quickly and effectively**.
  
-   Since most of my team members at Yalla are **not native English speakers**, it is **important that I use appropriate technical terms** in a concise and straightforward way to ensure **effective communication**.
  
-   When working with **clients or non-technical stakeholders**, I use **non-technical language to relay key issues in a clear way**.
  
-   I have found it useful to provide a **jargon cheat-sheet** that explains technical terms in **simple language to ensure that everyone is on the same page**

-   By using different communication methods based on the audience’s technical knowledge, I can ensure that everyone understands the project requirements and expectations.
  
-   **Clear communication with stakeholders can help to avoid misunderstandings and ensure that the project is completed successfully.**

### Compares and contrasts the different types of communication used for technical and non-technical audiences and the benefits of these types of communication methods.

- The benefits of using different communication methods for technical and non-technical audiences include:

	-   Improved understanding: Using language and visuals that are appropriate for the audience helps ensure that the message is clearly understood.

	-   Increased engagement: Using visual aids and jargon cheatsheets can help keep the audience engaged and interested.

	-   Reduced misunderstandings: By tailoring the communication method to the audience, the risk of misunderstandings and confusion is reduced.

	-   Improved outcomes: Effective communication can lead to improved outcomes, such as better decisions and increased productivity.

---

# AGILE / USER JOURNEYS / STORIES

### Describes the similarities and differences between different software development methodologies, such as Agile and Waterfall

Agile and Waterfall are two different software development methodologies, each with their own approach to project management. Here are some similarities and differences between the two:

**Similarities:**
  
-   Both methodologies require testing and quality assurance at various stages of the software development life cycle.
  
-   Both methodologies involve documentation to some extent

**Differences:**

-   Agile is an iterative and incremental approach to software development, while Waterfall is a linear approach.
  
-   Agile focuses on flexibility and adapting to changes, while Waterfall relies on a pre-defined plan that is executed in a linear way
  
-   In Agile, the software is developed in smaller chunks, while in Waterfall, the software is developed as a single unit
  
-   Agile emphasises collaboration and teamwork, while Waterfall emphasises individual tasks and responsibilities.
  
-   Agile is better suited for projects that are complex and require frequent changes or updates, while Waterfall is better suited for projects that are well-defined and have clear requirements.
  
-   Agile involves continuous delivery and feedback, while Waterfall involves a more structured and less flexible approach to software development.

Overall, as a junior developer working in an Agile environment, **I prefer Agile because it allows for more flexibility and collaboration**, which can result in a **better end product**. Agile also allows for **continuous delivery and feedback**, which can help catch issues early and ensure that the final product meets the client’s needs.

### Creates analysis artefacts, such as use cases and/or user stories to enable effective delivery of software activities

PROCESS OF GETTING RESEARCH

- **Identify the user:** The first step is to identify the user or stakeholder who will use the software. This helps me create a design that meets their needs and expectations.

- **Define the user's goals:** Once I have identified the user, I work with them to define their goals and objectives. This helps me understand what the user is trying to accomplish with the software.

- I Worked my **project manager and product owner** to create user journeys and user stories that would be used to create the requirements for the product. 

- **User journeys** are a useful tool to describe user requirements in a straightforward and understandable way, using normal language from a user's perspective.

- **User journeys** are a way to visualise the entire user experience from beginning to end

- **User stories**, on the other hand, are short, simple descriptions of a feature or functionality from the user's perspective

- Once I have created the user journeys and user stories, I **prioritise them based on their importance** and impact on the software's functionality.


---

# SOFTWARE DESIGN

### Suggests and applies different software design approaches and patterns, to identify reusable solutions to commonly occurring problems (include bespoke or off-the-shelf).

### Evaluates and recommends approaches to using reusable solutions to common problems.

 - In both projects I followed **Clean Architecture** design principles decided by senior developers at Yalla. 
 
	- Entities - SQL
	- Use-cases - Client logic
	- Controllers - Business logic
	- Database / UI

	- **Client logic** is the part of the software that handles the interaction between the user and the application, like what happens when you click a button or enter some data. 

	- **Business logic** is the part of the software that handles the rules and processes behind the scenes, like how data is stored or how calculations are performed.

-   **Clean Architecture insures everything is isolated**, so changing the front-end framework or database would mean not having to rewrite the entire codebase.

-   Followed the software design pattern of **Separation of Concerns (SoC)**
   
-   SoC separates an application into distinct sections, each addressing a separate concern
  
-   This creates an organised system that can adapt to change

-   I also used a **Component Based Architecture design pattern while using React**

-   The component based design pattern **emphasises the use of reusable parts that make up a whole**
  
-   Components are modular, independent and can be easily combined to create complex applications

	-  They help us maintain separation of concerns
	-   Code refactoring becomes much easier.
	-   Code becomes more organised and maintainable
	-   It makes testing much easier.****
  
-   REDUX - I also used the **Provider Design Pattern**, which shares global data across various components without having to pass them down into each component, making code DRY and easier to understand and debug

-   The component based design pattern **makes it easier to maintain and update code**
  
-   Material UI is a library of off-the-shelf components, such as Buttons and Inputs fields

-   It is important to evaluate reusable solutions like Material UI based on a range of criteria, such as **ease of implementation, compatibility with existing code, performance, and scalability.**

-   I used Material UI because : **maintained, documented and design**
  
-   Reusable solutions allow me to **focus on solving the bigger problems**...without having to solve the same problem over and over

- It is also important to consider the long-term implications of using reusable solutions. For example, **changes to the reusable solution** may affect other parts of the codebase

### Creates simple software designs to communicate understanding of the program to stakeholders and users of the program

1. Identify the program requirements: Before creating the software design, I identify the program requirements and define the functionality that the program should provide

2.  Once the requirements are defined, I choose an appropriate architecture pattern such as **Clean Architecture**, I do this with middleweight and senior developers

3. Separate stories into components and pages
   
4.  Design the structure of the data, for example a schema

5. Decide how the front-end, back-end and database will communicate

6.  Use design principles: I use design principles such as Separation of Concerns (SoC) and Don't Repeat Yourself (DRY) to ensure that the software architecture is simple, easy to understand, and scalable

8.  Iterate and improve: Web development is an iterative process, and I continuously seek feedback and make improvements based on the user's needs and expectations.

### Explains how they have interpreted and implemented a given design whilst remaining compliant with security and maintainability requirements

- As a Junior Web Developer, I used YUP for front-end validation to ensure that user input is correct and that the database receives the data in a type and format it expects
  
- YUP provides a simple and efficient way to validate user input and ensure that the application is secure and reliable.
  
- I made use of packages such as YUP and kept them up-to-date to ensure that the application is using the latest and most secure version of the packages. 
  
- Keeping packages up-to-date is important to prevent security vulnerabilities and ensure that the application is stable and reliable.
  
- Followed recommendations by the Cyber Essentials audit to use MFA to ensure that accounts linked to the project had an additional layer of security


---

# GIT, CI, DOCKER, SOURCE CONTROL

### Explains the relevance of organisational policies and procedures relating to the tasks being undertaken, and when to follow them including how they have followed company, team or client approaches to continuous integration, version, and source control

-   I used Git to track changes made to the project files, coordinating files amongst my team of developers.

- I used Git to push my code to a remote repository stored on GitHub where my code was reviewed by my fellow developers

- I in-turn also reviewed others code, allowing me to gain experience and understanding in different approaches and code styles

-   I Kept code DRY (**d**on't **r**epeat **y**ourself**)
  
-   I ensured code style consistency by using **ESLint and Prettier** on my local computer and also after a pushed code using continuous integration on GitHub

- I also used Docker during the Shannon Trust project

- Docker is a type of container that enables my code to run on a virtual machine, essentially it puts everything that my application needs to run, like the code, libraries, and settings, into a small package called a container. 

- A container can be easily moved between different computers or servers without worrying about whether all the necessary pieces are installed on the new machine. Making collaboration and deployment easier.
  
  
---

# DATABASE / RELATIONAL

### Applies the principles and uses of relational and non-relational databases to software development tasks

-   I chose to use a relational database for these projects
  
-   A relational database uses tables with rows and columns to store data
  
-   Each column has a specific datatype, such as a string or a number, and each row contains one value for each column
  
-   A relational database is structured and can link related tables via a unique identifier
  
-   A non-relational database is less structured and allows for more flexibility
  
-   I chose a relational database because the data for these projects was clearly defined

-   A non-relational database would be my choice when creating a quick prototype, but for a larger products that may require scaling, I think a relational database is a more robust choice
  
-   A relational database can easily be updated to accept new columns or tables
  
-   I created a database schema to visualise the database structure before implementation

### Explains how they have linked code to data sets

-   Before linking my code to a dataset such as a database, I ensure the data is stored in a structured way that can easily be understood by myself and other developers on my team

- Before creating a database, I create a schema of how the data will be structured

-   I use Application Program Interfaces (API's) to retrieve data from the backend to the front-end, enabling the front-end to connect to the back-end via an 'end point'

-   On the front-end I used the AXIOS library to interact with the end point

-   Axios is a library that provides pre-built functions for making HTTP requests such as GET and POST

-  There are other libraries, such as FETCH which are included in JavaScript however I decided not to use them as are not supported by old browsers

-   I have also used SQL (Structured Query Language) to link the backend code to the database

-   SQL allows me to write queries that can retrieve data from specific tables in the database

---

# TESTING

### Describes basic software testing frameworks and methodologies

-   I used **Jest**: a testing framework used for writing and running unit tests

-   I also used **Pa11y CLI**: a tool used for accessibility testing that checks for common accessibility issues and provides suggestions for fixing them

-   and **Storybook**: a tool used for developing and testing UI components in isolation

-   On the Shannon Trust project I used **AXE auditor** which is a tool used for accessibility testing that checks web applications for common accessibility issues and provides detailed reports on how to fix them

-   During both these projects there wasn't an opportunity for end-to-end or integration testing, but I have since worked with Playwright and Cypress for both end-to-end and integration testing

-  Integration testing focuses on testing how different components work together

-  End-to-end testing is a type of testing that verifies that the entire software system is working correctly, testing the complete flow of an application from start to finish

-  These tools help ensure that code is functional, accessible, and user-friendly, catching and fixing issues before they become major problems.

### Evaluates the use of various software testing frameworks and methodologies and justifies their choice.

- I did not use a particular testing methodology in the two projects that I have documented

- However, I have since used TDD (Test Driven Development) which involves writing tests before writing code.

- When I used the TDD methodology I followed the red green refactor approach.

- So I Write a test that fails, write code that makes the test pass and then refactor the code and the test to slowly incorporate new features

- TDD helps to ensure that the code meets the requirements and specifications of the software, and it can also help to identify and fix problems early in the development process.

- However, TDD may not be suitable for all projects, particularly those with tight deadlines or limited resources like the two project which I have documented.  

### Illustrates how to conduct test types, including Integration, System, User Acceptance, Non-Functional, Performance and Security testing including how they have followed testing frameworks and methodologies.

- **Integration testing:**  I used testing frameworks such as Jest to automate integration tests and ensure that different parts of the application are working together as expected.

- **System testing or end-to-end:** To test the entire application I used Cypress and Playwright for end-to-end testing

- **User acceptance testing:** After each sprint there is a period of testing where the stake-holders use the application and report any bugs or issues
    
- **Accessibility testing:** I use tools such as Pa11y CLI or AXE auditor to conduct accessibility testing and ensure that the application is accessible to users with disabilities.

-  **Performance testing:** I used googles lighthouse to test the performance of the Bug Reporting Platform and the Shannon Trust web app

-  **Security testing:** I did conduct security testing because we use an external company that audits our applications and suggests where we can improve


---

# DESIGN WIREFRAMES / USER INTERFACES

### Explains their own approach to design and development of user interfaces / wireframes 

-  **Before starting the development process**, I take the time to understand the user's needs and expectations. This helps me create a design that meets their needs and is user-friendly

-   On the Bug Reporting Platform I used **Figma** to create basic wireframes to test that each user journey was working as expected

-   I like to use a considered visual language throughout, ensuring visual items such as borders, text size and colours are consistent

-  I like to Keep it simple: I believe that simplicity is key to creating user-friendly interfaces, avoiding cluttered screens or too many features that can be overwhelming to the user.

-   Tools like Figma allow me to create working prototypes that can be presented to users during the research stages

-   I try to **continuously seek feedback and make improvements to the interface based on the user's needs and expectations**

---

# WAYS OF WORKING / COLLAB / PERSONAL

### Describes how they have operated independently to complete tasks to given deadlines which reflect the level of responsibility assigned to them by the organisation

1.  **Prioritisation:** I prioritise my tasks based on their importance and deadline. I create a task list and schedule my day based on the issues I have been assigned

2.  **Time management:** I manage my time efficiently, during the sprints for the Shannon Trust Web App I worked asynchronously with my team, which means that my team did not have to be online for me to be able to work on a task. It enabled me to work independently at times when I felt more motivated
   
3. I **break down large tasks into smaller ones** and set achievable goals for each day.

4.  **Effective communication:** I communicate effectively with my team and project manager, asking for help and providing regular progress updates. Working a fully remote agency, it is important that we have good communication, I use tools such as Discord and Gather to communicate.

5.  **Ask questions:**  I ask questions and clarification when needed, and I actively seek feedback to improve my work.

### Illustrates how they have worked collaboratively with people in different roles, internally and externally, which shows a positive attitude to inclusion & diversity.

- I worked with a middle-weight developer on the bug reporting platform, as a remote agency half my team is in Palestine. 

- As the documentation demonstrates, we worked together to resolve the issue and communicated the issue clearly to each other and when it was resolved ensured to celebrate the success.

- Sometimes I pair program with other developers to help resolve issues I have encountered, this helps me learn from more senior developers

- **I am flexible and adaptable in my approach to work**, recognising that different people have different working styles and needs. I am open to feedback and willing to make adjustments to my work as needed.

- **I approach my colleagues with empathy and respect**, recognising that everyone has their own unique perspective and experiences. I value diversity and recognise the strengths that come from having a diverse team.

### Explains how they have established an approach in the workplace which reflects integrity with respect to ethical, legal, and regulatory matters and ensures the protection of personal data, safety and security.

- The Shannon Trust web app was a project working with the Ministry of Justice, and required great care was taken over personal data and security

- The project was audited and changes were suggested to improve on the security and protection of personal data

- I have a good understanding of **GDPR** and where it is necessary to implement things like cookie banners to ensure **users have a choice in how their data is collected and processed**

- I have implemented security measures such as **encryption (hashing passwords, etc)** 

- I have also used tools to **hide important secrets** such as API keys which could cause data-leaks and be costly for clients


### Illustrates their approach to meeting unexpected minor changes at work and outlines their approach to delivering within their remit using their initiative.

- I understand that unexpected minor changes are inevitable in any project, and I always strive to approach them in a positive and proactive way

- When I encounter issues I speak with senior developers who are able to help me formulate a plan to resolve the issues

- Sometimes I pair program with other developers to help resolve issues I have encountered, this helps me learn from more senior developers

- I ensure that I always communicate when tasks are taking longer than their estimated time span, this way my project manager or scrum leader can update the kanban board

- I believe that by remaining proactive and focused on delivering quality work, even in the face of unexpected changes, I can help to ensure the success of any project I work on.


### Illustrates how they have responded to the business context with curiosity to explore new opportunities and techniques with tenacity to improve solution performance, establishing an approach to methods and solutions which reflects a determination to succeed.

- In a recent project, I identified an opportunity to improve password storage security, by using a password manager. 
  
- I researched best practices for password generation and storage and recommended a password manager to my team, Yalla has now implemented it as company policy.

- By being proactive I was able to significantly improve password strength and reduce the risk that passwords could fall into the wrong hands
  
- In my day-to-day work, I am constantly exploring new tools and techniques to improve my development process. 

- I regularly read articles and participate in online communities to stay up-to-date with the latest trends and best practices in web development. 

- This curiosity and willingness to learn has enabled me to continuously improve my skills and deliver better solutions for my clients.


### Explains how they reflect on their continued professional development and act independently to seek out new opportunities.

- As a junior developer, I understand the importance of continued professional development and actively seek out new opportunities to improve my skills and knowledge.

- I regularly reflect on my current skill set and identify areas that need improvement or where I would like to learn more. 

- In my spare time I complete workshops and online courses related to my field. 

- I also read blogs, articles, technical documentation and watch coding related YouTube videos to stay up-to-date on new technologies and trends.

---

- Questions quite weirdly worded
- Using notes is totally fine
- Only got 1 hour in the end and used the whole thing
- She never moved me on to another question
- I would cover a lot with a single answer, and then be asked a question I already answered, which was quite odd, like she had a list of predefined questions and was just going through them without considering if it had been answered already
- Older lady, very friendly
- Last 4 or so questions were just general about me, where I see my career going, my strengths and weaknesses, feel like I had answered everything and these we just chatty questions
- She asked at the end if there was anything I would like to cover that I hadn't so I gave said a few things which we didn't cover
- Overall felt pretty relaxed, but don't feel we covered everything on the spec.
- I have an audio recording, which is just me talking, welcome to listen to it

