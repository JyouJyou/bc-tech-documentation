---
layout: page
title: Project Management
permalink: /project-management/
---

## **Project Scope**

### Software Development Life Cycle Model

In this project, a mix of Scrum and XP will be adopted. The following paragraph describes the flow:

![SDLC](../images/SDLC.jpeg)

Before each release, the development team would go through the development cycle depicted in the diagram above. Every morning,
a short daily scrum meeting which lasts 5~15 minutes would be held by the developers to discuss about the project progress and 
difficulties faced. Two weeks are defined as a **sprint** (follow the scrum convention) and a milestone is expected to 
 be reached at the end of a sprint. While each week is defined as a semi-sprint, at the end of
each week (Friday), a meeting would be held to adjust the Gantt chart and development velocity and adapt to the 
potentially capricious requirement specification. 

This project is divided into two milestones: v1.0 and v1.1 
- v1.0: a deliverable product supporting continuous integration, and continuous deployment. (Expect a test structure to be settled.)
- v1.1: a fully tested and configurable product with the test coverage being greater than or equal to 75 percent. (Expect to support configuration.)

- Product Owner: Sinopac
- Scrum Master: Simon Chu
- Development team: Eddy and Hou Rui

### Revision Control

#### **Revision Control Software**: Github

#### **Revision Control Work flow**: Branching WorkFlow

![branch workflow](../images/branch-workflow.png)

### User Stories

Priorities: High (must have) - `* * *`, Medium (nice to have) - `* *`, Low (unlikely to have) - `*`

| US ID | Priority | As a …                                                         | I want to …                                                                                 | So that I can…                                                                     |
| - | -------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| <a name="US1">1</a> | `* * *`  | TMU Sales                                                   | collect the PSR data, CRM information, and transaction history on a client call (before pick up). - **SCENARIO 1** | |
| <a name="US2">2</a> | `* * *`  | TMU Sales                                                   | collect the PSR data, CRM information, and transaction history on answering a phone for other TMU sales(after pick up). - **SCENARIO 2** | |
| <a name="US3">3</a> | `* * *`  | TMU Sales                                                   | collect the PSR data, CRM information, and transaction history on proactively barging in other TMU sales' phone call. - **SCENARIO 4** | |
| <a name="US4">4</a> | `* * *`  | TMU Sales                                                   | collect the PSR data, CRM information, and transaction history on calling out. - **SCENARIO 8** | |
| <a name="US5">5</a> | `* * *`  | TMU Sales                                                   | collect the PSR data, CRM information, and transaction history on answering a transferred call (after pick up). - **SCENARIO 9** | |
| <a name="US6">6</a> | `* * *`  | QA engineer                                                 | have a continuous testing zone | continuously integrate the entire system and test iteratively. |
| <a name="US7">7</a> | `* * *`  | QA engineer                                                 | have a minimum 75% (standard adopted in SalesForce) test coverage system | assure the quality of the system.  |
| <a name="US8">8</a> | `* * *`  | Deployment engineer                                         | have a continuous deployment workflow | design the deployment plan and prepare the production and the UAT environment. |
| <a name="US9">9</a> | `* * *`  | Deployment engineer                                         | have a configuration system | deploy the product according to a customized environment to a certain degree. |
| <a name="US10">10</a> | `* * *`  | Maintenance engineer                                        | have a log management system | perform minimum system maintenance and report logging error to the developers. |
| <a name="US11">11</a> | `* * *`  | Developer                                         | maintain an always up-to-date developer guide and documentation | debug and scale the system much more efficiently. |
| <a name="US12">12</a> | `* * *`  | Developer                                         | a static analyzer for code quality and programming style | drastically reduce the amount of effort required for vulnerability check. |


## **Work Breakdown Structure (WBS)**

| Task ID | Task                                                        | Estimated Effort        | Buffer        |
| ------- | ----------------------------------------------------------- | ------------------------| -------------- |
| 1       | Bluewave system analysis                                    |  | |     
| 1.1     | Build quick event catcher                                   | 3 man hour | 1 man hour |
| 1.2     | Organize event snippets                                     | 1 man hour | 0.5 man hour |
| 1.3     | Bluewave system consultation with the stake engineers       | 1 man hour | 0.5 man hour |
| 1.4     | Design parser and logger structure based on system analysis result (meeting required) | 3 man hour | 1 man hour |
| 2       | Backend Revamp   |||
| 2.1     | Backend re-factoring |  |  | 
| 2.1.1     | Modularize existing code into multiple components (refactoring) | 3 man hour | 1 man hour | 
| 2.2     | Backend re-design |  |  | 
| 2.2.1     | Modularize existing code into multiple components (refactoring) | 3 man hour | 1 man hour | 
| 2.2.2     | Mock stored procedure set-up | 3 man hour | 1 man hour | 
| 2.2.3     | Build backend Persistence Layer structure (with stored procedure) | 2 man hour | 1 man hour | 
| 2.2.4     | Build parser and **Log strategy** | 6 man hour | 2 man hour | 
| 2.2.5     | Build Bluewave auth handler and receiver APIs | 3 man hour | 1 man hour | 
| 2.2.6     | Set up business logic component | 2 man hour | 1 man hour | 
| 2.2.6     | Arrange and structure the backend APIs, web socket, and encryption flow | 6 man hour | 2 man hour | 
| 3       | Frontend Revamp                                   |  | |   
| 3.1     | Frontend re-factoring |  |  |   
| 3.1.1     | Segregate existing code into microservices - authorization, components | 3 man hour | 1 man hour | 
| 3.1.2     | Centralize style sheets and themes | 5 man hour | 1 man hour | 
| 3.1.3     | Add the checkstyle support | 5 man hour(including trial and error) | 1 man hour | 
| 3.2     | Frontend re-design |  |  |   
| 3.2.1     | Build state management structure (consider to include Redux) | 6 man hour | 2 man hour | 
| 4       | Testing                                   |  | |   
| 4.1     | Backend Unit Testing                       |  | |   
| 4.1.1     | Auth component        | 3 man hour | 1 man hour |  
| 4.1.2     | Parser component      | 4 man hour | 1 man hour |  
| 4.1.3     | Persistence Layer component (test ORM)       | 4 man hour | 2 man hour |  
| 4.1.4     | Logic component test with Mock Database, Parser Stub, Auth Stub, and Data Stubs  | 6 man hour | 2 man hour |  
| 4.2     | Backend Integration Testing                       |  | |   
| 4.2.1   | Database + Persistence Layer (set up -> execution -> expectation -> clear up)   | 6 man hour | 2 man hour | 
| 4.2.2   | Bluewave component + Bluewave  | 2 man hour | 1 man hour |   
| 4.2.3   | **Logic** + Persistence Layer + Parser + Auth + Bluewave | 2 man hour | 1 man hour |    
| 4.2.4   | Backend API test | 6 man hour | 2 man hour |    
| 4.3     | Frontend testing              | tbd | tbd |  
| 5       | Deployment             | | |    
| 5.1     | Set up Jenkins in JyouJyou Server (possibly Docker)    | 3 man hour | 3 man hour |
| 5.2     | Set up Jenkins + Tomcat + Git CI/CD environment (including frontend and all other possible applications) | 6 man hour | 3 man hour |    
| 6       | Log management system and configuration          |  |  |  
| 6.1     | Log message parser         | 3 man hour | 1 man hour |   
| 6.2     | Response distributor       | 6 man hour | 2 man hour |   
| 6.3     | UI       | 6 man hour | 2 man hour |   
| 6.4     | Unit testing for parser and distributor       | 4 man hour | 2 man hour |   

## **PERT chart**

![SDLC](../images/PERT.jpeg)

## **Gantt chart**

![SDLC](../images/Gantt.png)