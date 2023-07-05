## OVERVIEW

The overall aim of the this project was to:
-   Develop new web-based application: Cost of Living Helper (CoL-Helper) for housing provider Hyde
-   Based on Universal Credit Helper (UC-Helper) developed by Yalla in 2021
-   It's goal was to assist people in cost of living crisis by providing a curated list of tools and resources in an easy to understand and accessible format 

The project was a fork of the original UC-Helper's codebase, the aim of this sprint was to add:
- Multi-lingual capabilities, adding a translation bar to the top of each page with a set of languages that the user could select and use the site with
- Improve overall accessibility
- Add a more extensive CMS to both the UC-Helper and the new CoL-Helper. 
- My focus was the translation feature which would include:
	- A responsive menu bar at the top of each page
	- A dropdown menu with languages displayed with their respective flags
	- The languages would be searchable
	- When a language was selected the page would be fully translated and formatted to suit the reading direction, so for instance Arabic is read right to left, so the page would need to change to suit that
	- I was tasked with researching the necessary technologies for this feature

## TEAM / COLLABORATION / ROLES

### Explain the roles and responsibilities of all people working within the software development lifecycle, and how they relate to the project

As a junior developer, I worked with many individuals on this project, each had a different role in the software development lifecycle and responsibilities within this project:

**Product owner**: Maggie Houghton from Hyde Housing
-   Represented the client's interests
-   Ensured the project met business goals
-   She worked in the research, planning, and design phases of the development lifecycle.

**Project manager**: Erica Gasparini
-  Managed the overall project
-  Oversaw timelines, budgets, and resources
-  Worked with the lead developer to break down user journeys into issues for the development team
- Organised and managed daily stand-ups, retrospectives and sprint kick off meetings
- Acted as a liaison between the development team and Hyde
- Worked through all 8 stages of the development lifecycle.

**UX/UI designers**: Jem Abulhawa and Beth Scott
- Conducted initial user testing
- Created the overall look, feel, user experience, and user interface of the website
- Worked on the research, planning, and design phases of the development lifecycle.

**Lead developer**: Ramy Al Shurafa
- Led the development team
- Worked with the project manager to ensure the project met requirements and was completed on time
- Worked on the planning, development, testing, deployment, and maintenance phases of the development lifecycle.

**Developers**: Fadi Omar, Simon Dupreesi, and myself
- Coded the website
- Worked closely with the lead developer, UX/UI designers, and project manager
- Worked in the development, testing, deployment, and maintenance phases of the development lifecycle.

Personally **I worked through five stages** of the eight stage software development life-cycle, research, planning, development, testing and deployment. Design, content creation and maintenance stages fell outside of the allocated seven weeks, and are not therefore documented.

To ensure each team member, including myself, made a contribution, we:
- Encouraged open and transparent communication
- Provided necessary resources and support throughout the sprints
- Practiced active feedback through retrospectives
- Used techniques like pair programming and code reviews to p

### !! DISTINCTION !!: Compare and contrast the requirements of a software development team, and how they would ensure that each member (including themselves) was able to make a contribution

**Similar roles**:
- **Lead developer** and **developers** (including myself): Both roles involve coding, testing, debugging, and problem-solving. We collaborated closely with each other and other team members to implement features and address issues.
- **UX/UI designers** and **developers** (including myself): Both roles have a strong focus on implementing and maintaining a high-quality user experience. We collaborated to ensure that the design and functionality of the software meet user needs and expectations.

**Differences between roles**:
- **Product owner**: This role is unique in its focus on business goals, client needs, and feature prioritisation. They worked closely with the team to refine requirements and provide feedback.
- **Project manager**: This role is distinct in its focus on overseeing project planning, resource allocation, and progress tracking. They worked closely with the team to manage risks, address issues, and maintain good communication throughout.
- **UX/UI designers**: This role is specialised in designing user interfaces, user experiences, and visual aspects of the software. While they collaborated with developers, their primary focus was on design.
- **Lead developer**: This role has additional responsibilities compared to developers like myself, such as leading the technical direction, mentoring junior developers, and making critical architectural decisions.
- **Developers (including myself)**: My role is primarily focused on writing, testing, and debugging code. Myself and other developers worked closely with other team members to understand requirements, implement features, and address issues.

While there are unique aspects to each role, all team members share the goal of creating a high-quality software product. By being collaborative and supportive of each other, we ensured that each member could make a contribution to the project's success.

### Outlines how teams work effectively to produce software and how to contribute appropriately

**Planning**:
-   Used Scrum, an Agile framework, for flexible project management
-   Broke down user journeys into stories with acceptance criteria
-   Provided progress updates to Erica the project manager regularly

**Organisational standards**:
-   My team followed the software design pattern of Separation of Concerns (SoC)
	- Separation of concerns is a principle that suggests that different parts of a program should be responsible for different tasks
	- One way we achieved separation of concerns was to use a modular approach, breaking functions and components down and importing them where needed
-   Kept code DRY (don't repeat yourself)
	- One way we did this was to store data sets in a single location and import them when required, ensuring the we did not unnecessarily replicate data making it easier to debug and maintain
-   Organised the front and back-end according to the standards laid out by Yalla in their handbook, this can be seen in Figures 5 and 6

**Code style**:
-   Used ESLint and Prettier to maintain consistent and readable code
	- This ensured consistency across all developers' work
	- This was implemented locally and also during the Continuous Integration phase, which checked the code against a set of rules

**Source control**:
-   I committed code with detailed commit messages
-   I used branches for new features and bug fixes
-   I always based branches on the latest code, so checking out the main branch, pulling any updates and then creating my feature branch from there
-   When a feature was complete, I would open a new PR and notify my team that it was ready for review
-   I then made suggested changes and requested re-reviews
-  I never merged my own code
- I also reviewed my colleagues code, which helped me learn and also further contribute to the project

**Component development and testing:**
-   I used Storybook to test components in isolation
-   This allowed me to focused on a specific components behaviour without having to insert it into the application
-   It also acted as a way to demonstrate components to my team
	- and another benefit was that it acted as a library of components, so when I was building pages I could use it as reference for how to implement other components that I did not work on

**Styling components:**
-   Used Emotion for writing CSS styles with JavaScript
-   Used a separate `style.js` file for each component following Yalla's organisational standard
	-  This approach helped modularity and maintainability

**Testing**
- I used playwright to create integration tests to test the interaction between components and ensure the overall functionality of the application.
- I used JEST to write unit tests to test individual functions and components to ensure that they were working as expected.
- I used Storybook as a tool for testing components in isolation, as mentioned above.


---

## ALGORITHMS, LOGIC, DATA STRUCTURES, FUNCTIONAL

### Outlines and applies the rationale and use of algorithms, logic and data-structures

### Demonstrate how you have applied algorithms, logic and data structures

**Algorithms:**
- I Implemented a `getCommon()` function to fetch and translate common words based on the provided language code.
	- The function first fetched the translation from the database, if the translation did not exist then English was provided as a fallback
	- Next a function checked if the language code in the response from the database matched the language code that was requested by the user
	- If it did, then a key in the response was mutated to true, if not it was sent to AWS for translation
	- Next, a function looped through the response, any translation which was not in the database was then passed to an SQL query which stored it in the database for future retrieval.
	- If it was already translated then nothing happened
	- Finally, the translation was returned.
		- The `forEach` which checked the database for the translation, was implemented to save the client money, being a charity they had minimal funds for ongoing costs. 
		- Each character sent to AWS costs money, for example 1penny per character, including spaces. If the site was being translated hundreds of times a day this cost would add up. 
		- Using this function means that if the site has been translated into a specific language already, and another user comes along and wants the site in that same already translated language, it can be fetched from the database instead of sending off to the API for translation
		- Overall this method is faster and more cost effective
- I also created the `translateJSON()` function to translate an object's values recursively while keeping the keys unchanged.
	- Takes an object, a target language, and a source language as input parameters
	- Creates an empty object to hold the translated results
	- Iterates over each key in the input object
	- If the value of the key is another object, recursively calls the `translateJSON` function with the nested object and the same target and source languages
	- If the value of the key is a string, calls the `translateText` function with the string and the target and source languages
	- Captures and logs any errors that occur during translation with the Sentry logging service
	- Adds the translated value to the response object with the same key as the original input object
	- Returns the response object with all translated values.

**Logic:**
- Designed and implemented the search feature for the language selector using React `useState` hook and the `filter()` method.

**Data structures:**
- Utilised an object inside `constants/data-types.js` to store language names and codes
- Stored `common` words object on the front end to speed up the translation and fetching
- Created a a relational Postgres database to store translations and English content in separate tables, allowing for better management, updates, and scalability.
	- I decided to keep the English content in a separate table from the translations in the database. 
	- This allowed for easy management and updates of the source content without affecting the translations. 
	- Moreover, this separation makes it simple for me to add new languages without the need to modify the existing structure of the database and to identifying missing translations. 
	- In summary, having two tables for source and translations is a more organised and efficient approach to localisation.


**Other key points:**
- Followed clean architecture principles to separate concerns in the application, making it easier to understand and maintain.
	- Clean Architecture is a way of organising the code in a project so that it is easy to understand, maintain, and test.
	- The idea is to separate the different parts of the code into different layers, each with a specific responsibility.

### Show that you have reviewed methods of software design with reference to functional/technical specifications and applied a justified approach to software development

- Reviewed functional and technical specifications to ensure that the chosen solution addressed the specific needs of the project and was compatible with existing components.

- I used a modular approach and followed Yalla's organisational standards for front and back-end code to maintain a consistent and maintainable codebase.

- I utilised Storybook to test components in isolation, allowing for focused development and ensuring that each component met design requirements.

- Implemented i18next for internationalisation (i18n), which streamlined the translation process and allowed for efficient localisation of the application. 
	- `i18next` has many features which suited the project specifications and organisation standards of Yalla
	- including fallbacks which enabled text to be shown before the response from the database was returned
	- It also enabled namespaces, which enabled different sets of translations to be loaded for each page, instead of fetching translations for the entire site

- Stored translations in a Postgres database, providing scalability and efficient retrieval of translations while keeping the base language content separate for easy management.

- Followed clean architecture principles when creating endpoints, which improved maintainability and understanding of the application.

- Implemented an algorithm to fetch, check, and translate content as necessary, ensuring that the application remained up-to-date with translations and reducing redundancy.

- Wrote unit tests for translation logic functions to identify issues efficiently and improve code quality.

- Linked the front-end and back-end using Axios, ensuring wide browser support and seamless integration between different components of the application.

- Utilised React Context to make translations available throughout the application, optimising performance by fetching data once and making it accessible to the entire app.

- Wrote integration tests using Playwright to verify that the translations were properly received by the front-end and rendered on the page, ensuring a smooth user experience.

### Creates logical and maintainable code to deliver project outcomes, explaining your choice of approach

### Show how you have applied logical thinking. For example, using clear and valid reasoning when making decisions related to planning and coding

### !! DISTINCTION !!: Explain the advantages and disadvantages of different coding and programming techniques to create logical and maintainable code

- Used functional programming paradigm, SoC, and DRY principle for better code quality.
- Ensured GDPR compliance and prioritised security measures.
- Conducted tests, used Heroku for deployment and leveraged Storybook and Emotion for UI components.
- Implemented i18next, Postgres, clean architecture, and helper functions for translation and `i18next` tasks.
- Linked the front-end and back-end using AXIOS and React context, 
- Wrote integration tests with Playwright to ensure translation functionality

**Advantages:** 
- I used an external library called `i18next` for internationalisation, making it easy to add and manage translations, plus useful functions for fallbacks and checking the users browsers language.
	- Also enabled me to use namespaces, meaning I could break the translations down into smaller chunks
- Emotion library provided a way to style components with JavaScript, making the code more modular and maintainable, allowed me to pass in variables which enabled me to write more concise code and adhere to the DRY policy
- I used Storybook allowed me to test components in isolation, improving development efficiency and collaboration
- I implemented clean architecture principles, making the code more maintainable and easier to understand. 
- By using React context, I efficiently fetched and shared common translations throughout the application. For example in Figure 26, which exports a function called `useLanguage` which could be shared across all components using React context, instead of passing props down to each component individually which would be less DRY and harder to maintain and debug.

**Disadvantages:** 
- Using multiple external libraries, like `i18next` and Emotion, might increase the complexity of the codebase and create potential dependency issues. 
- Future updates of external libraries could cause the application to break
- Vulnerabilities with external libraries are out of our control and may not be resolved
- The clean architecture approach might require more initial setup, but it pays off in the long run by keeping the code organised and maintainable. 
- While React context allows for efficient sharing of state across the application, it may not be as performant as other state management libraries like Redux for large-scale applications.

---

## TESTING

### Explain how you analysed unit testing results and reviewed the outcomes to correct errors

### Show how you Identified and created test scenarios which satisfied the project specification

I identified issues by using the browser's developer tools and server logs in the terminal to check for errors and bugs by using console log statements and built in error functions in libraries like AXIOS. Additionally, I analysed unit and end-to-end test results to identify areas for improvement. 

I identified test scenarios based on the project specifications for various components such as the LanguageBar, LanguageSelector, and front-end i18n implementation.

- I used JEST unit tests to identify issues or errors in the functions while writing the code, allowing me to fix issues efficiently as I went along.
	- I wrote a unit test to confirm the route for fetching common translations returned the expected output (Figure 21)
	- I wrote a series of unit tests to validate the three functions that made up the Translation algorithm (see Figure 24). These functions perform the single task of translating an object of key-value pairs, leaving the keys unmodified for referencing in the code while translating the values. These tests and their output helped to efficiently identify issues while I was writing the functions, rather than having to manually test each individual function as I went.
- Attempted to follow the TDD workflow of red, green, refactor on some simple functions
- Used Storybook for isolated front-end component testing, allowing me to focus on specific component behaviour and identify any issues.
	- For the LanguageBar component, I used Storybook to test it in isolation and ensure it met design and functional requirements.
- Wrote integration tests using Playwright to ensure proper front-end translation rendering on the page by simulating a user requesting a translation and checking if the expected translation was displayed. See Figure 30

---

## BUGS / PROBLEM SOLVING

### Show how you applied structured techniques to problem solving to identify and resolve issues and debug basic flaws in code

### !! DISTINCTION !! : Demonstrate how you analysed the code to identify and debug complex issues using a fix that provides a permanent solution

**IF NOT MENTIONED BEFORE THEN:**
I identified issues by using the browser's developer tools and server logs in the terminal to check for errors and bugs by using console log statements and built in error functions in libraries like AXIOS. Additionally, I analysed unit and end-to-end test results to identify areas for improvement.

**BUGS**
- An issue that was reported through user testing was that on slow connections the translations take several seconds to be rendered to the page. The user would click on a new page, and the page would be blank for several seconds, often.
	- To replicate this I used developer tools inside my browser to throttle my internet connection to a slower speed, allowing me to see the bug that others were experiencing
	- I used console log statements to log out the responses from the server
	- I realised the gaps were caused by the delay in fetching the data from the backend.
	- To resolve this I used i18next's fallback option with the `t()` function and created a static file with English text on the front-end.
- A bug that was identified through user testing was that changing the site's format caused everything to reverse, including phone numbers, which caused them to be incorrect. 
	- To prevent phone numbers from reversing in RTL languages, I set the `dir` attribute to `ltr` for direction-specific content, keeping them in the correct format.
- I encountered an issue where I was attempting to insert new translations into the database
	- By referring to sever logs in my terminal I was able to identity the issue
	- The issue was that the database schema had no requirement for a unique `language_code` and `id` combination, resulting in multiple rows with the same `common_id` and `language_code` that caused a conflict.
	- I addressed this by adding a `CREATE UNIQUE INDEX` command in the schema for the `common_i18n` and `content_i18n` tables to ensure no duplicate values in the indexed columns.
	- I wrote and tested database queries using BEEKEEPER Studio, and GUI for SQL databases. 
- I discovered through user testing that language codes provided by the browser are more specific than the codes I had used in the implementation of the function. For example, `FR-ch` instead of `fr`
	- To resolve this I used console.log's to first identify that the language codes were not what was expected by the function
	- I fixed the issue with extended language codes by slicing the first two characters of the language code, ensuring correct interpretation by the translation algorithm.

---

## CONTRIBUTION / APPROACH

### Demonstrate how you justify your approach and contribution to building, managing and deploying code into the relevant environment in accordance with the project specification

- I successfully implemented a language translation feature that allowed users to choose from 67 languages, with translations presented in their native direction, adhering to the project specification.

- My solution was efficient and cost-effective, as it translated both existing and future content, while following company procedures and producing maintainable code.

- I wrote tests to ensure that future updates would not break the feature and would alert developers to any issues before deployment.

- I deployed the CoL-Helper and updated the UC-Helper to a Heroku staging server, minimising potential issues when deploying to production and streamlining server configuration and database setup.

- Due to time and budget constraints, we maintained a local development environment without containerising the application, prioritising project requirements.

- I used Heroku's remote console for debugging and managing dependencies, deploying both UC-Helper and CoL-Helper on Heroku using sub-domains of production for client and Yalla testing.

- Deploying to the same environment for both staging and production reduced potential issues but also carried the risk of both production and staging going down simultaneously.

### !! DISTINCTION !! : Demonstrate how you evaluated different software development approaches in order justifying the best alignment with a given paradigm (for example, object oriented, event driven or procedural)

- My senior developer as mentioned previously worked on the architecture of the project, I was involved in this decision, we chose to use a functional programming paradigm for this project. In my experience, functional programming was a better choice than other paradigms, such as object-oriented programming, because it allowed me to more easily understand, modularize, test, and debug my code.

- The functional programming approach enabled me to create small, reusable, and testable functions that were easier to manage than the larger, more complex objects typically used in object-oriented programming. By breaking down my code into smaller, more manageable functions, I was able to create a more modular codebase that was easier to maintain and extend over time.

- In contrast, object-oriented programming can often result in complex and hard-to-maintain codebases with numerous class dependencies. In my experience, this can lead to code that is difficult to debug and test, making it harder to catch and resolve issues before they impact the application's performance.

Overall, I found that the **functional programming paradigm** was a better fit for this project due to its focus on small, modular functions that were easier to test and debug.

As well as using the functional paradigm, I also:

- Followed the software design pattern of Separation of Concerns (SoC), which separates an application into distinct sections, each addressing a separate concern, leading to an organised and adaptable system.
  
- Adhered to the DRY (don't repeat yourself) principle, which relates well to SoC, and organised the front and back-end in line with my organisation's standards.

- I used ESLint and Prettier to ensure uniformity, maintainability, and code style consistency across all developers' work, making the code more readable and easier to collaborate on.

- While working asynchronously with my team, I committed code with detailed messages, used branches for new features and bug fixes, opened PRs, made suggested changes, and never merged my own code.

- I followed a workflow created by my lead developer to push code from the CoL-Helper to the UC-Helper git repository.

- I implemented a cookie banner to comply with GDPR, obtaining user consent for the use of analytical technology that stored cookies containing usage data on the CoL and UC-Helper.

- To ensure security, I kept my computer's software updated, used two-factor authentication when available, and securely imported API keys and secrets through `dotenv`, adding them to my `.gitignore` file.

### How did you follow software designs and functional/technical specifications? : REDO THIS

As a junior developer, I followed software designs and also functional and technical specifications by first reviewing and analysing the issues assigned to me. I paid close attention to the requirements, constraints, and expected outcomes mentioned in the issues.

Once I had a good understanding of the specifications, I would then break down the requirements into smaller, manageable tasks that I could work on. I would also ensure that I had a clear understanding of the end-user needs and expectations to ensure that the final product would meet their needs. Based on my earlier research of the clients requirements to have a flexible and affordable language feature, I had a good overview.

I also made sure to collaborate with the project team and other stakeholders, asking questions when necessary to clarify any ambiguities or potential issues in the design. This helped ensure that my work aligned with the project goals and minimized the risk of errors or misunderstandings.

Throughout the development process, I continuously referred back to the specifications and design files to ensure that my work remained on track and aligned with the original vision. I also regularly communicated my progress and any challenges to the team to ensure that everyone was on the same page.

Ticking items off
Discussed the implementation with my senior developer before and throughout the development process


### Demonstrate how you have maintained a productive, professional, and secure working environment

- I used ESLint and Prettier to ensure uniformity, maintainability, and code style consistency across all developers' work, making the code more readable and easier to collaborate on.

- While working asynchronously with my team, I committed code with detailed messages, used branches for new features and bug fixes, opened PRs, made suggested changes, and never merged my own code.

- Maintaining good communication with my team through Discord, Gather and Notion

- I followed a workflow created by my lead developer to push code from the CoL-Helper to the UC-Helper GIT repository.

- I implemented a cookie banner to comply with GDPR, obtaining user consent for the use of analytical technology that stored cookies containing usage data on the CoL and UC-Helper.

- To ensure security, I kept my computer's software updated, used two-factor authentication when available, and securely imported API keys and secrets through `dotenv`, adding them to my `.gitignore` file.

## ADDITONAL

### SUCCESS

Two key metrics for success:
- Technically the project was successful if the code I wrote passed review and testing, was merged into staging and passed quality assurance.
- Engagement metrics were measured using heat-mapping and page analytics and only became apparent after the product was deployed. 
Another metric which became important later was loading speed:
- A slow-loading site can be frustrating for visitors and can lead to high bounce rates. Measuring loading speed and optimising the site to load quickly can be an important factor in retaining visitors.

### PLANNING

- We assigned a level of risk to each issue based on our experience, and confidence in that task. Language translation was assigned a high-risk factor due to our limited understanding and experience.
