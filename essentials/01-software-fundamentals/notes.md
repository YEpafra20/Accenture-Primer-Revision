# Software Fundamentals — Revision Notes

**Category:** Essentials · **Focus Area:** Critical Thinking · **Level:** Intermediate

---

## Table of Contents

1. [Logic Development](#1-logic-development)
2. [Selection Statements](#2-selection-statements)
3. [Looping Statements](#3-looping-statements)
4. [Arrays](#4-arrays)
5. [Software Engineering Fundamentals](#5-software-engineering-fundamentals)
6. [Phases of Software Engineering](#6-phases-of-software-engineering)
7. [Software Testing](#7-software-testing)
8. [Software Configuration Management](#8-software-configuration-management)

---

## 1. Logic Development

### 1.1 Introduction to Logic Development

Logic development is about building the step-by-step thinking process required to solve a problem before writing actual code. This is done using **algorithms**, **flowcharts**, and **pseudocode**.

### 1.2 Introduction to Algorithms, Flowcharts & Pseudocode

**Algorithm**
A step-by-step list of instructions to be followed in problem-solving operations.

**Flowchart**
A diagrammatic representation of an algorithm, workflow, or process.

**Symbols in a flowchart:**

| Symbol | Meaning | Shapes
|---|---|--- |
| START / END | Denotes start/stop operations | oval shape symbol
| INPUT / OUTPUT | Denotes getting inputs and displaying outputs | parellogram shape symbol
| PROCESS | Denotes actions or operations performed | Rectangle shape symbol
| FLOW DIRECTION | Denotes the direction of the process flow | arrow symbol
| CONNECTOR | Connects steps in the process | circle shape symbol
| DECISION | Indicates choices/questions to be answered (usually Yes/No or True/False) | diamond shape symbol

### 1.3 Defining Variables, Constants & Expressions

An algorithm consists of **variables**, **constants**, and **expressions**.

- **Variable** — name of a memory location whose value keeps changing. Variables are containers used to store values.
- **Constant** — like a variable, except its value is fixed. Once defined, it cannot be changed or undefined. Example: `PI = 3.14`
- **Expression** — a combination of operands and operators. An operand can be a variable or a constant.

### 1.4 Commonly Used Operators and Operations

Operators are symbols used to perform specific mathematical and logical computations on operands.

| Operator Type | Purpose |
|---|---|
| **Assignment Operator** | Used to assign a value to a variable. Example: `height = 5` or `c = a + b` |
| **Arithmetic Operator** | Performs Addition, Subtraction, Multiplication, Division, Power (Exponentiation), Remainder (Modulo) |
| **Relational Operator** | Compares two operands: less than, less than or equal to, equal to, not equal to, greater than, greater than or equal to |
| **Logical Operator** | Makes decisions based on multiple conditions: AND, OR, NOT |

### 1.5 Pseudocode

An informal way of describing algorithms, using a combination of natural language and programming-language-like structure.

- Does not require strict programming language syntax
- Easy to read and understand

---

## 2. Selection Statements

Selection statements allow a program to make **decisions** and choose between different paths of execution based on a condition (e.g., if a condition is true or false). They work together with relational and logical operators covered in [Section 1.4](#14-commonly-used-operators-and-operations) to control the flow of a program. 
selection statements can be categorised as (simple if, if-else, else-if ladder, nested if)
[Dry Run - Manual execution of steps in an algorithm is called as Dry Run.]

---

## 3. Looping Statements

**Flow of a program:** The order in which a computer executes the statements in a program.

Looping statements allow us to avoid repeating the same lines of code again and again. Depending on the situation, different loop types are used: **For**, **While**, **Do-While**, and **Nested Loop**.

### 3.1 For Loop

Code may execute 0 times or as many times as required by the condition. Used to execute a block of statements when the **number of iterations is known**.

```
FOR (specific condition)
DO
   ...
END FOR
```

### 3.2 While Loop

Repeats a statement or group of statements while a given condition is true. Tests the condition **before** executing the loop body.

```
WHILE (condition)
DO
   ...
END WHILE
```

### 3.3 Do-While Loop

Similar to the While loop, except it tests the condition **at the end** of the loop. The block of statements executes **at least once**.

```
DO
   ...
UNTIL (condition)
```

### 3.4 Nested Loop

Used when one or more loops are needed inside another looping statement (while, for, or do-while).

- The outer loop executes first, based on its condition
- The outer loop triggers the inner loop to execute completely until the condition fails in the inner loop
- After the inner loop finishes, control returns to the outer loop for its next iteration, which triggers the inner loop again
- This process continues until the condition fails in the outer loop

---

## 4. Arrays

**What is an array?**
A collection of homogeneous data stored sequentially. An array is a variable used to store data of the same type contiguously.

- Arrays have a **fixed size**
- Arrays can be classified as **single-dimensional** and **multi-dimensional**

### 4.1 One-Dimensional Arrays

1-D arrays are treated as a linear list of values. Elements are stored sequentially and accessed using the **index** of the array.

### 4.2 Two-Dimensional Arrays

An array of arrays (a list of arrays). Elements in array is treated like a Matrix and can be accessed using index of array. 
2-D arrays are represented as rows & columns.

### 4.3 Manipulating Arrays

Various operations can be performed on an array:

- Inserting elements
- Deleting elements
- Searching elements
- Sorting elements
- Accessing elements

---

## 5. Software Engineering Fundamentals

### 5.1 Key Terms

- **Program** — A computer program is a sequence of instructions written to perform a specified task on a computer.
- **Software** — A set of programs, procedures, and its documentation concerned with the operation of a data processing system.
- **Process** — A series of definable, repeatable, and measurable tasks leading to a useful result.

> Software Development Process involves the transformation of user needs into an effective software solution.

### 5.2 History — Ad-hoc Software Development (until 1960s)

- Software was developed on a trial-and-error basis
- No specific process was followed during development; no proper testing was done
- Defects were detected only **after** the product was delivered to external users

### 5.3 What is Software Engineering?

Software engineering is the application of a **systematic, disciplined, quantifiable approach** to the design, development, operation, and maintenance of software.

### 5.4 SDLC — Software Development Life Cycle

SDLC is the process used in a project to develop a software product.

- Defines the phases and tasks to be performed with the objective of developing software that meets requirements
- Describes how development activities are performed, and their appropriate sequence

**Phases in SDLC:**

```
Planning & Analysis → Design → Implement → Test → Deploy → Maintain
```

1. **Analysis** — Define the requirements of the system. Focus is on identifying the problem the customer is trying to solve.
2. **Design** — Documentation into system specification (System Design).
   - **Levels of design:** High Level Design (HLD) & Low Level Design (LLD)
   - **HLD:** What modules are required, what each module performs, and how the modules communicate with one another
   - **LLD:** Focuses on writing a detailed algorithm
   - **DD (Design Document) = HLD + LLD**
3. **Construction (Code + Unit Testing)**
   - Modular and subsystem programming code is accomplished during this stage
   - The design is converted into a workable solution using a programming language
   - Unit testing is done at this stage, by the developers
   - This stage produces the source code, executables, and applicable databases
4. **Testing** — Testing is the process of executing the program with the intent of finding errors.
   - **Software Testing:** Process of verifying and validating that a software application or program meets the business and technical requirements
   - **Levels of Testing:**
     - **Unit Testing** — done by the developer, on an individual module, for functional correctness
     - **System Testing** — checks for interface errors between the integrated components (Functional testing and performance testing)
     - **Integration Testing** — tests the system as a whole, checking functional and non-functional correctness
     - **Acceptance Testing** — done by the end user, for system acceptance (alpha testing and beta testing)
   - **Verification, Validation & Defects:**
     - **Verification** — confirms the software meets its technical specifications
     - **Validation** — confirms the software meets the business requirements
     - **Defect** — the variance between the expected and actual result
5. **Maintenance** — Changes or enhancements happen everywhere; software is no exception.
   - **Software Maintenance:** any change made to the software after it is deployed

### 5.5 Software Engineering Process Models

| Model | Description |
|---|---|
| **Waterfall Model** | Also known as the linear sequential model: Analysis → Design → Coding → Testing → Deployment → Maintenance |
| **V-Model** | Verification and Validation Model,its an extension of waterfall model where testing is emphasized more than in waterfall model. testing is done from earliest phases and each phase must be completed before the next phase begins. |
| **Prototype Model** | Developing a model for the system to be built. Two types: **Throw away** (used when requirements are unclear; built and given to the end user for review, then discarded) and **Evolutionary** (used when requirements are unstable; refined repeatedly by the developer until the prototype becomes the final system) |
| **RAD Model** | Rapid Application Development — modules developed in parallel as if they were mini-projects; high speed; component-based approach. Phases: 1) Business Modelling, 2) Data Modelling, 3) Process Modelling, 4) Application Generation, 5) Testing and Turnover |
| **Incremental Model** | Uses incremental development cycles, the incremental model priorities requirements of the system and implements them in small manageable units called as modules.each module undergoes analysis,design,coding and testing. |
| **Spiral Model** | Proposed by Barry Boehm in 1986. Suggested for high-risk-scenario-based projects. The number of loops of the spiral is unknown and varies from project to project .each loop of the spiral represents a phase of software development process.|

---

## 6. Phases of Software Engineering

### 6.1 Requirement Analysis (RA)

- **Requirements Engineering** — the process of defining, documenting, and maintaining requirements
- **Requirement** — a capability that the system must possess to meet a need, solve a problem, or offer a service
- **Requirements Elicitation** — gathering requirements from the users

**Common issues in RA:**

- **Contradicting requirements** — one requirement conflicts with another
- **Incomplete requirements** — some requirements have been omitted due to oversight

### 6.2 Requirement Analysis — SRS & ERD

**Software Requirements Specification (SRS) Document:** - it is a contract between development team and customer. SRS document focuses on "What needs to be done" and carefully avoids the solution ("how to do") aspects.

- **Functional requirements** — specify the input, the task, and the output. it describes a service that a software must offer.
- **Non-functional requirements** — specify the overall quality attributes and constraints. it describes qualitative attributes of a software such as (Maintainablity,portablity,usablity,reliablity,robustness,security,performance etc.)
- **Constraints on the system** — specify the restrictions ,
- SRS Constraints are (Standard compliance , hardware to be used , operation system, DBMS to be used ,Capablities of I/O devices ,Data Representation)

**Entity Relationship Diagram (ERD):**
Part of data modeling that focuses on defining and analyzing the data needed to support the business. it represents the conceptual lebvel of database design.
-Entity -> an entity is an business object that represents a group or category of data.
-Relationship -> specifies the relations among the entities. it is characterised by Cardinality and Optionality.
-Attribute -> Properties of an entity.

### 6.3 Software Design

Design converts the Software Requirement Specification document into a system specification.

### 6.4 Software Design and Coding

**Code + Testing:** Modular and subsystem programming code is accomplished during this stage.

---

## 7. Software Testing

### 7.1 Software Testing

- Testing is the process of executing a program with the intention of finding errors
- **Definition:** The process of verifying and validating that a software application or program meets the business and technical requirements that guide its design and development, and that it works as expected
- **V & V:**
  - **Verification** — are we building the product right?
  - **Validation** — are we building the right product?
- **Purpose:** Software testing is a process that ensures the correctness, completeness, and quality of the developed software

**Software Testing Life Cycle (STLC):**

```
Test Plan → Test Design → Test Execution → Report to Developer → Test Cycle Closure
```

**Methodologies of Testing:**

- **Manual Testing** — tests are executed manually by the QA
- **Automated Testing** — testers use automated scripts/tools to automate test execution and compare expected vs. actual results (e.g., JUnit for Java, NUnit for .NET)
- **Defect Tracking** — the process of logging and monitoring bugs during testing

**Levels of Testing:**

| Level | Performed By |
|---|---|
| Unit Testing | Developers |
| Integration Testing | Developers |
| System Testing | Testers |
| Performance Testing (Manual & Automated) — includes Stress Test, Regression Test, Usability Test | Testers |
| User Acceptance Testing | Client |

### 7.2 Static Testing

Testing of software work products manually, to find errors. Techniques include: **Review**, **Walkthrough**, **Inspection**.

**Members involved in static testing:** Author, Moderator, Reader, Recorder/Scribe.

### 7.3 Dynamic Testing

Also called glass box testing, structural testing, clear box testing, black box testing, white box testing.

- **Black Box Testing** — test cases are designed depending on the functionality. it identifies hidden functionalities.
- the Black box Testing techniques are Equivalence class partitioning , Boundary Value Analysis ,Cause Effect Analysis and Graphing , Decision Table.
- **White Box Testing** — deals with the internal logic and structure of the code . it identifies unreachable Code and checks for code coverage.
- the White box testing technique is Basic path testing.

### 7.4 Software Maintenance

- Modifying a program after it has begun being used
- Maintenance does not normally involve major changes to the system architecture
- Changes are implemented by modifying existing components or adding new components to the system

**Types of Maintenance:**

| Type | Description |
|---|---|
| **Corrective Maintenance** | Repair of defects in the existing system |
| **Adaptive Maintenance** | Adapting the software to changes in the working environment |
| **Perfective Maintenance** | Functional enhancements that increase the system's performance |
| **Preventive Maintenance** | Changes made to prevent the occurrence of errors in the future |

---

## 8. Software Configuration Management

**Software Configuration Management (SCM):**
A configuration is the functional and physical characteristics of hardware or software as set forth in technical documentation or achieved in a product.

### 8.1 Four Components of SCM

| Component | Description |
|---|---|
| **Configuration Identification** | Defines the product and its configuration documentation identification |
| **Change Management** | Controls changes to a product and its configuration documentation |
| **Configuration Status Accounting** | Provides status and information about a product and its configuration documentation |
| **Configuration Audits** | Reviews items against various specifications to ensure quality and correctness |

### 8.2 Version Management

Version control is a mechanism used to manage multiple versions of computer files and programs.

### 8.3 Software Configuration Management — Activities

1. Code is kept in a common repository
2. Developers pick up a working copy and work on their local machines
3. Changes are committed to the repository
4. Check if anyone has checked in the same file in the repository
5. If yes, compare the conflicts and merge the changes as per the requirement
6. Check in the new version of the files into the repository

## THE END 🎉
---
