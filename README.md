# Creating a Specification for a software system 

## Table of Contents
1. [Step 1: Build, install and configure the RADIUS Server](#step-1-build-install-and-configure-the-radius-server)
2. [Step 2. Build access control policy](#step-2-build-access-control-policy)
3. [Step 3. Model (Architect) the access control policy](#step-3-model-architect-the-access-control-policy)
4. [Step 4. Test Plan](#step-4-test-plan)
   4.1 [Test report](#31-test-report)
   4.2 [Test Planning](#32-test-planning)
   4.3 [Checking results](#33-checking-results)
5. [References](#references)

## Step 1: Build, install and configure the RADIUS Server
![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/1940567e-e0e3-45d6-aac9-b6a5ab35242f)

Policy Showing Guest Access is restricted to users that are not in the “VPN” Group. 
![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/dba84975-9381-4612-a1a8-d9273c4e8b16)

Access Granted to “Fatima” as she is an Approved User and has the required Roles.
![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/707e3882-52b7-460e-b9d8-35c12e808946)

5 Roles were created to separate the diverse types and connections that are allowed on the VPN.
![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/a951225b-721a-4ec2-a69a-f43db73dbd01)

Different Objects with multiple controls to within the objects to limit/grant access. 
![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/34105186-8b77-4d9f-814b-51d90537d119)

Verifying we do not allow Guest, with membership to the group “Guest” on to the VPN.
![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/55a37109-30e5-4cc0-9379-3dbc42b64af5)

Selected “No Guests...” you can see multiple objects configured to prevent access at multiple levels.
![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/fba532f6-af6f-4cc7-800f-66564a1b4a7b)

Roles are user and group-based access controls.

## Step 2. Build access control policy

1. **DETERMINE TEAMMATES TO BUILD ACCESS CONTROL POLICY**
   - With the proper application controls, businesses and organizations greatly reduce the risks and threats associated with application usage because applications are prevented from executing if they put the network or sensitive data at risk.
   - Why is access control important? The goal of access control is to minimize the security risk of unauthorized access to physical and logical systems.
   - Who decides how and when data in an organization will be used or controlled? Control and use of data in the Data owners are responsible for how and when data will be used, Data users are working with the data in their daily jobs.

2. **ACCESS CONTROL**
   - The rapid transformation to the digital world has required major changes to how organizations manage their workforce and in particular how they deliver and govern access to critical applications and data. That workforce is no longer just human users; employees, contractors and vendors, but also bots or service accounts each needing their own set of access requirements, restrictions, and locations. Additionally, data and applications spread cross cloud, on premises and hybrid infrastructures are being accessed from anywhere, on a variety of devices. Today many organizations are relying on identity tools designed to quickly authenticate and federate access to workers. While these tools offer basic lifecycle management capabilities to enable workers with 24/7 access, they lack the needed security access controls and policies required to effectively know who can access what and more importantly deliver access based on who can access what and more importantly deliver access based on who should access what.
   
3. **CONTROL PURPOSE**
   - An access control policy provides rules and guidelines structuring who can access data and resources at an organization. It takes the form of a document offering a high-level overview, and is then implemented via more specific rules and procedures.

**Title:** Access Control Policy  
**Effective Date:** 6/20/2023  
**Purpose:** To ensure that access controls are implemented and in compliance with IT security policies, standards, and procedures.  
**Reference:** National Institute of Standards and Technology (NIST) Special Publications (SP): NIST SP 800-53a – Access Control (AC), NIST SP 800-12, NIST 800-46, NIST SP 800-48, NIST SP 800-77, NIST SP 800-94, NIST SP 800-97, NIST SP 800-100, NIST SP 800-113, NIST SP 800-114, NIST SP 800-121, NIST SP 800-124, NIST SP 800-164; NIST Federal Information Processing Standards (FIPS) 199/200  

**POLICY**  
1. **Account Management**
   - Identify and select the following types of information system accounts to support organizational missions and business functions: individual, shared, group, system, guest/anonymous, emergency, developer/manufacturer/vendor, temporary, and service.
   - Assign account managers for information system accounts.
2. **Access Enforcement**
   - Ensure that the information system enforces approved authorizations for logical access to information and system resources in accordance with applicable access control policies.
3. **Information Flow Enforcement**
   - Ensure that the information system enforces approved authorizations for controlling the flow of information within the system and between interconnected systems based on applicable policy.
4. **Separation of Duties**
   - Separate duties of individuals as necessary, to prevent malevolent activity without collusion.
   - Document the separation of duties of individuals.
5. **Least Privilege**
   - Employ the principle of least privilege, allowing only authorized access for users (or processes acting on behalf of users) which are necessary to accomplish assigned tasks in accordance with organizational missions and business functions.
   - Authorize explicitly access to hardware and software controlling access to systems and filtering rules for routers/firewalls, cryptographic key management information, configuration parameters for security services, and access control lists.
6. **Unsuccessful Logon Attempts**
   - Enforces a limit of consecutive invalid logon attempts by a user during three attempts.
   - Locks the account/node automatically for 3 minutes or until released by an administrator when the maximum number of unsuccessful attempts is exceeded.
7. **System Use Notification**
   - Displays to users an approved system use notification message or banner before granting access to the system that provides privacy and security notices consistent with applicable state and federal laws, directives, policies, regulations, standards, and guidance and states informing that:
   - Users are accessing only their system information system.
8. **Session Lock**
   - Prevent further access to the system by initiating a session lock after 3 hours of inactivity or upon receiving a request from a user.
   - Retain the session lock until the user re-establishes access using established identification and authentication procedures.
9. **Session Termination**
   - Ensure that the information system automatically terminates a user session after 3 failed attempts.
10. **Permitted Action Without Identification or Authentication**
   - Identify user actions that can be performed on the information system without identification or authentication consistent with organizational missions and business functions.
   - Document and provide supporting rationale in the security plan for the information system, user actions not requiring identification or authentication.

**COMPLIANCE**
Employees who violate this policy may be subject to appropriate disciplinary action up to and including discharge as well as both civil and criminal penalties. Non-employees, including, without limitation, contractors, may be subject to termination of contractual agreements, denial of access to IT resources, and other actions as well as both civil and criminal penalties.

## Step 3. Model (Architect) the access control policy

![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/2122d4b7-ca0c-4764-abf4-332405747ab1)


## Step 4. Test Plan

### 1. INTRODUCTION
This document is intended to outline the Radius Server Lab test strategy and overall test approach. This includes test methodologies, implementations, and specifications. The goal is to provide a working Radius Server on the virtualized network. As well as demonstrate framework that can be used by organizations and testers to plan and execute the necessary tests in a timely and cost-effective manner.

### 2. TESTABILITY
The Radius test is aimed to demonstrate the operations of the Radius Server. The following checklist provides a set of characteristics that leads to a testable software system:
- Operability
- Quality
- Stability
- Under stability

### 3. THE TEST PROCESS: THE PLAN, TEST SPECIFICATIONS, AND TEST RESULTS

#### 3.1 Test report
The test cases must be executed, and results must be reported. First, a test log should be made. A test log lists: the individual that ran it, when it was ran, and the results of the execution (pass or fail). Second, the report must include the effort made and the results achieved. And third, remember to evaluate the quality of the testing.

#### 3.2 Test Planning
The goals of test planning are to coordinate certain tests and make relevant decisions. These decisions are detailed in a test plan. These test plans should include how the test strategy and test plan apply to that testing and state any exceptions to them.

#### 3.3 Checking results
After test planning has been conducted, you will follow by checking the results. To start with, the versions of the software under test and test specifications being used need to be recorded. Then the actual outcomes should also be recorded. Finally, the actual outcomes should be compared against the expected outcome and any discrepancy found logged and analyzed. Acceptance Testing The final stage before taking the system into full operation is to let the customers and users check that the system fulfills their actual needs.

### 4. SOFTWARE REQUIREMENTS
The hardware components in the system are a Database Server, a Webserver, a client PC with a web browser.

### 5. Test Output fields

| Field Name          | Field Description                                                 |
|---------------------|--------------------------------------------------------------------|
| Server              | The IP address of the Radius server authenticated                    |
| UDP port            | The Radius server port utilized during the authentication test     |
| Source IP Address   | “Default” is shown if the IP address is the same as that of the Radius server. |
| Server Timeout      | The Radius server timeout period.                                   |
| Server retry count  | The number of authentication attempts allowed by the Radius server. |
| Secret              | The shared secret used for authentication with the Radius server.  |
| Client Username     | The username authenticated by the Radius server.                    |
| Client Password     | The user password authenticated by the Radius server                |
| Status              | The test result status (Accepted or Rejected) and the number of retransmits utilized during authentication. |

![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/e8c43849-42c2-4ba4-9305-0aaf0eae6da8)


### 6. PROJECT FUNCTIONS

**PROJECT IDENTIFICATION**
| Project Name | Project Number | Date Created |
|--------------|----------------|--------------|
| Radius Server| 3              | 6/22/22      |

**Program Manager**  


**Project Manager**  


**Test Manager**  


**Test Lead**  

![image](https://github.com/jmart375/Creating-a-specification-for-a-software-system/assets/91294710/2c073d85-7ef0-4b00-bbfb-524bd8e6ae1f)

### 6.1 TESTING TYPES

| Type of Test             | Will Test Be Performed? | Comments/Explanations                | Pass / Fail |
|--------------------------|--------------------------|--------------------------------------|-------------|
| Does VPN connect         | Yes                      |                                      |             |
| Are user groups enforced | Yes                      |                                      |             |
| Are explicit denies in place | Yes                   |                                      |             |
| Availability of radius authentication | Yes         |                                      |             |
| User authentication on radius | Yes                 |                                      |             |
| Review accounts for compliance | Yes                 |                                      |             |
| Usability                | Yes                      |                                      |             |
| Performance              | Yes                      |                                      |             |

### 7. VERIFICATION

**Verification**  
Will Verification Be Performed?  
Performed By  
Comments/Explanations  
Operability Review | Yes | No | TPL |

## References

1. [Radius Server Load Testing - A Guide](https://www.blazemeter.com/blog/radius-server-load-testing-a-guide) (2017, December 4). Retrieved June 24, 2022.
2. [Radius Server (radius authentication) and how it works](https://www.foxpass.com/blog/radius-server-and-how-it-works) - Bhatt, M. (2019, November 24). Retrieved June 22, 2022.
3. [5 Free Radius Server Testing and Monitoring Tools](https://www.serverwatch.com/guides/5-free-radius-server-testing-and-monitoring-tools/) (2016, February 17). Retrieved June 22, 2022.
