
- Assume we need to devolop a E-commerce application called **example.com**

<img width="1582" height="1061" alt="image" src="https://github.com/user-attachments/assets/05a32c08-148f-461f-9325-fea37fd08642" />

- Above are the SDLC standard all organizations should follow

- If in case E-commerce app need to introduce new feature called **kids section**, before it selling only for **Mens-section**

**1. Planning-Phase**

- In the planning phase of the Software Development Life Cycle (SDLC), the primary focus is on gathering requirements (9:45). This is considered a fundamental starting stage where product owners, business analysts, and senior team members collect input from customers (10:07).

- The goal is to understand customer needs and determine if a proposed feature or product is genuinely useful and desired (10:37-10:53). For example, if an e-commerce website is considering adding a "kids' section," they would gather data on customer interest in various age ranges for kids' clothing (11:10-11:32). This information helps in deciding whether to proceed with the idea or suspend it at this early stage, avoiding wasted effort in later phases (10:55-11:00).

**2. Defining-Phase**

- The defining phase is where the gathered requirements are clearly documented (11:38). For example, a product owner or business analyst would write a Software Requirement Specification (SRS) document (12:17) that includes all the data collected during the planning stage.

**3. Designing-Phase**

The designing phase is a crucial stage where high-level design (HLD) and low-level design (LLD) are created (12:31-12:39).

- High-Level Design (HLD): Architects or senior resources define the overall system architecture, focusing on aspects like scalability and high availability. This includes decisions on databases and the number of application replicas (13:16-13:27).

- Low-Level Design (LLD): Senior members of the development team design the system in detail, specifying particular functions, modules, database calls (e.g., MySQL), and the arguments/responses for function calls (13:28-14:12).

<img width="1028" height="674" alt="image" src="https://github.com/user-attachments/assets/a7868a54-8f7a-4df0-8ae0-aafbd9e5c453" />


***********************************************************

The phases of SDLC that are considered DevOps-centric or where a DevOps engineer should be primarily interested are (14:55):

Building the software (developing) (15:50-16:00, 16:23-17:17)
Testing the software (16:00-16:02, 18:48-19:20)
Deploying the software (16:02-16:10, 19:26-19:57)
A DevOps engineer's main goal in these phases is to automate the processes to improve efficiency and reduce manual intervention (20:58-21:10, 22:50-23:04).

<img width="1134" height="677" alt="image" src="https://github.com/user-attachments/assets/5e59b923-af99-4909-b427-35fccf6fed52" />


**4. Building-Phase**

Building (Developing) Phase: This is where developers write the application code based on the design documents. Once the code is written, it's pushed to a common source code repository like Git (16:26-18:21).


**5. Testing Phase**

After development, the application is deployed to a server (like a staging or development server) where the Quality Assurance (QA) team tests it to ensure it meets quality standards (18:27-19:24).


**6. Deployment Phase**

In this final stage, the tested application is promoted to the production server, making it available to the end customer (19:25-19:55).

The video also briefly mentions the Agile Model (23:32-23:53). It is described as a project management methodology where organizations follow all the SDLC phases but in short sprints. This means that instead of waiting for all planning, defining, or design documents to be completed, small chunks of work are processed through the entire cycle, allowing for continuous iteration and delivery.



