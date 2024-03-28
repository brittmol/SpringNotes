## You will understand the five solid design principles

- **1. Single Responsibility Principle (SRP):**
    - **Definition:**
        - A class should have only one reason to change, meaning it should have only one responsibility.
    - **Metaphor:**
        - Think of a class like a person. A person who does one job is generally more efficient than a person juggling multiple tasks.
    - **Example:**

        ```java
        // Before SRP
        class Report {
            String generateReport() {
                // Generate report logic
            }

            void saveToFile(String filename) {
                // Save to file logic
            }
        }

        // After SRP
        class Report {
            String generateReport() {
                // Generate report logic
            }
        }

        class ReportSaver {
            void saveToFile(String filename) {
                // Save to file logic
            }
        }
        ```

- **2. Open/Closed Principle (OCP):**
    - **Definition:**
        - A class should be open for extension but closed for modification. You should be able to add new functionality without altering existing code.
    - **Metaphor:**
        - Think of a class like a box with a sealed lid. You can add things to the box (extend), but you don't need to open the sealed lid (modify) to do so.
    - **Example:**

        ```java
        // Before OCP
        class DiscountCalculator {
            double calculateDiscount(double totalAmount) {
                // Calculation logic
            }
        }

        // After OCP
        interface DiscountCalculator {
            double calculateDiscount(double totalAmount);
        }

        class StandardDiscountCalculator implements DiscountCalculator {
            @Override
            public double calculateDiscount(double totalAmount) {
                // Standard discount calculation logic
            }
        }

        class VIPDiscountCalculator implements DiscountCalculator {
            @Override
            public double calculateDiscount(double totalAmount) {
                // VIP discount calculation logic
            }
        }
        ```

- **3. Liskov Substitution Principle (LSP):**
    - **Definition:**
        - Subtypes should be substitutable for their base types without altering the correctness of the program.
    - **Metaphor:**
        - Think of a subtype like a specialized tool. If you replace a general tool with a specialized tool, the job should still get done.
    - **Example:**

        ```java
        // Before LSP
        class Bird {
            void fly() {
                // Flying logic
            }
        }

        class Penguin extends Bird {
            // Penguins can't fly, but they inherit the fly method
        }

        // After LSP
        interface FlyingBird {
            void fly();
        }

        class Sparrow implements FlyingBird {
            @Override
            public void fly() {
                // Flying logic for sparrows
            }
        }

        class Penguin implements Bird {
            // Penguins don't implement the fly method
        }
        ```

- **4. Interface Segregation Principle (ISP):**
    - **Definition:**
        - A class should not be forced to implement interfaces it does not use. Keep interfaces specific to the needs of the implementing classes.
    - **Metaphor:**
        - Think of an interface like a contract. If a class doesn't need to fulfill all parts of the contract, it shouldn't be forced to.
    - **Example:**

        ```java
        // Before ISP
        interface Worker {
            void work();

            void eat();
        }

        class Robot implements Worker {
            @Override
            public void work() {
                // Work logic
            }

            @Override
            public void eat() {
                // Eat logic for a robot?
            }
        }

        // After ISP
        interface Workable {
            void work();
        }

        interface Eatable {
            void eat();
        }

        class Human implements Workable, Eatable {
            @Override
            public void work() {
                // Work logic
            }

            @Override
            public void eat() {
                // Eat logic for a human
            }
        }
        ```

- **5. Dependency Inversion Principle (DIP):**
    - **Definition:**
        - High-level modules should not depend on low-level modules. Both should depend on abstractions. Abstractions should not depend on details; details should depend on abstractions.
    - **Metaphor:**
        - Think of it like a light switch. The switch doesn't care about the details of how electricity works; it abstracts that complexity.
    - **Example:**

        ```java
        // Before DIP
        class LightBulb {
            void turnOn() {
                // Turn on logic
            }
        }

        class LightSwitch {
            private LightBulb bulb;

            LightSwitch(LightBulb bulb) {
                this.bulb = bulb;
            }

            void operate() {
                bulb.turnOn();
            }
        }

        // After DIP
        interface Switchable {
            void turnOn();
        }

        class LightBulb implements Switchable {
            @Override
            public void turnOn() {
                // Turn on logic
            }
        }

        class Fan implements Switchable {
            @Override
            public void turnOn() {
                // Turn on fan logic
            }
        }

        class LightSwitch {
            private Switchable device;

            LightSwitch(Switchable device) {
                this.device = device;
            }

            void operate() {
                device.turnOn();
            }
        }
        ```


### **Key Takeaways:**

- **Single Responsibility Principle (SRP):**
    - A class should have only one reason to change.
- **Open/Closed Principle (OCP):**
    - Classes should be open for extension but closed for modification.
- **Liskov Substitution Principle (LSP):**
    - Subtypes should be substitutable for their base types.
- **Interface Segregation Principle (ISP):**
    - Classes should not be forced to implement interfaces they don't use.
- **Dependency Inversion Principle (DIP):**
    - High-level modules should not depend on low-level modules; both should depend on abstractions.

---

## You will be able to describe an agile development workflow

- **1. Agile Manifesto:**

    ### **Values:**

    - Individuals and interactions over processes and tools.
    - Working software over comprehensive documentation.
    - Customer collaboration over contract negotiation.
    - Responding to change over following a plan.

    ### **Principles:**

    - Welcome changing requirements, even late in development.
    - Deliver working software frequently, with a preference for shorter timescales.
    - Collaborate with customers and stakeholders throughout the project.
    - Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
    - The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
    - Working software is the primary measure of progress.
- **2. Scrum Framework:**

    ### **Roles:**

    - **Product Owner:** Represents the customer and defines the product backlog.
    - **Scrum Master:** Facilitates the Scrum process and ensures the team is adhering to its practices.
    - **Development Team:** Cross-functional, self-organizing team responsible for delivering increments of working product.

    ### **Artifacts:**

    - **Product Backlog:** A prioritized list of features and enhancements.
    - **Sprint Backlog:** The subset of the product backlog selected for a specific sprint.
    - **Increment:** The sum of all the product backlog items completed during a sprint.

    ### **Events:**

    - **Sprint Planning:** A meeting where the team plans the work for the upcoming sprint.
    - **Daily Standup:** A brief daily meeting to synchronize activities and plan for the day.
    - **Sprint Review:** A meeting at the end of the sprint to review and demonstrate the completed work.
    - **Sprint Retrospective:** A meeting to inspect and adapt the team's processes.
- **3. Kanban Method:**

    ### **Principles:**

    - Visualize the workflow to gain insights into work items.
    - Limit work in progress to avoid bottlenecks.
    - Manage and enhance the flow of work.
    - Make process policies explicit.
    - Use feedback loops to improve continuously.
- **4. Extreme Programming (XP):**

    ### **Practices:**

    - **Test-Driven Development (TDD):** Write tests before writing code.
    - **Pair Programming:** Two programmers work together at one workstation.
    - **Continuous Integration:** Integrate code changes frequently.
    - **Small Releases:** Deliver small, frequent releases of the software.
    - **Simple Design:** Keep the design of the software as simple as possible.

### **Metaphor:**

Think of an Agile development workflow as a well-coordinated dance:

- **Scrum is like a choreographed dance routine:** The roles, events, and artifacts are well-defined, creating a structured yet flexible framework for development teams to follow.
- **Kanban is like a smooth, continuous dance:** Work flows seamlessly from one stage to another, and the team adjusts dynamically based on the visualized workflow.
- **Extreme Programming is like a synchronized partner dance:** Developers work closely together, continuously integrating their code, testing rigorously, and releasing small increments frequently.

### **Key Takeaways:**

- Agile development is guided by the Agile Manifesto's values and principles.
- The Scrum framework provides a structured approach with roles, events, and artifacts.
- Kanban emphasizes visualizing and optimizing the flow of work.
- Extreme Programming introduces practices like TDD, pair programming, and continuous integration for high-quality, adaptive development.

## You will be able to compare and contrast agile and waterfall development

- **Waterfall Development:**

    ### **1. Sequential Approach:**

    - **Waterfall:**
        - Follows a linear and sequential approach.
        - Phases include requirements, design, implementation, testing, deployment, and maintenance.
        - Progress flows downward like a waterfall.

    ### **2. Planning and Documentation:**

    - **Waterfall:**
        - Emphasizes extensive upfront planning and documentation.
        - Detailed requirements and design documents are created before coding begins.

    ### **3. Rigidity:**

    - **Waterfall:**
        - Less adaptable to changes once the project has started.
        - Changes are expensive and time-consuming to implement.

    ### **4. Testing Stage:**

    - **Waterfall:**
        - Testing occurs at the end of the development process.
        - Potential for late identification of issues.

    ### **5. Client Involvement:**

    - **Waterfall:**
        - Client involvement mainly at the beginning and end of the project.
        - Limited opportunities for client feedback during development.

    ### **6. Delivery Time:**

    - **Waterfall:**
        - Final product is delivered at the end of the project timeline.

    ### **7. Metaphor:**

    - **Waterfall is like a Sequential Process:**
        - Imagine building a house floor by floor. Once you start building a floor, it's challenging to make changes to the structure.
- **Agile Development:**

    ### **1. Iterative and Incremental:**

    - **Agile:**
        - Follows an iterative and incremental approach.
        - Development is done in small, functional increments.

    ### **2. Planning and Documentation:**

    - **Agile:**
        - Emphasizes adaptive planning and responding to change.
        - Documentation is often minimal, with a focus on working software.

    ### **3. Flexibility:**

    - **Agile:**
        - Highly adaptable to changes throughout the development process.
        - Embraces changes even late in the project.

    ### **4. Testing Integration:**

    - **Agile:**
        - Testing is integrated throughout the development cycle.
        - Early identification and resolution of issues.

    ### **5. Client Involvement:**

    - **Agile:**
        - Encourages frequent client involvement and feedback.
        - Clients have visibility into the project's progress.

    ### **6. Delivery Time:**

    - **Agile:**
        - Delivers a potentially shippable product incrementally.
        - Allows for early and continuous delivery of value.

    ### **7. Metaphor:**

    - **Agile is like an Adaptive Process:**
        - Imagine crafting a sculpture with the ability to reshape and refine as you go. Flexibility is key.
- **Key Differences:**
    1. **Approach:**
        - **Waterfall:** Sequential and linear.
        - **Agile:** Iterative and incremental.
    2. **Flexibility:**
        - **Waterfall:** Less adaptable to changes.
        - **Agile:** Embraces changes and adapts.
    3. **Client Involvement:**
        - **Waterfall:** Limited client involvement during development.
        - **Agile:** Encourages frequent client collaboration.
    4. **Testing:**
        - **Waterfall:** Testing at the end of the development process.
        - **Agile:** Testing integrated throughout the development cycle.
    5. **Delivery Time:**
        - **Waterfall:** Final product delivered at the end.
        - **Agile:** Continuous delivery of increments.

### **Choosing the Right Methodology:**

- **Use Waterfall if:**
    - Requirements are well-defined and unlikely to change.
    - The project is small and straightforward.
- **Use Agile if:**
    - Requirements may change or evolve.
    - Flexibility and client involvement are crucial.
    - The project is large and complex.

### **Conclusion:**

Understanding the differences between Agile and Waterfall methodologies helps teams choose the most suitable approach based on project requirements, client involvement, and adaptability to changes. Each methodology has its strengths and weaknesses, and the choice often depends on the specific needs of the project.

---

## You will be able to identify key concepts related to SCRUMs including Sprints, regular meetings and common documentation

- **1. Sprints:**

    ### **Definition:**

    - A Sprint is a time-boxed iteration within which a specific set of work is completed. It is a fundamental unit of development in Scrum.

    ### **Characteristics:**

    - **Duration:** Typically 2 to 4 weeks.
    - **Fixed Scope:** Work is planned and committed to for the duration of the Sprint.
    - **Goal:** Each Sprint has a specific goal or deliverable.

    ### **Metaphor:**

    - **Sprints are like Running Tracks:**
        - Imagine a runner on a track. They have a clear path and a defined distance to cover. Sprints provide a focused and time-bound environment for the development team.
- **2. Regular Meetings:**

    ### **a. Sprint Planning:**

    - **Purpose:**
        - Plan the work to be performed in the Sprint.
        - Discuss and select the Product Backlog items to be included in the Sprint.
    - **Participants:**
        - Product Owner, Scrum Master, and the Development Team.

    ### **b. Daily Standup (Daily Scrum):**

    - **Purpose:**
        - Provide a quick status update and synchronize activities.
        - Identify any obstacles or challenges.
    - **Duration:**
        - 15 minutes or less.
    - **Format:**
        - Each team member answers three questions: What did I do yesterday? What will I do today? Are there any impediments?

    ### **c. Sprint Review:**

    - **Purpose:**
        - Demonstrate the work completed during the Sprint.
        - Gather feedback from stakeholders.
    - **Participants:**
        - Scrum Team, stakeholders, and Product Owner.

    ### **d. Sprint Retrospective:**

    - **Purpose:**
        - Reflect on the Sprint and identify areas for improvement.
        - Discuss what went well, what could be improved, and actions for the next Sprint.
    - **Participants:**
        - Scrum Team and Scrum Master.
- **3. Common Documentation:**

    ### **a. Product Backlog:**

    - **Definition:**
        - An ordered list of all the work to be done on the project.
        - Prioritized by the Product Owner.

    ### **b. Sprint Backlog:**

    - **Definition:**
        - The subset of Product Backlog items selected for the current Sprint.
        - Committed to by the Development Team.

    ### **c. Burndown Chart:**

    - **Definition:**
        - A graphical representation of work completed over time.
        - Helps visualize progress and remaining work in a Sprint.

    ### **d. Definition of Done (DoD):**

    - **Definition:**
        - A checklist of criteria that must be met for a product backlog item to be considered "done."
        - Agreed upon by the Scrum Team.

### **Key Takeaways:**

- **Sprints:** Time-boxed iterations with fixed scope.
- **Regular Meetings:**
    - Sprint Planning: Plan work for the Sprint.
    - Daily Standup: Quick daily status update.
    - Sprint Review: Demonstrate completed work and gather feedback.
    - Sprint Retrospective: Reflect on the Sprint and identify improvements.
- **Common Documentation:**
    - Product Backlog: Prioritized list of work.
    - Sprint Backlog: Subset of Product Backlog for the current Sprint.
    - Burndown Chart: Graphical representation of progress.
    - Definition of Done (DoD): Criteria for completed work.
