# C220-Part1e-Architecture Development Method

> 转换日期：2026-07-14  
> 原始文件：C220-Part1e-Architecture Development Method.pdf  
> 转换模式：text  
> 页码范围：[0, 152) / 152

---
<!-- page: 0 -->

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00000_img001.png)

## TOGAF® Standard —Architecture Development Method

## The Open Group Standard

<!-- page: 1 -->

*Table of Contents*

TOGAF® Standard — Architecture Development Method. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . ix Preface. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xi The Open Group. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xi The TOGAF® Standard. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xi The TOGAF Documentation. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xii This Document. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xii Intended Audience. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xii Trademarks. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xiii Acknowledgements. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xiv Referenced Documents. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . xv

1. Introduction. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1 1.1. ADM Overview. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1 1.1.1. The ADM, Enterprise Continuum, and Architecture Repository. . . . . . . . . . . . . . . . . . . . . . . . . 1 1.1.2. The ADM and the Foundation Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2 1.1.3. ADM and Supporting Guidelines and Techniques. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2

1.2. Architecture Development Cycle. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3 1.2.1. Key Points. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3 1.2.2. Basic Structure. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3 1.3. Adapting the ADM. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 5 1.4. Architecture Governance. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 7 1.5. Scoping the Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8 1.5.1. Breadth. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 9 1.5.2. Depth. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10 1.5.3. Time Period. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10 1.5.4. Architecture Domains. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 11 1.6. Architecture Alternatives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 12 1.6.1. Method. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 12 1.7. Architecture Integration. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13 1.8. Summary. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 14

2. Preliminary Phase. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 15 2.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16 2.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16 2.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16 2.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16 2.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17

2.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17 2.3.1. Scope the Enterprise Organizations Impacted. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18 2.3.2. Confirm Governance and Support Frameworks. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18

<!-- page: 2 -->

2.3.3. Define and Establish Enterprise Architecture Team and Organization. . . . . . . . . . . . . . . . . 18 2.3.4. Identify and Establish Architecture Principles. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 19 2.3.5. Tailor the TOGAF Framework and, if any, Other Selected Architecture Framework(s). . . 19 2.3.6. Develop a Strategy and Implementation Plan for Tools and Techniques. . . . . . . . . . . . . . . . 20 2.3.6.1. Issues in Tools Standardization. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20 2.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21 2.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22 2.5.1. Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 23 2.5.2. Organizational Context. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 23 2.5.3. Requirements for Architecture Work. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 24 2.5.4. Principles. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 24 2.5.5. Management Frameworks. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 25 2.5.6. Relating the Management Frameworks. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 26 2.5.7. Planning for Enterprise Architecture/Business Change Maturity Evaluation. . . . . . . . . . . . 27

3. Phase A: Architecture Vision. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 29 3.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 29 3.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 30 3.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 30 3.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 30 3.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 30

3.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 31 3.3.1. Establish the Architecture Project. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 31 3.3.2. Identify Stakeholders, Concerns, and Business Requirements. . . . . . . . . . . . . . . . . . . . . . . . . 31 3.3.3. Confirm and Elaborate Business Goals, Business Drivers, and Constraints. . . . . . . . . . . . . . 32 3.3.4. Evaluate Capabilities. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 33 3.3.5. Assess Readiness for Business Transformation. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 33 3.3.6. Define Scope. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34 3.3.7. Confirm and Elaborate Architecture Principles, including Business Principles. . . . . . . . . . 34 3.3.8. Develop Architecture Vision. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34 3.3.9. Define the Target Architecture Value Propositions and KPIs. . . . . . . . . . . . . . . . . . . . . . . . . . . 35 3.3.10. Identify the Business Transformation Risks and Mitigation Activities. . . . . . . . . . . . . . . . . 35 3.3.11. Develop Statement of Architecture Work; Secure Approval. . . . . . . . . . . . . . . . . . . . . . . . . . 36 3.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 37 3.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 38 3.5.1. General. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 38 3.5.2. Creating the Architecture Vision. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 38

4. Phase B: Business Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41 4.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41 4.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 42 4.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 42

<!-- page: 3 -->

4.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 42 4.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 42 4.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 43 4.3.1. Select Reference Models, Viewpoints, and Tools. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 44 4.3.1.1. Determine Overall Modeling Process. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 44 4.3.1.2. Identify Required Catalogs of Business Building Blocks. . . . . . . . . . . . . . . . . . . . . . . . . . . 45 4.3.1.3. Identify Required Matrices. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 45 4.3.1.4. Identify Required Diagrams. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 46 4.3.1.5. Identify Types of Requirement to be Collected. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 46 4.3.2. Develop Baseline Business Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 46 4.3.3. Develop Target Business Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 47 4.3.4. Perform Gap Analysis. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 47 4.3.5. Define Candidate Roadmap Components. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 47 4.3.6. Resolve Impacts Across the Architecture Landscape. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 47 4.3.7. Conduct Formal Stakeholder Review. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 48 4.3.8. Finalize the Business Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 48 4.3.9. Create/Update the Architecture Definition Document. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 48 4.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 48 4.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 50 4.5.1. General. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 50 4.5.2. Developing the Baseline Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 51 4.5.3. Applying Business Capabilities. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 51 4.5.4. Applying Value Streams. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 52 4.5.5. Applying the Organization Map. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 52 4.5.6. Applying Information Maps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 53 4.5.7. Applying Modeling Techniques. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 53 4.5.8. Architecture Repository. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 55

5. Phase C: Information Systems Architectures. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 56 5.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 57 5.2. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 57

6. Phase C: Information Systems Architectures — Data Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58 6.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58 6.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58 6.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58 6.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58 6.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58

6.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 59 6.3.1. Select Reference Models, Viewpoints, and Tools. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 60 6.3.1.1. Determine Overall Modeling Process. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 61 6.3.1.2. Identify Required Catalogs of Data Building Blocks. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 61

<!-- page: 4 -->

6.3.1.3. Identify Required Matrices. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 62 6.3.1.4. Identify Required Diagrams. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 62 6.3.1.5. Identify Types of Requirement to be Collected. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 62 6.3.2. Develop Baseline Data Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 63 6.3.3. Develop Target Data Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 63 6.3.4. Perform Gap Analysis. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 63 6.3.5. Define Candidate Roadmap Components. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 64 6.3.6. Resolve Impacts Across the Architecture Landscape. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 64 6.3.7. Conduct Formal Stakeholder Review. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 64 6.3.8. Finalize the Data Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 65 6.3.9. Create/Update the Architecture Definition Document. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 65 6.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 65 6.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 66 6.5.1. Data Structure. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 66 6.5.2. Key Considerations for Data Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 67 6.5.2.1. Data Management. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 67 6.5.2.2. Data Migration. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 68 6.5.2.3. Data Governance. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 68 6.5.3. Architecture Repository. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 68

7. Phase C: Information Systems Architectures — Application Architecture. . . . . . . . . . . . . . . . . . . . . . 69 7.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 69 7.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 69 7.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 69 7.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 69 7.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 69

7.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 70 7.3.1. Select Reference Models, Viewpoints, and Tools. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 71 7.3.1.1. Determine Overall Modeling Process. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 71 7.3.1.2. Identify Required Catalogs of Application Building Blocks. . . . . . . . . . . . . . . . . . . . . . . . 72 7.3.1.3. Identify Required Matrices. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 73 7.3.1.4. Identify Required Diagrams. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 73 7.3.1.5. Identify Types of Requirement to be Collected. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 74 7.3.2. Develop Baseline Application Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 74 7.3.3. Develop Target Application Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 74 7.3.4. Perform Gap Analysis. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 75 7.3.5. Define Candidate Roadmap Components. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 75 7.3.6. Resolve Impacts Across the Architecture Landscape. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 75 7.3.7. Conduct Formal Stakeholder Review. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 76 7.3.8. Finalize the Application Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 76 7.3.9. Create/Update the Architecture Definition Document. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 76

<!-- page: 5 -->

7.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 77 7.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 78 7.5.1. Architecture Repository. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 78

8. Phase D: Technology Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 79 8.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 79 8.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 80 8.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 80 8.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 80 8.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 80

8.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 81 8.3.1. Select Reference Models, Viewpoints, and Tools. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 82 8.3.1.1. Determine Overall Modeling Process. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 82 8.3.1.2. Identify Required Catalogs of Technology Building Blocks. . . . . . . . . . . . . . . . . . . . . . . . 83 8.3.1.3. Identify Required Matrices. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 84 8.3.1.4. Identify Required Diagrams. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 84 8.3.1.5. Identify Types of Requirement to be Collected. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 85 8.3.1.6. Select Services. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 85 8.3.2. Develop Baseline Technology Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 86 8.3.3. Develop Target Technology Architecture Description. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 86 8.3.4. Perform Gap Analysis. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 87 8.3.5. Define Candidate Roadmap Components. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 87 8.3.6. Resolve Impacts Across the Architecture Landscape. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 87 8.3.7. Conduct Formal Stakeholder Review. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 87 8.3.8. Finalize the Technology Architecture. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 88 8.3.9. Create/Update the Architecture Definition Document. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 88 8.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 88 8.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 89 8.5.1. Emerging Technologies. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 89 8.5.2. Architecture Repository. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 90

9. Phase E: Opportunities & Solutions. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 91 9.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 91 9.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 92 9.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 92 9.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 92 9.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 92

9.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 93 9.3.1. Determine/Confirm Key Corporate Change Attributes. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 94 9.3.2. Determine Business Constraints for Implementation. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 94 9.3.3. Review and Consolidate Gap Analysis Results from Phases B to D. . . . . . . . . . . . . . . . . . . . . 94 9.3.4. Review Consolidated Requirements Across Related Business Functions. . . . . . . . . . . . . . . . 95

<!-- page: 6 -->

9.3.5. Consolidate and Reconcile Interoperability Requirements. . . . . . . . . . . . . . . . . . . . . . . . . . . . 95 9.3.6. Refine and Validate Dependencies. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 96 9.3.7. Confirm Readiness and Risk for Business Transformation. . . . . . . . . . . . . . . . . . . . . . . . . . . . 96 9.3.8. Formulate Implementation and Migration Strategy. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 96 9.3.9. Identify and Group Major Work Packages. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 97 9.3.10. Identify Transition Architectures. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 97 9.3.11. Create the Architecture Roadmap & Implementation and Migration Plan. . . . . . . . . . . . . 97 9.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 98 9.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 100

10. Phase F: Migration Planning. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 101 10.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 102 10.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 102 10.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 102 10.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 102 10.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 102

10.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 104 10.3.1. Confirm Management Framework Interactions for the Implementation and Migration Plan. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 104 10.3.2. Assign a Business Value to Each Work Package. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 105 10.3.3. Estimate Resource Requirements, Project Timings, and Availability/Delivery Vehicle. 106 10.3.4. Prioritize the Migration Projects by Conducting a Cost/Benefit Assessment and Risk Assessment. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 106 10.3.5. Confirm Architecture Roadmap and Update Architecture Definition Document. . . . . . 106 10.3.6. Complete the Implementation and Migration Plan. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 107 10.3.7. Complete the Architecture Development Cycle and Document Lessons Learned. . . . . . 107 10.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 107 10.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 108

11. Phase G: Implementation Governance. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 110 11.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 111 11.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 111 11.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 111 11.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 111 11.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 111

11.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 112 11.3.1. Confirm Scope and Priorities for Deployment with Development Management. . . . . . . 113 11.3.2. Identify Deployment Resources and Skills. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 113 11.3.3. Guide Development of Solutions Deployment. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 113 11.3.4. Perform Enterprise Architecture Compliance Reviews. . . . . . . . . . . . . . . . . . . . . . . . . . . . . 114 11.3.5. Implement Business and IT Operations. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 114 11.3.6. Perform Post-Implementation Review and Close the Implementation. . . . . . . . . . . . . . . . 114

<!-- page: 7 -->

11.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 114 11.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 115

12. Phase H: Architecture Change Management. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 117 12.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 118 12.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 118 12.2.1. Reference Materials External to the Enterprise. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 118 12.2.2. Non-Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 118 12.2.3. Architectural Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 118

12.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 120 12.3.1. Establish Value Realization Process. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 120 12.3.2. Deploy Monitoring Tools. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 120 12.3.3. Manage Risks. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 120 12.3.4. Provide Analysis for Architecture Change Management. . . . . . . . . . . . . . . . . . . . . . . . . . . . 121 12.3.5. Develop Change Requirements to Meet Performance Targets. . . . . . . . . . . . . . . . . . . . . . . 121 12.3.6. Manage Governance Process. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 121 12.3.7. Activate the Process to Implement Change. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 121 12.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 121 12.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 122 12.5.1. Drivers for Change. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 123 12.5.2. Enterprise Architecture Change Management Process. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 125 12.5.3. Guidelines for Maintenance versus Architecture Redesign. . . . . . . . . . . . . . . . . . . . . . . . . . 126

13. ADM Architecture Requirements Management. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 127 13.1. Objectives. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 128 13.2. Inputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 128 13.3. Steps. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 129 13.4. Outputs. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 131 13.5. Approach. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 132 13.5.1. General. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 132 13.5.2. Requirements Development. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 133 13.5.3. Resources. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 133 13.5.3.1. Business Scenarios. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 134 13.5.3.2. Requirements Tools. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 134

Index. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 135

<!-- page: 8 -->

## TOGAF® Standard — Architecture Development Method

The Open Group Standard

<!-- page: 9 -->

Copyright © 2005 - 2025, The Open Group All rights reserved.

No part of this publication may be reproduced, stored in a retrieval system, or transmitted, in any form or by any means, electronic, mechanical, photocopying, recording, or otherwise, without the prior permission of the copyright owners. Specifically, without such written permission, the use or incorporation of this publication, in whole or in part, is NOT PERMITTED for the purposes of training or developing large language models (LLMs) or any other generative artificial intelligence systems, or otherwise for the purposes of using, or in connection with the use of, such technologies, tools, or models to generate any data or content and/or to synthesize or combine with any other data or content.

Any use of this publication for commercial purposes is subject to the terms of the Annual Commercial License relating to it. For further information, see www.opengroup.org/legal/licensing.

The Open Group Standard TOGAF® Standard — Architecture Development Method ISBN: 1-947754-90-4 Document Number: C220

Published by The Open Group, April 2022. Updated May 2025 to include Technical Corrigendum 1

Comments relating to the material contained in this document may be submitted to: The Open Group, Apex Plaza, Forbury Road, Reading, Berkshire, RG1 1AX, United Kingdom or by electronic mail to: ogspecs@opengroup.org

Built with asciidoctor, version 2.0.18. Backend: pdf Build date: 2025-06-02 17:44:36 +0100

<!-- page: 10 -->

## Preface

## The Open Group

The Open Group is a global consortium that enables the achievement of business objectives through technology standards and open source initiatives by fostering a culture of collaboration, inclusivity, and mutual respect among our diverse group of 900+ memberships. Our membership includes customers, systems and solutions suppliers, tool vendors, integrators, academics, and consultants across multiple industries.

The mission of The Open Group is to drive the creation of Boundaryless Information FlowTM achieved by:

- Working with customers to capture, understand, and address current and emerging requirements, establish policies, and share best practices

- Working with suppliers, consortia, and standards bodies to develop consensus and facilitate interoperability, to evolve and integrate specifications and open source technologies

- Offering a comprehensive set of services to enhance the operational efficiency of consortia

- Developing and operating the industry’s premier certification service and encouraging procurement of certified products

Further information on The Open Group is available at www.opengroup.org.

The Open Group publishes a wide range of technical documentation, most of which is focused on development of standards and guides, but which also includes white papers, technical studies, certification and testing documentation, and business titles. Full details are available at www.opengroup.org/library.

## The TOGAF® Standard

The TOGAF® Standard is an open, industry consensus framework for Enterprise Architecture.

It is a foundational framework, which means that it is applicable to the development of any kind of architecture in any context. This foundational framework is supplemented by The Open Group TOGAF Library, a publicly-accessible resource with an extensive and growing portfolio of guidance material, providing practical guidance in the application of the TOGAF framework in specific contexts; refer to: www.opengroup.org/togaf-library.

<!-- page: 11 -->

## The TOGAF Documentation

The TOGAF documentation consists of a set of documents:

- The TOGAF Standard, which describes the generally applicable approach to Enterprise and IT Architecture

- The TOGAF Library, a portfolio of additional guidance material, which supports the practical application of the TOGAF approach

## This Document

This document is the TOGAF® Standard — Architecture Development Method.

It has been developed and approved by The Open Group.

## Intended Audience

The TOGAF Standard is intended for Enterprise Architects, Business Architects, IT Architects, Data Architects, Systems Architects, Solution Architects, and anyone responsible for the architecture function within an organization.

<!-- page: 12 -->

## Trademarks

ArchiMate, FACE, FACE logo, Future Airborne Capability Environment, Making Standards Work, Open Footprint, Open O logo, Open O and Check certification logo, Open Subsurface Data Universe, OSDU, SOSA, SOSA logo, The Open Group, TOGAF, UNIX, UNIXWARE, and X logo are registered trademarks and Boundaryless Information Flow, Build with Integrity Buy with Confidence, Commercial Aviation Reference Architecture, Dependability Through Assuredness, Digital Practitioner Body of Knowledge, DPBoK, EMMM, FHIM Profile Builder, FHIM logo, FPB, IT4IT, IT4IT logo, O-AA, O-DA, O-DEF, O-HERA, O- PAS, O-TTPS, O-VBA, Open Agile Architecture, Open FAIR, Open Process Automation, Open Trusted Technology Provider, Sensor Integration Simplified, and Sensor Open Systems Architecture are trademarks of The Open Group.

COBIT is a registered trademark of the Information Systems Audit and Control Association (ISACA) and the IT Governance Institute.

ITIL and PRINCE2 are registered trademarks of AXELOS Limited.

MDA, Model-Driven Architecture, Object Management Group, OMG, and UML are registered trademarks and BPMN, Business Process Model and Notation, and Unified Modeling Language are trademarks of the Object Management Group.

Zachman is a registered trademark of Zachman International, Inc.

The Open Group acknowledges that there may be other company names and products that might be covered by trademark protection and advises the reader to verify them independently.

<!-- page: 13 -->

## Acknowledgements

The Open Group is grateful for the contribution of many individuals and organizations in the development of the TOGAF Standard. See the TOGAF Standard — Introduction and Core Concepts for details.

<!-- page: 14 -->

## Referenced Documents

Please refer to the TOGAF Standard — Introduction and Core Concepts, Appendix A for documents referenced in the TOGAF Standard.

<!-- page: 15 -->



<!-- page: 16 -->

## 1. Introduction

This chapter introduces the Architecture Development Method (ADM) cycle, adapting the ADM, architecture scope, and architecture integration.

### 1.1. ADM Overview

The TOGAF® ADM describes a method for developing and managing the lifecycle of an Enterprise Architecture, and forms the core of the TOGAF Standard.

It integrates elements of the TOGAF Standard, as well as other available architectural assets, to meet the business needs of an organization.

#### 1.1.1. The ADM, Enterprise Continuum, and Architecture Repository

The Enterprise Continuum provides a framework and context to support the leverage of relevant architecture assets in executing the ADM. These assets may include Architecture Descriptions, models, and patterns taken from a variety of sources, as explained in the TOGAF Standard — Architecture Content.

The Enterprise Continuum categorizes architectural source material — both the contents of the organization’s own enterprise repositories and the set of relevant, available reference models and standards in the industry.

The practical implementation of the Enterprise Continuum will typically take the form of an Architecture Repository (see the TOGAF Standard — Architecture Content) that includes reference architectures, models, and patterns that have been accepted for use within the enterprise, and actual architectural work done previously within the enterprise. The architect would seek to re-use as much as possible from the Architecture Repository that was relevant to the project in hand. (In addition to the collection of architecture source material, the repository would also contain architecture development work-in-progress.)

At relevant places throughout the ADM there are reminders to consider which, if any, architecture assets from the Architecture Repository the architect should use. In some cases — for example, in the development of a Technology Architecture — this may be the TOGAF Foundation Architecture. In other cases — for example, in the development of a Business Architecture — it may be a reference model for e-Commerce taken from the industry at large.

The criteria for including source materials in an organization’s Architecture Repository will typically form part of the Enterprise Architecture Governance process. These governance processes should consider available resources both within and outside the enterprise in order to determine when general resources can be adapted for specific enterprise needs and also to determine where specific solutions can be generalized to support wider re-use.

<!-- page: 17 -->

While using the ADM, the architect is developing a snapshot of the enterprise’s decisions and their implications at particular points in time. Each iteration of the ADM will populate an organizationspecific landscape with all the architecture assets identified and leveraged through the process, including the final organization-specific architecture delivered.

Architecture development is a continuous, cyclical process, and in executing the ADM repeatedly over time, the architect gradually adds more and more content to the organization’s Architecture Repository. Although the primary focus of the ADM is on the development of the enterprise-specific architecture, in this wider context the ADM can also be viewed as the process of populating the enterprise’s own Architecture Repository with relevant re-usable building blocks taken from the “left”, more generic side of the Enterprise Continuum.

In fact, the first execution of the ADM will often be the hardest, since the architecture assets available for re-use will be relatively scarce. Even at this stage of development, however, there will be architecture assets available from external sources such as the TOGAF Standard, as well as the IT industry at large, that could be leveraged in support of the effort.

Subsequent executions will be easier as more and more architecture assets become identified, are used to populate the organization’s Architecture Repository, and are thus available for future re-use.

#### 1.1.2. The ADM and the Foundation Architecture

The ADM is also useful to populate the Foundation Architecture of an enterprise. Business requirements of an enterprise may be used to identify the necessary definitions and selections in the Foundation Architecture. This could be a set of re-usable common models, policy and governance definitions, or even as specific as overriding technology selections (e.g., if mandated by law). Population of the Foundation Architecture follows similar principles as for an Enterprise Architecture, with the difference that requirements for a whole enterprise are restricted to the overall concerns and thus less complete than for a specific enterprise.

It is important to recognize that existing models from these various sources, when integrated, may not necessarily result in a coherent Enterprise Architecture. “Integratability” of Architecture Descriptions is considered in Section 1.7.

#### 1.1.3. ADM and Supporting Guidelines and Techniques

The application of the TOGAF ADM is supported by an extended set of resources — guidelines, templates, checklists, and other detailed materials. These are included in:

- The TOGAF Standard — ADM Techniques

- TOGAF Series Guides — the Guidance part of the Standard (guidance material on how to use and adapt the TOGAF Standard for specific needs)

- White Papers and Guides published by The Open Group, classified and referenced in the TOGAF Library (see www.opengroup.org/togaf-library)

<!-- page: 18 -->

The individual guidelines and techniques are described separately so that they can be referenced from the relevant points in the ADM as necessary, rather than having the detailed text clutter the description of the ADM itself.

### 1.2. Architecture Development Cycle

#### 1.2.1. Key Points

The following are the key points about the ADM:

- The ADM is iterative, over the whole process, between phases, and within phases (see the TOGAF Standard — ADM Techniques)

- For each iteration of the ADM, a fresh decision must be taken as to:

- The breadth of coverage of the enterprise to be defined

- The level of detail to be defined

- The extent of the time period aimed at, including the number and extent of any intermediate time periods

- The architectural assets to be leveraged, including:

  - Assets created in previous iterations of the ADM cycle within the enterprise

- Assets available elsewhere in the industry (other frameworks, systems models, vertical industry models, etc.)

- These decisions should be based on a practical assessment of resource and competence availability, and the value that can realistically be expected to accrue to the enterprise from the chosen scope of the architecture work

- As a generic method, the ADM is intended to be used by enterprises in a wide variety of different geographies and applied in different vertical sectors/industry types

As such, it may be, but does not necessarily have to be, tailored to specific needs. For example, it may be used in conjunction with the set of deliverables of another framework, where these have been deemed to be more appropriate for a specific organization. (For example, many US Federal agencies have developed individual frameworks that define the deliverables specific to their particular departmental needs.)

These issues are considered in detail in Section 1.3.

#### 1.2.2. Basic Structure

The basic structure of the ADM is shown in Figure 1-1.

Throughout the ADM cycle, there needs to be frequent validation of results against the original expectations, both those for the whole ADM cycle, and those for the particular phase of the process.

<!-- page: 19 -->

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00019_img001.png)

*Figure 1-1. Architecture Development Cycle*

The phases of the ADM cycle are further divided into steps, which are defined in the detailed description of each phase.

The Requirements Management phase is a continuous phase which ensures that any changes to requirements are handled through appropriate governance processes and reflected in all other phases. An enterprise may choose to record all new requirements, including those which are in scope of the current Statement of Architecture Work through a single Requirements Repository.

The phases of the cycle are described in detail in the following chapters.

Note that output is generated throughout the process, and that the output from an early phase may be modified in a later phase. In the ADM, the status of outputs at each stage is defined. The lifecycle of outputs must be managed through a version numbering policy, adapted by the architect to meet the

<!-- page: 20 -->

requirements of the organization and to work with the architecture tools and repositories employed by the organization.

In the ADM, documents which are under development and have not undergone any formal review and approval process are designated “draft”. Documents which have been reviewed and approved are designated “approved” in accordance with the organization’s governance practices. Approved does not necessarily mean finalized. Documents may evolve during subsequent phases but may only be changed through an appropriate change control and governance process. This is used in particular within the ADM to illustrate the evolution of Baseline and Target Architecture Definitions.

### 1.3. Adapting the ADM

The ADM is a generic method for architecture development, which is designed to deal with most system and organizational requirements. However, it will often be necessary to modify or extend the ADM to suit specific needs. One of the tasks before applying the ADM is to review its components for applicability, and then tailor them as appropriate to the circumstances of the individual enterprise. This activity may well produce an “enterprise-specific” ADM.

One reason for wanting to adapt the ADM, which it is important to stress, is that the order of the phases in the ADM is to some extent dependent on the maturity of the architecture discipline within the enterprise. For example, if the business case for doing architecture at all is not well recognized, then creating an Architecture Vision is almost always essential; and a detailed Business Architecture often needs to come next, in order to underpin the Architecture Vision, detail the business case for remaining architecture work, and secure the active participation of key stakeholders in that work. In other cases a slightly different order may be preferred; for example, a detailed inventory of the baseline environment may be done before undertaking the Business Architecture.

The order of phases may also be defined by the Architecture Principles and business principles of an enterprise. For example, the business principles may dictate that the enterprise be prepared to adjust its business processes to meet the needs of a packaged solution, so that it can be implemented quickly to enable a fast response to market changes. In such a case, the Business Architecture (or at least the completion of it) may well follow completion of the Information Systems Architecture or the Technology Architecture.

Another reason for wanting to adapt the ADM is if the TOGAF framework is to be integrated with another enterprise framework (as explained in the TOGAF Standard — Introduction and Core Concepts). For example, an enterprise may wish to use the TOGAF framework and its generic ADM in conjunction with the Zachman® Framework, or another Enterprise Architecture framework that has a defined set of deliverables specific to a particular vertical sector: Government, Defense, e-Business, Telecommunications, etc. The ADM has been specifically designed with this potential integration in mind.

<!-- page: 21 -->

Other possible reasons for wanting to adapt the ADM include:

- The ADM is one of the many corporate processes that make up the corporate governance model

It is complementary to, and supportive of, other standard program management processes, such as those for authorization, risk management, business planning and budgeting, development planning, systems development, and procurement.

- The ADM is being mandated for use by a prime or lead contractor in an outsourcing situation, and needs to be tailored to achieve a suitable compromise between the contractor’s existing practices and the contracting enterprise’s requirements

- The enterprise is a small-to-medium enterprise, and wishes to use a “cut-down” method more attuned to the reduced level of resources and system complexity typical of such an environment

- The enterprise is very large and complex, comprising many separate but interlinked “enterprises” within an overall collaborative business framework, and the architecture method needs to be adapted to recognize this

- Different approaches to planning and integration may be used in such cases, including the following (possibly in combination):

- Top-down planning and development — designing the whole interconnected meta-enterprise as a single entity (an exercise that typically stretches the limits of practicality)

- Development of a “generic” or “reference” architecture, typical of the enterprises within the organization, but not representing any specific enterprise, which individual enterprises are then expected to adapt in order to produce an architecture “instance” suited to the particular enterprise concerned

- Replication — developing a specific architecture for one enterprise, implementing it as a proofof-concept, and then taking that as a “reference architecture” to be cloned in other enterprises

- In a vendor or production environment, a generic architecture for a family of related products is often referred to as a “Product Line Architecture”, and the analogous process to that outlined above is termed “(Architecture-based) Product Line Engineering”. The ADM is targeted primarily at architects in IT user enterprises, but a vendor organization whose products are IT-based might well wish to adapt it as a generic method for a Product Line Architecture development.

The descriptions of the phases of the ADM contain lists of deliverables and artifacts that could be applicable to any enterprise. It is important to adapt deliverables and artifacts to reflect the specific needs of the enterprise for the required architecture.

Adapting the Content Framework and Enterprise Metamodel, which defines the organization-specific deliverables and artifacts, together with detailed descriptions of the specific deliverables and artifacts referenced in the ADM phase descriptions may be found in the TOGAF Standard — Architecture Content.

<!-- page: 22 -->

The ADM can also be adapted to support an Agile Enterprise Architecture delivery style as well as to enable enterprise agility. Detailed guidance on how to adapt the ADM may be found in the following documents:

- TOGAF® Series Guide: Enabling Enterprise Agility

- TOGAF® Series Guide: Applying the TOGAF® ADM using Agile Sprints

Additional guidance on adapting the ADM process may be found in the TOGAF Standard — Applying the ADM, and also in the TOGAF® Series Guide: A Practitioners’ Approach to Developing Enterprise Architecture Following the TOGAF® ADM.

### 1.4. Architecture Governance

The ADM, whether adapted by the organization or used as documented here, is a key process to be managed in the same manner as other architecture artifacts classified through the Enterprise Continuum and held in the Architecture Repository. The Architecture Board should be satisfied that the method is being applied correctly across all phases of an architecture development iteration. Compliance with the ADM is fundamental to the governance of the architecture, to ensure that all considerations are made and all required deliverables are produced.

The management of all architectural artifacts, governance, and related processes should be supported by a controlled environment. Typically, this would be based on one or more repositories supporting versioned objects, process control, and status.

The major information areas managed by a governance repository should contain the following types of information:

- Reference Data (collateral from the organization’s own repositories/Enterprise Continuum, including external data; e.g., COBIT®, the IT4IT Reference Architecture): used for guidance and instruction during project implementation

This includes the details of information outlined above. The reference data includes a description of the governance procedures themselves.

- Process Status: all information regarding the state of any governance processes will be managed

Examples of this include outstanding compliance requests, dispensation requests, and compliance assessments investigations.

- Audit Information: this will record all completed governance process actions and will be used to support:

- Key decisions and responsible personnel for any architecture project that has been sanctioned by the governance process

- A reference for future architectural and supporting process developments, guidance, and precedence

<!-- page: 23 -->

The governance artifacts and process are themselves part of the contents of the Architecture Repository.

Architecture Governance is addressed in detail in the TOGAF Standard — EA Capability and Governance.

### 1.5. Scoping the Architecture

There are many reasons to constrain (or restrict) the scope of the architectural activity to be undertaken, most of which relate to limits in:

- The organizational authority of the team producing the architecture

- The objectives and stakeholder concerns to be addressed within the architecture

- The availability of people, finance, and other resources

The scope chosen for the architecture activity should ideally allow the work of all architects within the enterprise to be effectively governed and integrated. This requires a set of aligned “architecture partitions” that ensure architects are not working on duplicate or conflicting activities. It also requires the definition of re-use and compliance relationships between architecture partitions.

The division of the enterprise and its architecture-related activity is discussed in more detail in the TOGAF Standard — Applying the ADM.

Four dimensions are typically used in order to define and limit the scope of an architecture:

- Breadth: what is the full extent of the enterprise, and what part of that extent will this architecting effort deal with?

- Many enterprises are very large, effectively comprising a federation of organizational units that could validly be considered enterprises in their own right

- The modern enterprise increasingly extends beyond its traditional boundaries, to embrace a fuzzy combination of traditional business enterprise combined with suppliers, customers, and partners

- Depth: to what level of detail should the architecting effort go?

How much architecture is “enough”? What is the appropriate demarcation between the architecture effort and other, related activities (system design, system engineering, system development)?

- Time Period: what is the time period that needs to be articulated for the Architecture Vision, and does it make sense (in terms of practicality and resources) for the same period to be covered in the detailed Architecture Description?

If not, how many Transition Architectures are to be defined, and what are their time periods?

<!-- page: 24 -->

- Architecture Domains: a complete Enterprise Architecture Description should contain all four architecture domains (Business, Data, Application, Technology), but the realities of resource and time constraints often mean there is not enough time, funding, or resources to build a top-down, all-inclusive Architecture Description encompassing all four architecture domains, even if the enterprise scope is chosen to be less than the full extent of the overall enterprise

Typically, the scope of an architecture is first expressed in terms of breadth, depth, and time. Once these dimensions are understood, a suitable combination of architecture domains can be selected that are appropriate to the problem being addressed. Techniques for using the ADM to develop a number of related architectures are discussed in the TOGAF Standard — Applying the ADM.

The four dimensions of architecture scope are explored in detail below. In each case, particularly in large-scale environments where architectures are necessarily developed in a federated manner, there is a danger of architects optimizing within their own scope of activity, instead of at the level of the overall enterprise. It is often necessary to sub-optimize in a particular area, in order to optimize at the enterprise level. The aim should always be to seek the highest level of commonality and focus on scalable and re-usable modules in order to maximize re-use at the enterprise level.

#### 1.5.1. Breadth

One of the key decisions is the focus of the architecture effort, in terms of the breadth of overall enterprise activity to be covered (which specific business sectors, functions, organizations, geographical areas, etc.).

It is often necessary to have a number of different architectures existing across an enterprise, focused on particular timeframes, business functions, or business requirements.

For large complex enterprises, federated architectures — independently developed, maintained, and managed architectures that are subsequently integrated within an integration framework — are typical. Such a framework specifies the principles for interoperability, migration, and conformance. This allows specific business units to have architectures developed and governed as stand-alone architecture projects. More details and guidance on specifying the interoperability requirements for different solutions can be found in the TOGAF Standard — ADM Techniques.

The feasibility of a single enterprise-wide architecture for every business function or purpose may be rejected as too complex and unwieldy. In these circumstances it is suggested that a number of different Enterprise Architectures exist across an enterprise. These Enterprise Architectures focus on particular timeframes, business segments or functions, and specific organizational requirements. In such a case we need to create the overarching Enterprise Architecture as a “federation” of these Enterprise Architectures. An effective way of managing and exploiting these Enterprise Architectures is to adopt a publish-and-subscribe model that allows architecture to be brought under a governance framework. In such a model, architecture developers and architecture consumers in projects (the supply and demand sides of architecture work) sign up to a mutually beneficial framework of governance that ensures that:

<!-- page: 25 -->

- Architectural material is of good quality, up-to-date, fit-for-purpose, and published (reviewed and agreed to be made public)

- Usage of architecture material can be monitored, and compliance with standards, models, and principles can be exhibited, via:

- A Compliance Assessment process that describes what the user is subscribing to, and assesses their level of compliance

- A dispensation process that may grant dispensations from adherence to architecture standards and guidelines in specific cases (usually with a strong business imperative)

Publish and subscribe techniques are being developed as part of general IT governance and specifically for the Defense sphere.

#### 1.5.2. Depth

Care should be taken to judge the appropriate level of detail to be captured, based on the intended use of the Enterprise Architecture and the decisions to be made based on it. It is important that a consistent and equal level of depth be completed in each architecture domain (Business, Data, Application, Technology) included in the architecture effort. If pertinent detail is omitted, the architecture may not be useful. If unnecessary detail is included, the architecture effort may exceed the time and resources available, and/or the resultant architecture may be confusing or cluttered. Developing architectures at different levels of detail within an enterprise is discussed in more detail in the TOGAF Standard — Applying the ADM.

It is also important to predict the future uses of the architecture so that, within resource limitations, the architecture can be structured to accommodate future tailoring, extension, or re-use. The depth and detail of the Enterprise Architecture needs to be sufficient for its purpose, and no more.

Iterations of the ADM will build on the artifacts and the capabilities created during previous iterations.

There is a need to document all the models in an enterprise, to the level of detail appropriate to the need of the current ADM cycle. The key is to understand the status of the enterprise’s architecture work, and what can realistically be achieved with the resources and competencies available, and then focus on identifying and delivering the value that is achievable. Stakeholder value is a key focus: too broad a scope may deter some stakeholders (no return on investment).

#### 1.5.3. Time Period

The ADM is described in terms of a single cycle of Architecture Vision, and a set of Target Architectures (Business, Data, Application, Technology) that enable the implementation of the vision.

In such cases, a wider view may be taken, whereby an enterprise is represented by several different architecture instances (for example, strategic, segment, capability), each representing the enterprise at a particular point in time. One architecture instance will represent the current enterprise state (the “as-is”, or baseline). Another architecture instance, perhaps defined only partially, will represent the ultimate target end-state (the “vision”). In-between, intermediate or “Transition Architecture”

<!-- page: 26 -->

instances may be defined, each comprising its own set of Target Architecture Descriptions. An example of how this might be achieved is given in the TOGAF Standard — ADM Techniques.

By this approach, the Target Architecture work is split into two or more discrete stages:

1. First, develop Target Architecture Descriptions for the overall (large-scale) system, demonstrating a response to stakeholder objectives and concerns for a relatively distant timeframe (for example, a six-year period)

2. Then develop one or more “Transition Architecture” descriptions, as increments or plateaus, each in line with and converging on the Target Architecture Descriptions, and describing the specifics of the increment concerned

In such an approach, the Target Architectures are evolutionary in nature, and require periodic review and update according to evolving business requirements and developments in technology, whereas the Transition Architectures are (by design) incremental in nature, and in principle should not evolve during the implementation phase of the increment, in order to avoid the “moving target” syndrome. This, of course, is only possible if the implementation schedule is under tight control and relatively short (typically less than two years).

The Target Architectures remain relatively generic, and are therefore less vulnerable to obsolescence than the Transition Architectures. They embody only the key strategic architectural decisions, which should be blessed by the stakeholders from the outset, whereas the detailed architectural decisions in the Transition Architectures are deliberately postponed as far as possible (i.e., just before implementation) in order to improve responsiveness vis a vis new technologies and products.

The enterprise evolves by migrating to each of these Transition Architectures in turn. As each Transition Architecture is implemented, the enterprise achieves a consistent, operational state on the way to the ultimate vision. However, this vision itself is periodically updated to reflect changes in the business and technology environment, and in effect may never actually be achieved, as originally described. The whole process continues for as long as the enterprise exists and continues to change.

Such a breakdown of the Architecture Description into a family of related architecture products of course requires effective management of the set and their relationships.

#### 1.5.4. Architecture Domains

A complete Enterprise Architecture should address all four architecture domains (Business, Data, Application, Technology), but the realities of resource and time constraints often mean there is not enough time, funding, or resources to build a top-down, all-inclusive Architecture Description encompassing all four architecture domains.

Architecture Descriptions will normally be built with a specific purpose in mind — a specific set of business drivers that drive the architecture development — and clarifying the specific issue(s) that the Architecture Description is intended to help explore, and the questions it is expected to help answer, is an important part of the initial phase of the ADM.

<!-- page: 27 -->

For example, if the purpose of a particular architecture effort is to define and examine technology options for achieving a particular capability, and the fundamental business processes are not open to modification, then a full Business Architecture may well not be warranted. However, because the Data, Application, and Technology Architectures build on the Business Architecture, the Business Architecture still needs to be thought through and understood.

While circumstances may sometimes dictate building an Architecture Description not containing all four architecture domains, it should be understood that such an architecture cannot, by definition, be a complete Enterprise Architecture. One of the risks is a lack of consistency and therefore an ability to integrate. Integration either needs to come later — with its own costs and risks — or the risks and trade-offs involved in not developing a complete and integrated architecture need to be articulated by the architect, and communicated to and understood by the enterprise management.

### 1.6. Architecture Alternatives

There is often more than one possible Target Architecture that would conform to the Architecture Vision, Architecture Principles, and Requirements. It is important to identify alternative Target Architectures and build understanding of different possibilities and identify trade-offs between the alternatives. Creating an architecture normally requires trade-offs among competing forces. Presenting different alternatives and trade-offs to stakeholders helps architects to extract hidden agendas, principles, and requirements that could impact the final Target Architecture.

#### 1.6.1. Method

It is most common that a single alternative does not exist that will meet all stakeholders’ concerns. The TOGAF Standard (see the TOGAF Standard — ADM Techniques: Architecture Alternatives and Tradeoffs) provides a technique to investigate different alternatives and to discuss these with the stakeholders.

Commonly, alternatives are defined per domain. This is done to simplify the analysis of the different alternatives. Of course, the alternatives per domain can be merged into on overall analysis of the alternatives for the whole architecture. This approach is illustrated in Figure 1-2.

The first part of the method uses the vision, principles, requirements, and other information to select sets of criteria fitting for different alternatives.

The second part of the method defines alternatives based on the criteria and builds an understanding of each.

The third part of the method will either select one of the alternatives, or else combine features from more than one, to create the proposed alternative. Perform the following activities in just enough detail to support that decision. The method can be used for any phase at any level of an architecture.

<!-- page: 28 -->

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00028_img001.png)

*Figure 1-2. Architecture Alternatives Method*

### 1.7. Architecture Integration

Architectures that are created to address a subset of issues within an enterprise require a consistent frame of reference so that they can be considered as a group as well as point deliverables. The dimensions that are used to define the scope boundary of a single architecture (e.g., level of detail, architecture domain, etc.) are typically the same dimensions that must be addressed when considering the integration of many architectures. Figure 1-3 illustrates how different types of architecture need to co-exist.

At the present time, the state of the art is such that architecture integration can be accomplished only at the lower end of the integratability spectrum. Key factors to consider are the granularity and level of detail in each artifact, and the maturity of standards for the interchange of architectural descriptions.

<!-- page: 29 -->

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00029_img001.png)

*Figure 1-3. Integration of Architecture Artifacts*

As organizations address common themes (such as Service-Oriented Architecture (SOA), and integrated information infrastructure) and universal data models and standard data structures emerge, integration toward the high end of the spectrum will be facilitated. However, there will always be the need for effective standards governance to reduce the need for manual co-ordination and conflict resolution.

### 1.8. Summary

The TOGAF ADM defines a recommended sequence for the various phases and steps involved in developing an architecture, but it cannot recommend a scope — this has to be determined by the organization itself, bearing in mind that the recommended sequence of development in the ADM process is an iterative one, with the depth and breadth of scope and deliverables increasing with each iteration. Each iteration will add resources to the organization’s Architecture Repository.

While a complete framework is useful (indeed, essential) to have in mind as the ultimate long-term goal, in practice there is a key decision to be made as to the scope of a specific Enterprise Architecture effort. This being the case, it is vital to understand the basis on which scoping decisions are being made, and to set clear expectations for the goal of the effort.

The main guideline is to focus on what creates value to the enterprise, and to select horizontal and vertical scope, and time periods, accordingly. Whether or not this is the first time around, understand that this exercise will be repeated, and that future iterations will build on what is being created in the current effort, adding greater width and depth.

<!-- page: 30 -->

## 2. Preliminary Phase

This chapter describes the preparation and initiation activities required to meet the business directive for a new Enterprise Architecture, including the definition of an Organization-Specific Architecture framework and the definition of principles.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00030_img001.png)

*Figure 2-1: Preliminary Phase*

<!-- page: 31 -->

### 2.1. Objectives

The objectives of the Preliminary Phase are to:

1. Determine the Architecture Capability desired by the organization:

- Review the organizational context for conducting Enterprise Architecture

- Identify and scope the elements of the enterprise organizations affected by the Architecture Capability

- Identify the established frameworks, methods, and processes that intersect with the Architecture Capability

- Establish Capability Maturity target

2. Establish the Architecture Capability:

- Define and establish the Organizational Model for Enterprise Architecture

- Define and establish the detailed process and resources for Architecture Governance

- Select and implement tools that support the Architecture Capability

- Define the Architecture Principles

### 2.2. Inputs

This section defines the inputs to the Preliminary Phase.

#### 2.2.1. Reference Materials External to the Enterprise

- The TOGAF Library

- Other architecture framework(s), if required

#### 2.2.2. Non-Architectural Inputs

- Board strategies and board business plans, business strategy, IT strategy, business principles, business goals, and business drivers, when pre-existing

- Major frameworks operating in the business; e.g., project/portfolio management

- Governance and legal frameworks, including Architecture Governance strategy, when pre-existing

- Architecture capability

- Partnership and contract agreements

<!-- page: 32 -->

#### 2.2.3. Architectural Inputs

Pre-existing models for operating an Enterprise Architecture Capability can be used as a baseline for the Preliminary Phase. Inputs would include:

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Budget requirements

- Governance and support strategy

- Existing Architecture Framework, if any, including:

- Architecture method

- Architecture content

- Configured and deployed tools

- Architecture Principles

- Architecture Repository

### 2.3. Steps

The TOGAF ADM is a generic method, intended to be used by a wide variety of different enterprises, and in conjunction with a wide variety of other architecture frameworks, if required. The Preliminary Phase therefore involves doing any necessary work to initiate and adapt the ADM to define an organization-specific framework. The issues involved with adapting the ADM to a specific organizational context are discussed in detail in Section 1.3.

The level of detail addressed in the Preliminary Phase will depend on the scope and goals of the overall architecture effort.

The order of the steps in the Preliminary Phase as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance.

The steps within the Preliminary Phase are as follows:

- Scope the enterprise organizations impacted; see Section 2.3.1

- Confirm governance and support frameworks; see Section 2.3.2

- Define and establish Enterprise Architecture team and organization; see Section 2.3.3

- Identify and establish Architecture Principles; see Section 2.3.4

<!-- page: 33 -->

- Tailor the TOGAF framework and, if any, other selected architecture frameworks; see Section 2.3.5

- Develop a strategy and implementation plan for tools and techniques; see Section 2.3.6

#### 2.3.1. Scope the Enterprise Organizations Impacted

- Identify core enterprise (units) — those who are most affected and achieve most value from the work

- Identify soft enterprise (units) — those who will see change to their capability and work with core units but are otherwise not directly affected

- Identify extended enterprise (units) — those units outside the scoped enterprise who will be affected in their own Enterprise Architecture

- Identify communities involved (enterprises) — those stakeholders who will be affected and who are in groups of communities

- Identify governance involved, including legal frameworks and geographies (enterprises)

#### 2.3.2. Confirm Governance and Support Frameworks

The architecture framework will form the keystone to the flavor (centralized or federated, light or heavy, etc.) of Architecture Governance organization and guidelines that need to be developed. Part of the major output of this phase is a framework for Architecture Governance. We need to understand how architectural material (standards, guidelines, models, compliance reports, etc.) is brought under governance; i.e., what type of governance repository characteristics are going to be required, what relationships and status recording are necessary to ascertain which governance process (dispensation, compliance, take-on, retirement, etc.) has ownership of an architectural artifact.

It is likely that the existing governance and support models of an organization will need to change to support the newly adopted architecture framework.

To manage the organizational change required to adopt the new architectural framework, the current enterprise governance and support models will need to be assessed to understand their overall shape and content. Additionally, the sponsors and stakeholders for architecture will need to be consulted on potential impacts that could occur.

Upon completion of this step, the architecture touch-points and likely impacts should be understood and agreed by relevant stakeholders.

#### 2.3.3. Define and Establish Enterprise Architecture Team and Organization

- Determine existing enterprise and business capability

- Conduct an Enterprise Architecture/business change maturity assessment, if required

- Identify gaps in existing work areas

- Allocate key roles and responsibilities for Enterprise Architecture Capability management and governance

<!-- page: 34 -->

- Define requests for change to existing business programs and projects:

- Inform existing Enterprise Architecture and IT architecture work of stakeholder requirements

- Request assessment of impact on their plans and work

- Identify common areas of interest

- Identify any critical differences and conflicts of interest

- Produce requests for change to stakeholder activities

- Determine constraints on Enterprise Architecture work

- Review and agree with sponsors and board

- Assess budget requirements

#### 2.3.4. Identify and Establish Architecture Principles

Architecture Principles (see the TOGAF Standard — ADM Techniques) are based on business principles and are critical in setting the foundation for Architecture Governance. Once the organizational context is understood, define a set of Architecture Principles that is appropriate to the enterprise.

#### 2.3.5. Tailor the TOGAF Framework and, if any, Other Selected Architecture Framework(s)

In this step, determine what tailoring of the TOGAF framework is required. Consider the need for:

- Terminology Tailoring: architecture practitioners should use terminology that is generally understood across the enterprise

Tailoring should produce an agreed terminology set for description of architectural content. Consideration should be given to the creation of an Enterprise Glossary, to be updated throughout the architecture process.

- Process Tailoring: the TOGAF ADM provides a generic process for carrying out architecture

Process tailoring provides the opportunity to remove tasks that are already carried out elsewhere in the organization, add organization-specific tasks (such as specific checkpoints), and to align the ADM processes to external process frameworks and touch-points. Key touch-points to be addressed would include:

- Links to (project and service) portfolio management processes

- Links to project lifecycle

- Links to operations handover processes

- Links to operational management processes (including configuration management, change management, and service management)

- Links to procurement processes

<!-- page: 35 -->

- Content Tailoring: using the TOGAF Architecture Content Framework and Enterprise Continuum as a basis, tailoring of content structure and classification approach allows adoption of third-party content frameworks and also allows for customization of the framework to support organizationspecific requirements

#### 2.3.6. Develop a Strategy and Implementation Plan for Tools and Techniques

There are many tools and techniques which may be used to develop Enterprise Architecture across many domains. The development of a tools strategy is recommended that reflects the understanding and level of formality required by the enterprise’s stakeholders. Architecture content will be highly dependent on the scale, sophistication, and culture of both the stakeholders and the Architecture Capability within the organization. A tools strategy which recognizes the stakeholders’ articulation requirements will enable more effective and rapid decision-making by stakeholders and their ownership of artifacts.

The strategy should encompass management techniques, decision management, workshop techniques, business modeling, detailed infrastructure modeling, office products, languages, and repository management as well as more formal architecture tools. For example, the Balanced Scorecard technique is a best practice performance measurement tool used by business schools and many organizations that can be used successfully in architecture projects.

The implementation of the tools strategy may be based on common desktop and office tools or may be based on a customized deployment of specialist management and architecture tools. Change management of the artifact deliverables is a major consideration and a degree of management control and governance of artifacts needs to be considered. Access to decisions needs to be managed carefully as many of the artifacts may contain sensitive information. Therefore the tools implementation, access, and security of the content needs to reflect the sensitivity requirements.

##### 2.3.6.1. Issues in Tools Standardization

In the current state of the tools market, many enterprises developing Enterprise Architectures struggle with the issue of standardizing on tools, whether they seek a single “one size fits all” tool or a multitool suite for modeling architectures and generating the different architecture views required.

There are ostensible advantages associated with selecting a single tool. Organizations following such a policy can hope to realize benefits such as reduced training, shared licenses, quantity discounts, maintenance, and easier data interchange. However, there are also reasons for refusing to identify a single mandated tool, including reasons of principle (endorsing a single architecture tool would not encourage competitive commercial innovation or the development of advanced tool capability); and the fact that a single tool would not accommodate a variety of architecture development “maturity levels” and specific needs across an enterprise.

<!-- page: 36 -->

Successful Enterprise Architecture teams are often those that harmonize their architecture tools with their architecture maturity level, team/organizational capabilities, and objectives or focus. If different organizations within an enterprise are at different architecture maturity levels and have different objectives or focus (e.g., Enterprise versus Business versus Technology Architecture), it becomes very difficult for one tool to satisfy all organizations’ needs.

### 2.4. Outputs

The outputs of the Preliminary Phase may include, but are not restricted to:

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Tailored Architecture Framework (see the TOGAF Standard — Architecture Content), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Architecture Principles (see the TOGAF Standard — Architecture Content)

- Configured and deployed tools

- Initial Architecture Repository (see the TOGAF Standard — Architecture Content), populated with framework content

- Restatement of, or reference to, business principles, business goals, and business drivers (see the TOGAF Standard — Architecture Content)

- Request for Architecture Work (optional) (see the TOGAF Standard — Architecture Content)

- Architecture Governance Framework (see the TOGAF Standard — EA Capability and Governance)

- The Architecture of the Enterprise Architecture Capability (see the TOGAF Standard — EA Capability and Governance)

The outputs may include some or all of the following:

- Catalogs:

- Principles catalog

<!-- page: 37 -->

### 2.5. Approach

This Preliminary Phase is about defining “where, what, why, who, and how we do architecture” in the enterprise concerned. The main aspects are as follows:

- Defining the enterprise

- Identifying key drivers and elements in the organizational context

- Defining the requirements for architecture work

- Defining the Architecture Principles that will inform any architecture work

- Defining the framework to be used

- Defining the relationships between management frameworks

- Evaluating the Enterprise Architecture maturity

The Enterprise Architecture provides a strategic, top-down view of an organization to enable executives, planners, architects, and engineers to coherently co-ordinate, integrate, and conduct their activities. The Enterprise Architecture framework provides the strategic context within which this team can operate.

Therefore, developing the Enterprise Architecture is not a solitary activity and Enterprise Architects need to recognize the interoperability between their frameworks and the rest of the business.

Strategic, interim, and tactical business objectives and aspirations need to be met. Similarly, the Enterprise Architecture needs to reflect this requirement and allow for operation of architecture discipline at different levels within the organization.

Depending on the scale of the enterprise and the level of budgetary commitment to Enterprise Architecture discipline, a number of approaches may be adopted to sub-divide or partition architecture teams, processes, and deliverables. Approaches for architecture partitioning are discussed in the TOGAF Standard — Architecture Content. The Preliminary Phase should be used to determine the desired approach to partitioning and to establish the groundwork for the selected approach to be put into practice.

The Preliminary Phase may be revisited, from the Architecture Vision phase (see the TOGAF Standard

- Applying the ADM), in order to ensure that the organization’s Architecture Capability is suitable to address a specific architecture problem.

The Preliminary Phase is about creating an architecture for the Enterprise Architecture Capability in an organization. As such, the same best practices employed in developing any architecture should be used here. Refer to the TOGAF Standard — EA Capability and Governance for an explanation about the application of the TOGAF ADM to establish the Enterprise Architecture Capability. Further guidance on how to construct an Enterprise Architecture Capability may be found in the following document: TOGAF® Series Guide: The TOGAF Leader’s Guide to Establishing and Evolving an EA Capability.

<!-- page: 38 -->

#### 2.5.1. Enterprise

One of the main challenges of Enterprise Architecture is that of enterprise scope.

The scope of the enterprise, and whether it is federated, will determine those stakeholders who will derive most benefit from the Enterprise Architecture Capability. It is imperative that a sponsor is appointed at this stage to ensure that the resultant activity has resources to proceed and the clear support of the business management. The enterprise may encompass many organizations and the duties of the sponsor are to ensure that all stakeholders are included in defining, establishing, and using the Architecture Capability.

#### 2.5.2. Organizational Context

In order to make effective and informed decisions about the framework for architecture to be used within a particular enterprise, it is necessary to understand the context surrounding the architecture framework. Specific areas to consider would include:

- The commercial models for Enterprise Architecture and budgetary plans for Enterprise Architecture activity; where no such plans exist, the Preliminary Phase should be used to develop a budget plan

- The stakeholders for architecture in the enterprise; their key issues and concerns

- The intentions and culture of the organization, as captured within board business directives, business imperatives, business strategies, business principles, business goals, and business drivers

- Current processes that support execution of change and operation of the enterprise, including the structure of the process and also the level of rigor and formality applied within the organization

Areas for focus should include:

- Current methods for architecture description

- Current project management frameworks and methods

- Current systems management frameworks and methods

- Current project portfolio management processes and methods

- Current application portfolio management processes and methods

- Current technology portfolio management processes and methods

- Current information portfolio management processes and methods

- Current systems design and development frameworks and methods

- The Baseline Architecture landscape, including the state of the enterprise and also how the landscape is currently represented in documentation form

- The skills and capabilities of the enterprise and specific organizations that will be adopting the framework

<!-- page: 39 -->

Review of the organizational context should provide valuable requirements on how to tailor the architecture framework in terms of:

- Level of formality and rigor to be applied

- Level of sophistication and expenditure required

- Touch-points with other organizations, processes, roles, and responsibilities

- Focus of content coverage

#### 2.5.3. Requirements for Architecture Work

The business imperatives behind the Enterprise Architecture work drive the requirements and performance metrics for the architecture work. They should be sufficiently clear so that this phase may scope the business outcomes and resource requirements, and define the outline enterprise business information requirements and associated strategies of the Enterprise Architecture work to be done. For example, these may include:

- Business requirements

- Cultural aspirations

- Organization intents

- Strategic intent

- Forecast financial requirements

Significant elements of these need to be articulated so that the sponsor can identify all the key decision-makers and stakeholders involved in defining and establishing an Architecture Capability.

#### 2.5.4. Principles

The Preliminary Phase defines the Architecture Principles that will form part of the constraints on any architecture work undertaken in the enterprise. The issues involved in this are explained in the TOGAF Standard — ADM Techniques.

The definition of Architecture Principles is fundamental to the development of an Enterprise Architecture. Architecture work is informed by business principles as well as Architecture Principles. The Architecture Principles themselves are also normally based in part on business principles. Defining business principles normally lies outside the scope of the architecture function. However, depending on how such principles are defined and promulgated within the enterprise, it may be possible for the set of Architecture Principles to also restate, or cross-refer to a set of business principles, business goals, and strategic business drivers defined elsewhere within the enterprise. Within an architecture project, the architect will normally need to ensure that the definitions of these business principles, goals, and strategic drivers are current, and to clarify any areas of ambiguity.

The issue of Architecture Governance is closely linked to that of Architecture Principles. The body responsible for governance will also normally be responsible for approving the Architecture

<!-- page: 40 -->

Principles, and for resolving architecture issues. The issues involved in governance are explained in the TOGAF Standard — EA Capability and Governance.

#### 2.5.5. Management Frameworks

The TOGAF ADM is a generic method, intended to be used by enterprises in a wide variety of industry types and geographies. It is also designed for use with a wide variety of other Enterprise Architecture frameworks, if required (although it can be used perfectly well in its own right, without adaptation).

The TOGAF framework has to co-exist with and enhance the operational capabilities of other management frameworks that are present within any organization either formally or informally. In addition to these frameworks, most organizations have a method for the development of solutions, most of which have an IT component. The significance of systems is that they bring together the various domains (also known as People, Processes, and Material/Technology) to deliver a business capability.

The main frameworks suggested to be co-ordinated with the TOGAF framework are:

- Business Capability Management that determines what business capabilities are required to deliver business value including the definition of return on investment and the requisite control/performance measures

- Project/Portfolio Management Methods that determine how a company manages its change initiatives

- Operations Management Methods that describe how a company runs its day-to-day operations, including IT

- Solution Development Methods that formalize the way that business systems are delivered in accordance with the structures developed in the IT architecture

As illustrated in Figure 2-2, these frameworks are not discrete and there are significant overlaps between them and the Business Capability Management. The latter includes the delivery of performance measured business value.

The overall significance is that the Enterprise Architect applying the TOGAF framework cannot narrowly focus on the IT implementation, but must be aware of the impact that the architecture has on the entire enterprise.

<!-- page: 41 -->

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00041_img001.png)

*Figure 2-2: Management Frameworks to Co-ordinate with the TOGAF Framework*

The Preliminary Phase therefore involves doing any necessary work to adapt the ADM to define an organization-specific framework, using either the TOGAF deliverables or the deliverables of another framework. The issues involved in this are discussed in Section 1.3.

#### 2.5.6. Relating the Management Frameworks

*Figure 2-3 illustrates a more detailed set of dependencies between the various frameworks and*

business planning activity that incorporates the enterprise’s strategic plan and direction. The Enterprise Architecture can be used to provide a structure for all of the corporate initiatives, the Portfolio Management Framework can be used to deliver the components of the architecture, and the Operations Management Framework supports incorporation of these new components within the corporate infrastructure.

The business planners are present throughout the process and are in a position to support and enforce the architecture by retaining approval for resources at the various stages of planning and development.

The solution development methodology is used within the Portfolio Management Framework to plan, create, and deliver the architectural components specified in the project and portfolio charters. These deliverables include, but are not exclusively, IT; for example, a new building, a new set of skills, production equipment, hiring, marketing, and so on. Enterprise Architecture potentially provides the context for all enterprise activities.

<!-- page: 42 -->

The management frameworks are required to complement each other and work in close harmony for the good of the enterprise.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00042_img001.png)

*Figure 2-3: Interoperability and Relationships between Management Frameworks*

Business planning at the strategy level provides the initial direction to Enterprise Architecture. Updates at the annual planning level provide a finer level of ongoing guidance. Capability-based planning is one of many popular techniques for business planning.

Enterprise Architecture structures the business planning into an integrated framework that regards the enterprise as a system or system of systems. This integrated approach will validate the business plan and can provide valuable feedback to the corporate planners. In some organizations, the Enterprise Architects have been moved to or work very closely with the strategic direction groups. The TOGAF approach delivers a framework for Enterprise Architecture.

Project/portfolio management is the delivery framework that receives the structured, detailed direction that enables them to plan and build what is required, knowing that each assigned deliverable will be in context (i.e., the piece of the puzzle that they deliver will fit into the corporate puzzle that is the Enterprise Architecture). Often this framework is based upon the Project Management Institute or UK Office of Government Commerce (PRINCE2®) project management methodologies. Project architectures and detailed out-of-context design are often based upon systems design methodologies.

Guidance on how to use the TOGAF ADM along with a Project Management framework may be found in the TOGAF® Series Guide: Architecture Project Management.

Operations management receives the deliverables and then integrates and sustains them within the corporate infrastructure. Often the IT service management services are based upon the IT4IT Reference Architecture, ITIL®, and ISO/IEC 20000:2011.

#### 2.5.7. Planning for Enterprise Architecture/Business Change Maturity Evaluation

Capability Maturity Models are useful ways of assessing the ability of an enterprise to exercise different capabilities.

<!-- page: 43 -->

Capability Maturity Models typically identify selected factors that are required to exercise a capability. An organization’s ability to execute specific factors provides a measure of maturity and can be used to recommend a series of sequential steps to improve a capability. It is an assessment that gives executives an insight into pragmatically improving a capability.

A good Enterprise Architecture maturity model covers the characteristics necessary to develop and consume Enterprise Architecture. Organizations can determine their own factors and derive the appropriate maturity models, but it is recommended to take an existing model and customize it as required.

Several good models exist, including National Association of State CIOs (NASCIO), and the US Department of Commerce Architecture Capability Maturity Model. Other examples include the US Federal Enterprise Architecture Maturity Model. Even though the models are originally from government, they are equally applicable to industry.

<!-- page: 44 -->

## 3. Phase A: Architecture Vision

This chapter describes the initial phase of the ADM. It includes information about defining the scope, identifying the stakeholders, creating the Architecture Vision, and obtaining approvals.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00044_img001.png)

*Figure 3-1: Phase A: Architecture Vision*

### 3.1. Objectives

The objectives of Phase A are to:

- Develop a high-level aspirational vision of the capabilities and business value to be delivered as a result of the proposed Enterprise Architecture

<!-- page: 45 -->

- Obtain approval for a Statement of Architecture Work that defines a program of works to develop and deploy the architecture outlined in the Architecture Vision

### 3.2. Inputs

This section defines the inputs to Phase A.

#### 3.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

#### 3.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Business principles, business goals, and business drivers (see the TOGAF Standard — Architecture Content)

#### 3.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Re-use requirements

- Budget requirements

- Requests for change

- Governance and support strategy

- Tailored Architecture Framework (see the TOGAF Standard — Architecture Content), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Architecture Principles (see the TOGAF Standard — Architecture Content), including business principles, when pre-existing

- Configured and deployed tools

- Populated Architecture Repository (see the TOGAF Standard — Architecture Content) — existing architectural documentation (framework description, architectural descriptions, baseline descriptions, Architecture Building Blocks (ABBs), etc.)

<!-- page: 46 -->

### 3.3. Steps

The level of detail addressed in Phase A will depend on the scope and goals of the Request for Architecture Work, or the subset of scope and goals associated with this iteration of architecture development.

The order of the steps in Phase A as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance.

The steps in Phase A are as follows:

- Establish the architecture project; see Section 3.3.1

- Identify stakeholders, concerns, and business requirements; see Section 3.3.2

- Confirm and elaborate business goals, business drivers, and constraints; see Section 3.3.3

- Evaluate capabilities; see Section 3.3.4

- Assess readiness for business transformation; see Section 3.3.5

- Define scope; see Section 3.3.6

- Confirm and elaborate Architecture Principles, including business principles; see Section 3.3.7

- Develop Architecture Vision; see Section 3.3.8

- Define the Target Architecture value propositions and KPIs; see Section 3.3.9

- Identify the business transformation risks and mitigation activities; see Section 3.3.10

- Develop Statement of Architecture Work; secure approval; see Section 3.3.11

#### 3.3.1. Establish the Architecture Project

Enterprise Architecture is a business capability; each cycle of the ADM should normally be handled as a project using the project management framework of the enterprise. In some cases, architecture projects will be stand-alone. In other cases, architectural activities will be a subset of the activities within a larger project. In either case, architecture activity should be planned and managed using accepted practices for the enterprise.

Conduct the necessary procedures to secure recognition of the project, the endorsement of corporate management, and the support and commitment of the necessary line management. Include references to other management frameworks in use within the enterprise, explaining how this project relates to those frameworks.

#### 3.3.2. Identify Stakeholders, Concerns, and Business Requirements

Identify the key stakeholders and their concerns/objectives, and define the key business requirements to be addressed in the architecture engagement. Stakeholder engagement at this stage is intended to accomplish three objectives:

<!-- page: 47 -->

- To identify candidate vision components and requirements to be tested as the Architecture Vision is developed

- To identify candidate scope boundaries for the engagement to limit the extent of architectural investigation required

- To identify stakeholder concerns, issues, and cultural factors that will shape how the architecture is presented and communicated

The major product resulting from this step is a stakeholder map for the engagement, showing which stakeholders are involved with the engagement, their level of involvement, and their key concerns (see the TOGAF Standard — ADM Techniques). The stakeholder map is used to support various outputs of the Architecture Vision phase, and to identify:

- The concerns and viewpoints that are relevant to this project; this is captured in the Architecture Vision (see the TOGAF Standard — Architecture Content)

- The stakeholders that are involved with the project and as a result form the starting point for a Communications Plan (see the TOGAF Standard — Architecture Content)

- The key roles and responsibilities within the project, which should be included within the Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

Another key task will be to consider which architecture views and viewpoints need to be developed to satisfy the various stakeholder requirements. As described in the TOGAF Standard — ADM Techniques, understanding at this stage which stakeholders and which views need to be developed is important in setting the scope of the engagement.

During the Architecture Vision phase, new requirements generated for future architecture work within the scope of the selected requirements need to be documented within the Architecture Requirements Specification, and new requirements which are beyond the scope of the selected requirements must be input to the Requirements Repository for management through the Requirements Management process.

#### 3.3.3. Confirm and Elaborate Business Goals, Business Drivers, and Constraints

Identify the business goals and strategic drivers of the organization.

If these have already been defined elsewhere within the enterprise, ensure that the existing definitions are current, and clarify any areas of ambiguity. Otherwise, go back to the originators of the Statement of Architecture Work and work with them to define these essential items and secure their endorsement by corporate management.

Define the constraints that must be dealt with, including enterprise-wide constraints and projectspecific constraints (time, schedule, resources, etc.). The enterprise-wide constraints may be informed by the business and Architecture Principles developed in the Preliminary Phase or clarified as part of Phase A.

<!-- page: 48 -->

#### 3.3.4. Evaluate Capabilities

It is valuable to understand a collection of capabilities within the enterprise. One part refers to the capability of the enterprise to develop and consume the architecture. The second part refers to the baseline and target capability level of the enterprise. Gaps identified in the Architecture Capability require iteration between Architecture Vision and Preliminary Phase to ensure that the Architecture Capability is suitable to address the scope of the architecture project (see the TOGAF Standard — Applying the ADM).

A key step following from evaluation of business models, or artifacts that clarify priorities of a business strategy, is to identify the required business capabilities the enterprise must possess to act on the strategic priorities.

The detailed assessment of business capability gaps belongs in Phase B as a core aspect of the Business Architecture, where the architect can help the enterprise understand gaps throughout the business, of many types, that need to be addressed in later phases of the architecture.

In the Architecture Vision phase, however, the architect should consider the capability of the enterprise to develop the Enterprise Architecture itself, as required in the specific initiative or project underway. Gaps in the ability to progress through the ADM, whether deriving from skill shortages, information required, process weakness, or systems and tools, are a serious consideration in the vision of whether the architecture effort should continue. The architect can find guidance in Section 3.5 to gather existing business capability frameworks for the enterprise in this early assessment.

Gaps, or limitations, identified in the enterprise’s capability to execute on change will inform the architect on the description of the Target Architecture and on the Implementation and Migration Plan (see the TOGAF Standard — Architecture Content) created in Phase E and Phase F. This step seeks to understand the capabilities and desires of the enterprise at an appropriate level of abstraction (see the TOGAF Standard — Applying the ADM). Consideration of the gap between the baseline and target capability of the enterprise is critical. Showing the baseline and target capabilities within the context of the overall enterprise can be supported by creating Value Chain diagrams that show the linkage of related capabilities. The results of the assessment are documented in a Capability Assessment (see the TOGAF Standard — Architecture Content).

#### 3.3.5. Assess Readiness for Business Transformation

A Business Transformation Readiness Assessment can be used to evaluate and quantify the organization’s readiness to undergo a change. This assessment is based upon the determination and analysis/rating of a series of readiness factors, as described in the TOGAF Standard — ADM Techniques.

The results of the readiness assessment should be added to the Capability Assessment (see the TOGAF Standard — Architecture Content). These results are then used to shape the scope of the architecture, to identify activities required within the architecture project, and to identify risk areas to be addressed.

<!-- page: 49 -->

#### 3.3.6. Define Scope

Define what is inside and what is outside the scope of the Baseline Architecture and Target Architecture efforts, understanding that the baseline and target need not be described at the same level of detail. In many cases, the baseline is described at a higher level of abstraction, so more time is available to specify the target in sufficient detail. The issues involved in this are discussed in Section 1.5. In particular, define:

- The breadth of coverage of the enterprise

- The level of detail required

- The partitioning characteristics of the architecture (see the TOGAF Standard — Applying the ADM for more details)

- The specific architecture domains to be covered (Business, Data, Application, Technology)

- The extent of the time period aimed at, plus the number and extent of any intermediate time period

- The architectural assets to be leveraged, or considered for use, from the organization’s Architecture Repository:

- Assets created in previous iterations of the ADM cycle within the enterprise

- Assets available elsewhere in the industry (other frameworks, systems models, vertical industry models, etc.)

#### 3.3.7. Confirm and Elaborate Architecture Principles, including Business Principles

Review the principles under which the architecture is to be developed. Architecture Principles are normally based on the principles developed as part of the Preliminary Phase. They are explained, and an example set given, in the TOGAF Standard — ADM Techniques. Ensure that the existing definitions are current, and clarify any areas of ambiguity. Otherwise, go back to the body responsible for Architecture Governance and work with them to define these essential items for the first time and secure their endorsement by corporate management.

#### 3.3.8. Develop Architecture Vision

An understanding of the required artifacts will enable the stakeholders to start to scope out their decision-making which will guide subsequent phases. These decisions need to be reflected in the stakeholder map.

Policy development and strategic decisions need to be captured in this phase to enable the subsequent work to be quantified; for example, rationalization decisions and metrics, revenue generation, and targets which meet the business strategy. There are also other areas which need to be addressed; for example, Digital Transformation and IT strategy where decisions on the Architecture Vision will provide leadership and direction for the organization in subsequent phases.

<!-- page: 50 -->

For the Architecture Vision it is recommended that first an overall architecture be decided upon showing how all of the various architecture domain deliverables will fit together (based upon the selected course of action).

Based on the stakeholder concerns, business capability requirements, scope, constraints, and principles, create a high-level view of the Baseline and Target Architectures. The Architecture Vision typically covers the breadth of scope identified for the project, at a high level. Informal techniques are often employed. A common practice is to draw a simple solution concept diagram that illustrates concisely the major components of the solution and how the solution will result in benefit for the enterprise.

Business scenarios are an appropriate and useful technique to discover and document business requirements, and to articulate an Architecture Vision that responds to those requirements. Business scenarios may also be used at more detailed levels of the architecture work (e.g., in Phase B) and are described in the TOGAF® Series Guide: Business Scenarios.

This step generates the first, very high-level definitions of the baseline and target environments, from a business, information systems, and technology perspective, as described in Section 3.4.

These initial versions of the architecture should be stored in the Architecture Repository, organized according to the standards and guidelines established in the architecture framework.

#### 3.3.9. Define the Target Architecture Value Propositions and KPIs

- Develop the business case for the architectures and changes required

- Produce the value proposition for each of the stakeholder groupings

- Assess and define the procurement requirements

- Review and agree the value propositions with the sponsors and stakeholders concerned

- Define the performance metrics and measures to be built into the Enterprise Architecture to meet the business needs

- Assess the business risk (see the TOGAF Standard — ADM Techniques)

The outputs from this activity should be incorporated within the Statement of Architecture Work to allow performance to be tracked accordingly.

#### 3.3.10. Identify the Business Transformation Risks and Mitigation Activities

Identify the risks associated with the Architecture Vision and assess the initial level of risk (e.g., catastrophic, critical, marginal, or negligible) and the potential frequency associated with it. Assign a mitigation strategy for each risk. A risk management framework is described in the TOGAF Standard — ADM Techniques.

<!-- page: 51 -->

There are two levels of risk that should be considered, namely:

- Initial Level of Risk: risk categorization prior to determining and implementing mitigating actions

- Residual Level of Risk: risk categorization after implementation of mitigating actions (if any)

Risk mitigation activities should be considered for inclusion within the Statement of Architecture Work.

#### 3.3.11. Develop Statement of Architecture Work; Secure Approval

Assess the work products that are required to be produced (and by when) against the set of business performance requirements. This will involve ensuring that:

- Performance metrics are built into the work products

- Specific performance-related work products are available

Then, activities will include:

- Identify new work products that will need to be changed

- Provide direction on which existing work products, including building blocks, will need to be changed and ensure that all activities and dependencies on these are co-ordinated

- Identify the impact of change on other work products and dependence on their activities

- Based on the purpose, focus, scope, and constraints, determine which architecture domains should be developed, to what level of detail, and which architecture views should be built

- Assess the resource requirements and availability to perform the work in the timescale required; this will include adhering to the organization’s planning methods and work products to produce the plans for performing a cycle of the ADM

- Estimate the resources needed, develop a roadmap and schedule for the proposed development, and document all these in the Statement of Architecture Work

- Define the performance metrics to be met during this cycle of the ADM by the Enterprise Architecture team

- Develop the specific Enterprise Architecture Communications Plan and show where, how, and when the Enterprise Architects will communicate with the stakeholders, including affinity groupings and communities, about the progress of the Enterprise Architecture developments

- Review and agree the plans with the sponsors, and secure formal approval of the Statement of Architecture Work under the appropriate governance procedures

- Gain sponsor’s sign-off to proceed

<!-- page: 52 -->

### 3.4. Outputs

The outputs of Phase A may include, but are not restricted to:

- Approved Statement of Architecture Work (see the TOGAF Standard — Architecture Content), including in particular:

- Architecture project description and scope

- Overview of Architecture Vision

- Architecture project plan and schedule

- Refined statements of business principles, business goals, and business drivers (see the TOGAF Standard — Architecture Content)

- Architecture Principles (see the TOGAF Standard — ADM Techniques)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

- Tailored Architecture Framework (see the TOGAF Standard — Architecture Content) (for the engagement), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Architecture Vision (see the TOGAF Standard — Architecture Content), including:

- Problem description

- Objective of the Statement of Architecture Work

- Summary views

- Business scenario (optional)

- Refined key high-level stakeholder requirements

- Draft Architecture Definition Document, which may include Baseline and/or Target Architectures of any architecture domain

- Communications Plan (see the TOGAF Standard — Architecture Content)

- Additional content populating the Architecture Repository (see the TOGAF Standard — Architecture Content)

Note: Multiple business scenarios may be used to generate a single Architecture Vision.

The TOGAF Standard — Architecture Content contains a detailed description of architectural artifacts which might be produced in this phase, describing them in detail and relating them to entities,

<!-- page: 53 -->

### 3.5. Approach

#### 3.5.1. General

Phase A starts with receipt of a Request for Architecture Work from the sponsoring organization to the architecture organization.

The issues involved in ensuring proper recognition and endorsement from corporate management, and the support and commitment of line management, are discussed in the TOGAF Standard — EA Capability and Governance.

Phase A also defines what is in and what is outside the scope of the architecture effort and the constraints that must be dealt with. Scoping decisions need to be made on the basis of a practical assessment of resource and competence availability, and the value that can realistically be expected to accrue to the enterprise from the chosen scope of architecture work. The issues involved in this are discussed in Section 1.5. Scoping issues addressed in the Architecture Vision phase will be restricted to the specific objectives for this ADM cycle and will be constrained within the overall scope definition for architecture activity as established within the Preliminary Phase and embodied within the architecture framework.

In situations where the architecture framework in place is not appropriate to achieve the desired Architecture Vision, revisit the Preliminary Phase and extend the overall architecture framework for the enterprise.

The constraints will normally be informed by the business principles and Architecture Principles, developed as part of the Preliminary Phase; see Chapter 2.

Normally, the business principles, business goals, and strategic drivers of the organization are already defined elsewhere in the enterprise. If so, the activity in Phase A is involved with ensuring that existing definitions are current, and clarifying any areas of ambiguity. Otherwise, it involves defining these essential items for the first time.

Similarly, the Architecture Principles that form part of the constraints on architecture work will normally have been defined in the Preliminary Phase; see Chapter 2. The activity in Phase A is concerned with ensuring that the existing principle definitions are current, and clarifying any areas of ambiguity. Otherwise, it entails defining the Architecture Principles for the first time, as explained in the TOGAF Standard — ADM Techniques.

#### 3.5.2. Creating the Architecture Vision

The Architecture Vision provides the sponsor with a key tool to sell the benefits of the proposed capability to stakeholders and decision-makers within the enterprise. Architecture Vision describes how the new capability will meet the business goals and strategic objectives and address the stakeholder concerns when implemented.

<!-- page: 54 -->

Integral to the Architecture Vision is an understanding of emerging technologies and their potential impact on industries and enterprises, without which many business opportunities may be missed.

Clarifying and agreeing the purpose of the architecture effort is one of the key parts of this activity, and the purpose needs to be clearly reflected in the vision that is created. Architecture projects are often undertaken with a specific purpose in mind — a specific set of business drivers that represent the return on investment for the stakeholders in the architecture development. Clarifying that purpose, and demonstrating how it will be achieved by the proposed architecture development, is the whole point of the Architecture Vision.

Normally, key elements of the Architecture Vision — such as the enterprise mission, vision, strategy, and goals — have been documented as part of some wider business strategy or enterprise planning activity that has its own lifecycle within the enterprise. In such cases, the activity in Phase A is concerned with verifying and understanding the documented business strategy and goals, and possibly bridging between the enterprise strategy and goals on the one hand, and the strategy and goals implicit within the current architecture reality.

Business models are key strategy artifacts that can provide such a perspective, by showing how the organization intends to deliver value to its customers and stakeholders. Section 3.3.4 introduces the application of business models as a step in developing the Architecture Vision.

In other cases, little or no Business Architecture work may have been done to date. In such cases, there will be a need for the architecture team to research, verify, and gain buy-in to the key business objectives and processes that the architecture is to support. This may be done as a free-standing exercise, either preceding architecture development, or as part of the ADM initiation phase (Preliminary Phase).

This exercise should examine and search for existing materials on fundamental Business Architecture concepts such as:

- Business Capabilities, which represent a particular ability or capacity that a business may possess or exchange to achieve a specific purpose or outcome

In this phase, the architect should determine whether a framework exists in the organization to represent business capabilities. If one does not exist, the architect should consider whether developing a framework is within the scope of the project. For an introduction to business capabilities, see TOGAF® Series Guide: Business Capabilities.

- Value Streams, which represent an end-to-end collection of value-adding activities that create an overall result for a customer, stakeholder, or end user; for an introduction to value streams, see the TOGAF® Series Guide: Value Streams.

- Organization Maps, which depict the relationships between the primary entities that make up the enterprise, its partners, and stakeholders

As traditional organizational charts often lack the necessary detail to reflect the full scope of the enterprise’s activities, the architect can help to identify and understand the complex web of

<!-- page: 55 -->

relationships between business entities as well as where business capabilities are used and connection to value stream stages. These are refined and extended in subsequent phases. For an introduction to organization maps, see the TOGAF® Series Guide: Organization Mapping.

In addition, the Architecture Vision explores other domains which are appropriate for the Enterprise Architecture in hand. These domains may include elements of the basic domains, yet serve an additional purpose for the stakeholders. Example domains may include:

- Information

- Security

- Digital

- Network Management

- Knowledge

- Industry-specific

- Services

- Partnership

- Cybersecurity

These domains may be free-standing or linked with other domains to provide enterprise-wide views of the organization vision and structure.

The Architecture Vision phase includes the conduct of a business assessment (using, for example, business scenarios) where critical factors are documented and various courses of action are assessed. High-level advantages and disadvantages, including risks and opportunities, are documented and the best course of action selected to serve as the basis for the Architecture Vision.

The Architecture Vision provides a first-cut, high-level description of the Baseline and Target Architectures, covering the Business, Data, Application, and Technology domains. These outline descriptions are developed in subsequent phases.

Once an Architecture Vision is defined and documented in the Statement of Architecture Work, it is critical to use it to build a consensus, as described in the TOGAF Standard — EA Capability and Governance. Without this consensus it is very unlikely that the final architecture will be accepted by the organization as a whole. The consensus is represented by the sponsoring organization signing the Statement of Architecture Work.

<!-- page: 56 -->

## 4. Phase B: Business Architecture

This chapter describes the development of a Business Architecture to support an agreed Architecture Vision.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00056_img001.png)

*Figure 4-1: Phase B: Business Architecture*

### 4.1. Objectives

The objectives of Phase B are to:

- Develop the Target Business Architecture that describes how the enterprise needs to operate to achieve the business goals, and respond to the strategic drivers set out in the Architecture Vision, in a way that addresses the Statement of Architecture Work and stakeholder concerns

<!-- page: 57 -->

- Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Business Architectures

### 4.2. Inputs

This section defines the inputs to Phase B.

#### 4.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

#### 4.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Business principles, business goals, and business drivers (see the TOGAF Standard — Architecture Content)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

- Communications Plan (see the TOGAF Standard — Architecture Content)

#### 4.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Tailored Architecture Framework (see the TOGAF Standard — Architecture Content), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Approved Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Principles (see the TOGAF Standard — Architecture Content), including business principles, when pre-existing

- Enterprise Continuum (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

<!-- page: 58 -->

- Re-usable building blocks

- Publicly available reference models

- Organization-specific reference models

- Organization standards

- Architecture Vision (see the TOGAF Standard — Architecture Content), including:

- Problem description

- Objective of the Statement of Architecture Work

- Summary views

- Business Scenario (optional)

- Refined key high-level stakeholder requirements

- Draft Architecture Definition Document, which may include Baseline and/or Target Architectures of any architecture domain

### 4.3. Steps

The level of detail addressed in Phase B will depend on the scope and goals of the overall architecture effort.

New models characterizing the needs of the business will need to be defined in detail during Phase B. Existing business artifacts to be carried over and supported in the target environment may already have been adequately defined in previous architectural work; but, if not, they too will need to be defined in Phase B.

The order of the steps in Phase B as well as the time at which they are formally started and completed should be adapted to the situation at hand, in accordance with the established Architecture Governance. In particular, determine whether in this situation it is appropriate to conduct Baseline or Target Architecture development first, as described in the TOGAF Standard — Applying the ADM.

All activities that have been initiated in these steps should be closed during the Finalize the Business Architecture step; see Section 4.3.8. The documentation generated from these steps must be formally published in the Create/Update the Architecture Definition Document step; see Section 4.3.9.

The steps in Phase B are as follows:

- Select reference models, viewpoints, and tools; see Section 4.3.1

- Develop Baseline Business Architecture Description; see Section 4.3.2

- Develop Target Business Architecture Description; see Section 4.3.3

- Perform gap analysis; see Section 4.3.4

- Define candidate roadmap components; see Section 4.3.5

- Resolve impacts across the Architecture Landscape; see Section 4.3.6

<!-- page: 59 -->

- Conduct formal stakeholder review; see Section 4.3.7

- Finalize the Business Architecture; see Section 4.3.8

- Create/Update the Architecture Definition Document; see Section 4.3.9

#### 4.3.1. Select Reference Models, Viewpoints, and Tools

Select relevant Business Architecture resources (reference models, patterns, etc.) from the Architecture Repository, on the basis of the business drivers and stakeholder concerns.

Select relevant Business Architecture viewpoints (e.g., operations, management, financial); i.e., those that will enable the architect to demonstrate how the stakeholder concerns are being addressed in the Business Architecture.

Identify appropriate tools and techniques to be used for capture, modeling, and analysis, in association with the selected viewpoints. Depending on the degree of sophistication warranted, these may comprise simple documents or spreadsheets, or more sophisticated modeling tools and techniques, such as activity models, business process models, use-case models, etc.

##### 4.3.1.1. Determine Overall Modeling Process

Business modeling and strategy assessments are effective techniques for framing the target state of an organization’s Business Architecture; see Section 3.3.4. The output from that activity is then used to articulate the business capabilities, organizational structure, and value streams required to close gaps between the current and target state. As addressed in Section 3.5, the frameworks for these maps may already exist and should be leveraged, now using them to characterize gaps and better map business value to achieve the Target Business Architecture.

For each viewpoint, select the models needed to support the specific view required, using the selected tool or method.

Ensure that all stakeholder concerns are covered. If they are not, create new models to address concerns not covered, or augment existing models; see Section 4.5.7. Business scenarios are a useful technique to discover and document business requirements, and may be used iteratively, at different levels of detail in the hierarchical decomposition of the Business Architecture. Business scenarios are described in the TOGAF® Series Guide: Business Scenarios. The techniques described in Section 4.5 can be utilized to progressively decompose a business:

- Business Capability Mapping: identifies, categorizes, and decomposes the business capabilities required for the business to have the ability to deliver value to one or more stakeholders

- Information Mapping: collecting the information concepts and their relationships that matter most to the business

- Organization Mapping: a representation of the organizational structure of the business (including third-party domains), depicting business units, the decomposition of those units into lower-level functions, and organizational relationships (unit-to-unit and mapping to business capabilities, locations, and other attributes)

<!-- page: 60 -->

- Process Modeling: the activity of articulating business processes of an enterprise, to enable analysis and improvement

- Structured Analysis: identifies the key business capabilities within the scope of the architecture, and maps those capabilities onto business functions and organizational units within the business

- Use-case Analysis: a technique used to identify the requirements of a system or task to be completed, from a user’s perspective

- Value Stream Mapping: the end-to-end breakdown of activities that an organization performs to create the value being exchanged with stakeholders

Value stream maps illustrate how an organization delivers value and are in the context of a specific set of stakeholders, and leverage business capabilities in order to create stakeholder value and align to other aspects of the Target Business Architecture.

The level and rigor of decomposition needed varies from enterprise to enterprise, as well as within an enterprise, and the architect should consider the enterprise’s goals, objectives, scope, and purpose of the Enterprise Architecture effort to determine the level of decomposition.

##### 4.3.1.2. Identify Required Catalogs of Business Building Blocks

Catalogs capture inventories of the core assets of the business. Catalogs are hierarchical in nature and capture the decomposition of a building block and also decompositions across related building blocks (e.g., organization/actor).

Catalogs form the raw material for development of matrices and views and also act as a key resource for managing the business and IT capability.

The TOGAF Standard — Architecture Content contains a detailed description of catalogs which should be considered for development within a Business Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 4.3.1.3. Identify Required Matrices

Matrices show the core relationships between related model entities.

Matrices form the raw material for development of views and also act as a key resource for impact assessment, carried out as a part of gap analysis.

The TOGAF Standard — Architecture Content contains a detailed description of matrices which should be considered for development within a Business Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

<!-- page: 61 -->

##### 4.3.1.4. Identify Required Diagrams

Diagrams present the Business Architecture information from a set of different perspectives (viewpoints) according to the requirements of the stakeholders.

The TOGAF Standard — Architecture Content contains a detailed description of diagrams which should be considered for development within a Business Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 4.3.1.5. Identify Types of Requirement to be Collected

Once the Business Architecture catalogs, matrices, and diagrams have been developed, architecture modeling is completed by formalizing the business-focused requirements for implementing the Target Architecture.

These requirements may:

- Relate to the business domain

- Provide requirements input into the Data, Application, and Technology Architectures

- Provide detailed guidance to be reflected during design and implementation to ensure that the solution addresses the original architecture requirements

Within this step, the architect should identify requirements that should be met by the architecture; see

### Section 13.5.2.

In many cases, the Architecture Definition will not be intended to give detailed or comprehensive requirements for a solution (as these can be better addressed through general requirements management discipline). The expected scope of requirements content should be established during the Architecture Vision phase and documented in the approved Statement of Architecture Work.

Any requirement, or change in requirement, that is outside of the scope defined in the Statement of Architecture Work must be submitted to the Requirements Repository for management through the governed Requirements Management process.

#### 4.3.2. Develop Baseline Business Architecture Description

Develop a Baseline Description of the existing Business Architecture, to the extent necessary to support the Target Business Architecture. The scope and level of detail to be defined will depend on the extent to which existing business elements are likely to be carried over into the Target Business Architecture, and on whether Architecture Descriptions exist, as described in Section 4.5. To the extent possible, identify the relevant Business Architecture building blocks, drawing on the Architecture Repository (see the TOGAF Standard — Architecture Content).

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 4.3.1) as a guideline for creating new architecture content to describe the Baseline Architecture.

<!-- page: 62 -->

#### 4.3.3. Develop Target Business Architecture Description

Develop a Target Description for the Business Architecture, to the extent necessary to support the Architecture Vision. The scope and level of detail to be defined will depend on the relevance of the business elements to attaining the Target Architecture Vision, and on whether architectural descriptions exist. To the extent possible, identify the relevant Business Architecture building blocks, drawing on the Architecture Repository (see the TOGAF Standard — Architecture Content).

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 4.3.1) as a guideline for creating new architecture content to describe the Target Architecture.

If appropriate, investigate different Target Architecture alternatives and discuss these with stakeholders using the Architecture Alternatives and Trade-offs technique (see the TOGAF Standard — ADM Techniques).

#### 4.3.4. Perform Gap Analysis

Verify the architecture models for internal consistency and accuracy:

- Perform trade-off analysis to resolve conflicts (if any) among the different views

- Validate that the models support the principles, objectives, and constraints

- Note changes to the viewpoint represented in the selected models from the Architecture Repository, and document

- Test architecture models for completeness against requirements

Identify gaps between the baseline and target, using the gap analysis technique, as described in the TOGAF Standard — ADM Techniques.

#### 4.3.5. Define Candidate Roadmap Components

Following the creation of a Baseline Architecture, Target Architecture, and gap analysis results, a business roadmap is required to prioritize activities over the coming phases.

This initial Business Architecture Roadmap will be used as raw material to support more detailed definition of a consolidated, cross-discipline roadmap within the Opportunities & Solutions phase.

#### 4.3.6. Resolve Impacts Across the Architecture Landscape

Once the Business Architecture is finalized, it is necessary to understand any wider impacts or implications. At this stage, other architecture artifacts in the Architecture Landscape should be examined to identify:

- Does this Business Architecture create an impact on any pre-existing architectures?

- Have recent changes been made that impact on the Business Architecture?

<!-- page: 63 -->

- Are there any opportunities to leverage work from this Business Architecture in other areas of the organization?

- Does this Business Architecture impact other projects (those planned as well as those in progress)?

- Will this Business Architecture be impacted by other projects (those planned as well as those in progress)?

#### 4.3.7. Conduct Formal Stakeholder Review

Check the original motivation for the architecture project and the Statement of Architecture Work against the proposed Business Architecture, asking if it is fit for the purpose of supporting subsequent work in the other architecture domains. Refine the proposed Business Architecture only if necessary.

#### 4.3.8. Finalize the Business Architecture

- Select standards for each of the building blocks, re-using as much as possible from the reference models selected from the Architecture Repository

- Fully document each building block

- Conduct a final cross-check of overall architecture against business goals; document the rationale for building block decisions in the architecture document

- Document the final requirements traceability report

- Document the final mapping of the architecture within the Architecture Repository; from the selected building blocks, identify those that might be re-used (working practices, roles, business relationships, job descriptions, etc.), and publish via the Architecture Repository

- Finalize all the work products, such as gap analysis results

#### 4.3.9. Create/Update the Architecture Definition Document

- Document the rationale for building block decisions in the Architecture Definition Document

- Prepare the appropriate business sections of the Architecture Definition Document related to the intended scope and use of the architecture

If appropriate, use reports and/or graphics generated by modeling tools to demonstrate key views of the architecture. Route the document for review by relevant stakeholders, and incorporate feedback.

### 4.4. Outputs

The outputs of Phase B may include, but are not restricted to:

- Refined and updated versions of the Architecture Vision phase deliverables, where applicable, including:

<!-- page: 64 -->

- Validated business principles, business goals, and business drivers (see the TOGAF Standard — Architecture Content), updated if necessary

- Architecture Principles (see the TOGAF Standard — Architecture Content)

- Draft Architecture Definition Document (see the TOGAF Standard — Architecture Content), including:

- Baseline Business Architecture, Approved, if appropriate

- Target Business Architecture, Approved, including:

- Organization structure — identifying business locations and relating them to organizational units

- Business goals and objectives — for the enterprise and each organizational unit

- Business functions — a detailed, recursive step involving successive decomposition of major functional areas into sub-functions

- Business capabilities — the abilities that a business needs to possess or exchange to achieve its goals and objectives

- Business services — the services that support the business by encapsulating a unique “elements of business behavior”; a service offered external to the enterprise may be supported by business services

- Products — output generated by the business to be offered to customers; products include materials and/or services

- Business processes, including measures and deliverables

- Business roles, including development and modification of skills requirements

- Business data model

- Correlation of organization/business functions and business capabilities — relate business capabilities to organizational units in the form of a matrix report

- Views corresponding to the selected viewpoints addressing key stakeholder concerns

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including such Business Architecture requirements as:

- Gap analysis results

- Technical requirements — identifying, categorizing, and prioritizing the implications for work in the remaining architecture domains; for example, by a dependency/priority matrix (e.g., guiding trade-off between speed of transaction processing and security); list the specific models that are expected to be produced (for example, expressed as primitives of the Zachman Framework)

- Updated business requirements

- Business Architecture components of an Architecture Roadmap (see the TOGAF Standard — Architecture Content)

<!-- page: 65 -->

The TOGAF Standard — Architecture Content contains a detailed description of architectural artifacts which might be produced in this phase.

### 4.5. Approach

Business Architecture is a representation of holistic, multi-dimensional business views of capabilities, end-to-end value delivery, information, and organizational structure; and the relationships among these business views and strategies, products, policies, initiatives, and stakeholders.

Business Architecture relates business elements to business goals and elements of other domains.

#### 4.5.1. General

A knowledge of the Business Architecture is a prerequisite for architecture work in any other domain (Data, Application, Technology), and is therefore the first architecture activity that needs to be undertaken, if not catered for already in other organizational processes (enterprise planning, strategic business planning, business process re-engineering, etc.).

In practical terms, the Business Architecture is also often necessary as a means of demonstrating the business value of subsequent architecture work to key stakeholders, and the return on investment to those stakeholders from supporting and participating in the subsequent work.

The scope of work in Phase B is primarily determined by the Architecture Vision as set out in Phase A. The business strategy defines the goals and drivers and the metrics for success, but not necessarily how to get there. That is the role of the Business Architecture, defined in detail in Phase B.

This will depend to a large extent on the enterprise environment. In some cases, key elements of the Business Architecture may be done in other activities; for example, the enterprise mission, vision, strategy, and goals may be documented as part of some wider business strategy or enterprise planning activity that has its own lifecycle within the enterprise.

In such cases, there may be a need to verify and update the currently documented business strategy and plans, and/or to bridge between high-level business drivers, business strategy, and goals on the one hand, and the specific business requirements that are relevant to this architecture development effort.

In other cases, little or no Business Architecture work may have been done to date. In such cases, there will be a need for the architecture team to research, verify, and gain buy-in to the key business objectives and processes that the architecture is to support. This may be done as a free-standing exercise, either preceding architecture development, or as part of Phase A.

In both of these cases, the business scenarios technique (see the TOGAF® Series Guide: Business Scenarios), or any other method that illuminates the key business requirements and indicates the implied technical requirements for IT architecture, may be used.

<!-- page: 66 -->

A key objective is to re-use existing material as much as possible. In architecturally more mature environments, there will be existing Architecture Definitions, which (hopefully) will have been maintained since the last architecture development cycle. Where Architecture Descriptions exist, these can be used as a starting point, and verified and updated if necessary; see the TOGAF Standard — Architecture Content.

Gather and analyze only that information that allows informed decisions to be made relevant to the scope of this architecture effort. If this effort is focused on the definition of (possibly new) business processes, then Phase B will necessarily involve a lot of detailed work. If the focus is more on the Target Architectures in other domains (data/information, application systems, infrastructure) to support an essentially existing Business Architecture, then it is important to build a complete picture in Phase B without going into unnecessary detail.

#### 4.5.2. Developing the Baseline Description

If an enterprise has existing Architecture Descriptions, they should be used as the basis for the Baseline Description. This input may have been used already in Phase A in developing the Architecture Vision, such as the business capability map or a core set of value streams as introduced in Section 3.5.2, and may be sufficient in itself for this baseline.

The reasons to update these materials include having a missing business capability, a new value stream, or changed organizational unit that has not previously been assessed within the scope of the Enterprise Architecture project. Section 4.5.3, through Section 4.5.6, address the use of core Business Architecture methods to model the Business Architecture driven by the strategy scope from Phase A. Note that putting these methods into action to drive a focus and target state for later architecture work does not mean that the fundamental frameworks from Phase A, such as a common enterprise business capability map, will necessarily change but rather that they are applied in a manner driven by the scope and needs of the specific Enterprise Architecture project.

If no Architecture Descriptions exist, information should be gathered and Business Architecture models developed.

Whatever the scope of the specific project, it is important to determine whether it is the fundamental view of the business that is changing or the usage of those views to determine scope, priorities, and relationships for the specific project in relation to the rest of the enterprise.

#### 4.5.3. Applying Business Capabilities

The business capability map found or developed in the Architecture Vision phase provides a selfcontained view of the business that is independent of the current organizational structure, business processes, information systems and applications, and the rest of the product or service portfolio. Those business capabilities should be mapped back to the organizational units, value streams, information systems, and strategic plans within the scope of the Enterprise Architecture project. This relationship mapping provides greater insight into the alignment and optimization of each of those domains (see Relationship Mapping in TOGAF® Series Guide: Business Capabilities).

<!-- page: 67 -->

Another common analysis technique involves heat mapping, which can be used to show a range of different perspectives on the same set of core business capabilities. These include maturity, effectiveness, performance, and the value or cost of each capability to the business. Different attributes determine the colors of each capability on the business capability map (see Heat Mapping in TOGAF® Series Guide: Business Capabilities).

For example, a business capability maturity heat map shows the desired maturity as green for a specific capability, one level down as yellow, and two or more levels down as red. Other colors may indicate status, such as purple denoting a capability that does not exist yet in the company but is desired, or perhaps as a capability that is over-funded and has more resources than necessary. This gap analysis is directly tied to the Enterprise Architecture project underway; a gap is only relevant in the context of the business need and provides focus for more mapping in this phase or priorities for later architecture phases.

#### 4.5.4. Applying Value Streams

Value streams provide valuable stakeholder context into why the organization needs business capabilities, while business capabilities provide what the organization needs for a particular value stage to be successful.

Start with the initial set of value stream models for the business documented in the Architecture Vision phase. Within the scope of the specific Enterprise Architecture project, if sufficiently larger in breadth, there may be a need for new value streams not already in the repository.

A new or existing value stream can be analyzed within the scope of the project through heat mapping (by value stream stage) or by developing use-cases around a complete definition of the value stream (see Baseline Example in the TOGAF® Series Guide: Value Streams). A project might focus on specific stakeholders, one element of business value, or stress some stages over others to develop better requirements for solutions in later phases.

The most substantive benefits come from mapping relationships between the stages in a value stream to business capabilities, then performing a gap analysis for capabilities (such as heat mapping) in the context of the business value achieved by the value stream for a specific stakeholder (see Mapping Value Streams to Business Capabilities in the TOGAF® Series Guide: Value Streams).

#### 4.5.5. Applying the Organization Map

An organization map shows the key organizational units, partners, and stakeholder groups that make up the enterprise ecosystem. The map should also depict the working relationship between those entities, as distinct from an organizational chart that only shows hierarchical reporting relationships. The map is typically depicted as a network or web of relationships and interactions between the various business entities (see Organigraphs: Drawing How Companies Really Work, by Mintzberg and Van der Heyden, 1999).

The business unit is the main concept used to establish organization maps. In keeping with the relatively unconstrained view of what constitutes as enterprise, the enterprise may be one business

<!-- page: 68 -->

unit for the project underway, may include all business units, or also include third parties or other stakeholder groups. The interpretation depends on the scope of the architecture effort.

This map is a key element of Business Architecture because it provides the organizational context for the whole Enterprise Architecture effort. While capability mapping exposes what a business does and value stream mapping exposes how it delivers value to specific stakeholders, the organization map identities the business units or third parties that possess or use those capabilities and which participate in the value streams.

Taken together with the methods in Section 4.5.3, Section 4.5.4, and the associated Guides, the organization map provides an understanding of which business units to involve in the architecture effort, who and when to talk about a given requirement, and how to measure the impact of various decisions.

For further guidance on organization maps, see the TOGAF® Series Guide: Organization Mapping.

#### 4.5.6. Applying Information Maps

Characterizing information in the Business Architecture phase starts with the elements that matter most to the business, such as product, customer, factory, etc. With a list of these key elements, a crossdiscipline team can list and map the information that matters most and how it is described using business terms. Domains of information can be derived from groupings or categories that the business terms fall into logically. These domains are a good place to start the information map for completeness and highest value before proceeding later to the details of data types.

Relationships among the information domains can then be added to the map as the next level of understanding for a good baseline information map. The most significant benefit then comes with building matrices between information and business capabilities. The linkage between the information that matters most to the business and the business capabilities that describe the ability to apply that information to create value is a key aspect of Business Architecture. These information maps and relationships to business capabilities will then apply in later architecture phases on data characterization, applications, and infrastructure.

For further guidance on information maps, see the TOGAF® Series Guide: Information Mapping.

#### 4.5.7. Applying Modeling Techniques

The modeling and mapping techniques provided here are extensions that implement the business capabilities, value streams, and organization maps described above in Phase B into the practices of the business. They expand the operating model, which is a representation for how an organization operates across a range of domains in order to accomplish its purpose (see A Method for Identifying Process Re-Use Opportunities to Enhance the Operating Model, M. de Vries et al.).

<!-- page: 69 -->

In addition to the techniques described above (capability maps, value streams, and organization maps), a variety of other modeling techniques may be employed, if deemed appropriate. For example:

- Activity Models (also called Business Process Models) describe the enterprise’s business activities, the data and/or information exchanged between activities (internal exchanges), and the data and/or information exchanged with other activities that are outside the scope of the model (external exchanges)

Activity models are hierarchical in nature. They capture the activities performed in a business process, and the Inputs, Controls, Outputs, and Mechanisms/Resources (ICOMs) of those activities. Activity models can be annotated with explicit statements of business rules, which represent relationships among the ICOMs. For example, a business rule can specify who can do what under specified conditions, the combination of inputs and controls needed, and the resulting outputs. One technique for creating activity models is the Integrated Computer Aided Manufacturing (ICAM) DEFinition (IDEF) modeling technique.

The Object Management Group (OMG) has developed the Business Process Model and Notation TM (BPMN TM), a standard for business process modeling that includes a language with which to specify business processes, their tasks/steps, and the documents produced.

- Use-Case Models describe the business process of an enterprise in terms of use-cases and actors corresponding to business processes and organizational participants (people, organizations, etc.)

The use-case model is described in use-case diagrams and use-case specifications.

- Logical Data Model (or Class Model)

Logical data models describe the entities, their attributes, and the acceptable values for these attributes as well as the relationships between the various entities. Particularly useful is the “is-a” relationship for analyses. For example, if a sedan is a type of car which is a type of vehicle, then a general business rule for all vehicles can be written once and automatically picked up for all types of cars and trucks.

A class model expands the logical data model to include behaviors by including services (methods) unique to the entity (now called a class). Normally applications and information architects will use the class diagram, and Business Architects will use the logical data model.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00069_img001.png)

*Figure 4-2: UML Business Class Diagram*

<!-- page: 70 -->

All three types of model above can be represented in the Unified Modeling LanguageTM (UML®), and a variety of tools exist for generating such models.

Certain industry sectors have modeling techniques specific to the sector concerned.

#### 4.5.8. Architecture Repository

As part of Phase B, the architecture team will need to consider what relevant Business Architecture resources are available from the Architecture Repository (see the TOGAF Standard — Architecture Content), in particular:

- Industry reference models relevant to the organization’s industry sector

- Enterprise-specific Business Architecture views (capability maps, value stream maps, organization maps, etc.)

- Enterprise-specific building blocks (process components, business rules, job descriptions, etc.)

- Applicable standards

<!-- page: 71 -->

## 5. Phase C: Information Systems Architectures

This chapter describes the Information Systems Architectures for an architecture project, including the development of Data and Application Architectures.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00071_img001.png)

*Figure 5-1: Phase C: Information Systems*

<!-- page: 72 -->

### 5.1. Objectives

- Develop the Target Information Systems Architectures, describing how the enterprise’s Information Systems Architecture will enable the Business Architecture and the Architecture Vision, in a way that addresses the Statement of Architecture Work and stakeholder concerns

- Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Information Systems (Data and Application) Architectures

### 5.2. Approach

Phase C involves some combination of Data and Application Architecture, in either order. Advocates exist for both sequences. For example, Steven Spewak’s Enterprise Architecture Planning (EAP) recommends a data-driven approach.

On the other hand, major applications systems — such as those for Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), etc. — often provide a combination of technology infrastructure and business application logic. Some organizations take an application-driven approach, whereby they recognize certain key applications as forming the core underpinning of the missioncritical business processes, and take the implementation and integration of those core applications as the primary focus of their architecture effort (the integration issues often constituting a major challenge).

Detailed descriptions for Phase C are given separately for each architecture domain:

- Phase C: Information Systems Architectures — Data Architecture; see Chapter 6

- Phase C: Information Systems Architectures — Application Architecture; see Chapter 7

<!-- page: 73 -->

## 6. Phase C: Information Systems Architectures — Data Architecture

This chapter describes the Data Architecture part of Phase C.

### 6.1. Objectives

The objectives of the Data Architecture part of Phase C are to:

- Develop the Target Data Architecture that enables the Business Architecture and the Architecture Vision, in a way that addresses the Statement of Architecture Work and stakeholder concerns

- Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Data Architectures

### 6.2. Inputs

This section defines the inputs to Phase C (Data Architecture).

#### 6.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

- TOGAF® Series Guide: Information Architecture — Customer Master Data Management

- TOGAF® Series Guide: Information Architecture: Business Intelligence & Analytics and Metadata Management Reference Models

#### 6.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

- Communications Plan (see the TOGAF Standard — Architecture Content)

#### 6.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

<!-- page: 74 -->

- Governance and support strategy

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Data principles (see the TOGAF Standard — ADM Techniques), if existing

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

- Re-usable building blocks (in particular, definitions of current data)

- Publicly available reference models

- Organization-specific reference models

- Organization standards

- Draft Architecture Definition Document, which may include Baseline and/or Target Architectures of any architecture domain

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Gap analysis results (from Business Architecture)

- Relevant technical requirements that will apply to this phase

- Business Architecture components of an Architecture Roadmap (see the TOGAF Standard — Architecture Content)

### 6.3. Steps

The level of detail addressed in Phase C will depend on the scope and goals of the overall architecture effort.

New data building blocks being introduced as part of this effort will need to be defined in detail during Phase C. Existing data building blocks to be carried over and supported in the target environment may already have been adequately defined in previous architectural work; but, if not, they too will need to be defined in Phase C.

The order of the steps in this phase as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance. In particular, determine whether in this situation it is appropriate to conduct Baseline Description or Target Architecture development first, as described in the TOGAF Standard — Applying the ADM.

<!-- page: 75 -->

All activities that have been initiated in these steps should be closed during the Finalize the Data Architecture step; see Section 6.3.8. The documentation generated from these steps must be formally published in the Create/Update the Architecture Definition Document step; see Section 6.3.9.

The steps in Phase C (Data Architecture) are as follows:

- Select reference models, viewpoints, and tools; see Section 6.3.1

- Develop Baseline Data Architecture Description; see Section 6.3.2

- Develop Target Data Architecture Description; see Section 6.3.3

- Perform gap analysis; see Section 6.3.4

- Define candidate roadmap components; see Section 6.3.5

- Resolve impacts across the Architecture Landscape; see Section 6.3.6

- Conduct formal stakeholder review; see Section 6.3.7

- Finalize the Data Architecture; see Section 6.3.8

- Create/update the Architecture Definition Document; see Section 6.3.9

#### 6.3.1. Select Reference Models, Viewpoints, and Tools

Review and validate (or generate, if necessary) the set of data principles. These will normally form part of an overarching set of Architecture Principles. Guidelines for developing and applying principles, and a sample set of data principles, are given in the TOGAF Standard — ADM Techniques.

Select relevant Data Architecture resources (reference models, patterns, etc.) on the basis of the business drivers, stakeholders, concerns, and Business Architecture.

Select relevant Data Architecture viewpoints (for example, stakeholders of the data — regulatory bodies, users, generators, subjects, auditors, etc.; various time dimensions — real-time, reporting period, event-driven, etc.; locations; business processes); i.e., those that will enable the architect to demonstrate how the stakeholder concerns are being addressed in the Data Architecture.

Identify appropriate tools and techniques (including forms) to be used for data capture, modeling, and analysis, in association with the selected viewpoints. Depending on the degree of sophistication warranted, these may comprise simple documents or spreadsheets, or more sophisticated modeling tools and techniques such as data management models, data models, etc.

Examples of data modeling techniques are:

- Entity relationship diagram

- Class diagram

<!-- page: 76 -->

Further guidance on Information Architecture reference models can be found in the following documents:

- TOGAF® Series Guide: Information Architecture — Customer Master Data Management

- TOGAF® Series Guide: Information Architecture: Business Intelligence & Analytics

- TOGAF® Series Guide: Information Architecture: Metadata Management

##### 6.3.1.1. Determine Overall Modeling Process

For each viewpoint, select the models needed to support the specific view required, using the selected tool or method.

Ensure that all stakeholder concerns are covered. If they are not, create new models to address concerns not covered, or augment existing models (see above).

The recommended process for developing a Data Architecture is as follows:

- Collect data-related models from existing Business Architecture and Application Architecture materials

- Rationalize data requirements and align with any existing enterprise data catalogs and models; this allows the development of a data inventory and entity relationship

- Update and develop matrices across the architecture by relating data to business service, business capability, business function, access rights, and application

- Elaborate Data Architecture views by examining how data is created, distributed, migrated, secured, and archived

##### 6.3.1.2. Identify Required Catalogs of Data Building Blocks

Descriptions of data may be captured as a catalog showing decomposition across related model entities (e.g., data entity → logical data component → physical data component).

During the Business Architecture phase, a Business Service/Information diagram was created showing the key data entities required by the main business services. This is a prerequisite to successful Data Architecture activities.

Using the traceability from business function/business capability to application and data entity, it is possible to create an inventory of the data needed to support the Architecture Vision.

Once the data requirements are consolidated in a single location, it is possible to refine the data inventory to achieve semantic consistency and to remove gaps and overlaps.

The TOGAF Standard — Architecture Content contains a detailed description of catalogs which should be considered for development within a Data Architecture, describing them in detail and relating them

<!-- page: 77 -->

##### 6.3.1.3. Identify Required Matrices

At this stage, an entity to applications matrix could be produced to validate this mapping. How data is created, maintained, transformed, and passed to other applications, or used by other applications, will now start to be understood. Obvious gaps such as entities that never seem to be created by an application or data created but never used, need to be noted for later gap analysis.

The rationalized data inventory can be used to update and refine the architectural diagrams of how data relates to other aspects of the architecture.

Once these updates have been made, it may be appropriate to drop into a short iteration of the Application Architecture to resolve the changes identified.

The TOGAF Standard — Architecture Content contains a detailed description of matrices which should be considered for development within a Data Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 6.3.1.4. Identify Required Diagrams

Diagrams present the Data Architecture information from a set of different perspectives (viewpoints) according to the requirements of the stakeholders.

Once the data entities have been refined, a diagram of the relationships between entities and their attributes can be produced.

It is important to note at this stage that information may be a mixture of enterprise-level data (from system service providers and package vendor information) and local-level data held in personal databases and spreadsheets.

The level of detail modeled needs to be carefully assessed. Some physical system data models will exist down to a very detailed level; others will only have core entities modeled. Not all data models will have been kept up-to-date as applications were modified and extended over time. It is important to achieve a balance in the level of detail provided (e.g., the reproduction of existing detailed system physical data schemas or the presentation of high-level process maps and data requirements highlight the two extreme views).

The TOGAF Standard — Architecture Content contains a detailed description of diagrams which should be considered for development within a Data Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 6.3.1.5. Identify Types of Requirement to be Collected

Once the Data Architecture catalogs, matrices, and diagrams have been developed, architecture modeling is completed by formalizing the data-focused requirements for implementing the Target Architecture.

<!-- page: 78 -->

These requirements may:

- Relate to the data domain

- Provide requirements input into the Application and Technology Architectures

- Provide detailed guidance to be reflected during design and implementation to ensure that the solution addresses the original architecture requirements

Within this step, the architect should identify requirements that should be met by the architecture (see

### Section 13.5.2).

#### 6.3.2. Develop Baseline Data Architecture Description

Develop a Baseline Description of the existing Data Architecture, to the extent necessary to support the Target Data Architecture. The scope and level of detail to be defined will depend on the extent to which existing data elements are likely to be carried over into the Target Data Architecture, and on whether architectural descriptions exist, as described in Section 6.5. To the extent possible, identify the relevant Data Architecture building blocks, drawing on the Architecture Repository (see the TOGAF Standard — Architecture Content).

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 6.3.1) as a guideline for creating new architecture content to describe the Baseline Architecture.

#### 6.3.3. Develop Target Data Architecture Description

Develop a Target Description for the Data Architecture, to the extent necessary to support the Architecture Vision and Target Business Architecture. The scope and level of detail to be defined will depend on the relevance of the data elements to attaining the Target Architecture, and on whether architectural descriptions exist. To the extent possible, identify the relevant Data Architecture building blocks, drawing on the Architecture Repository (see TOGAF Standard — Architecture Content).

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 6.3.1) as a guideline for creating new architecture content to describe the Target Architecture.

If appropriate, investigate different Target Architecture alternatives and discuss these with stakeholders using the Architecture Alternatives and Trade-offs technique (see the TOGAF Standard — ADM Techniques).

#### 6.3.4. Perform Gap Analysis

Verify the architecture models for internal consistency and accuracy:

- Perform trade-off analysis to resolve conflicts (if any) among the different views

- Validate that the models support the principles, objectives, and constraints

<!-- page: 79 -->

- Note changes to the viewpoint represented in the selected models from the Architecture Repository, and document

- Test architecture models for completeness against requirements

Identify gaps between the Baseline and Target, using the gap analysis technique as described in the TOGAF Standard — ADM Techniques.

#### 6.3.5. Define Candidate Roadmap Components

Following the creation of a Baseline Architecture, Target Architecture, and gap analysis, a data roadmap is required to prioritize activities over the coming phases.

This initial Data Architecture roadmap will be used as raw material to support more detailed definition of a consolidated, cross-discipline roadmap within the Opportunities & Solutions phase.

#### 6.3.6. Resolve Impacts Across the Architecture Landscape

Once the Data Architecture is finalized, it is necessary to understand any wider impacts or implications.

At this stage, other architecture artifacts in the Architecture Landscape should be examined to identify:

- Does this Data Architecture create an impact on any pre-existing architectures?

- Have recent changes been made that impact the Data Architecture?

- Are there any opportunities to leverage work from this Data Architecture in other areas of the organization?

- Does this Data Architecture impact other projects (including those planned as well as those currently in progress)?

- Will this Data Architecture be impacted by other projects (including those planned as well as those currently in progress)?

#### 6.3.7. Conduct Formal Stakeholder Review

Check the original motivation for the architecture project and the Statement of Architecture Work against the proposed Data Architecture. Conduct an impact analysis to identify any areas where the Business and Application Architectures (e.g., business practices) may need to change to cater for changes in the Data Architecture (for example, changes to forms or procedures, applications, or database systems).

If the impact is significant, this may warrant the Business and Application Architectures being revisited.

Identify any areas where the Application Architecture (if generated at this point) may need to change to cater for changes in the Data Architecture (or to identify constraints on the Application Architecture about to be designed).

<!-- page: 80 -->

If the impact is significant, it may be appropriate to drop into a short iteration of the Application Architecture at this point.

Identify any constraints on the Technology Architecture about to be designed, refining the proposed Data Architecture only if necessary.

#### 6.3.8. Finalize the Data Architecture

- Select standards for each of the building blocks, re-using as much as possible from the reference models selected from the Architecture Repository

- Fully document each building block

- Conduct a final cross-check of overall architecture against business requirements; document the rationale for building block decisions in the architecture document

- Document the final requirements traceability report

- Document the final mapping of the architecture within the Architecture Repository; from the selected building blocks, identify those that might be re-used, and publish via the Architecture Repository

- Finalize all the work products, such as gap analysis

#### 6.3.9. Create/Update the Architecture Definition Document

Document the rationale for building block decisions in the Architecture Definition Document.

Prepare the Data Architecture sections of the Architecture Definition Document, comprising some or all of:

- Business data model

- Logical data model

- Data management process model

- Data Entity/Business Function matrix

- Data interoperability requirements (e.g., XML schema, security policies)

- If appropriate, use reports and/or graphics generated by modeling tools to demonstrate key views of the architecture; route the document for review by relevant stakeholders, and incorporate feedback

### 6.4. Outputs

The outputs of Phase C (Data Architecture) may include, but are not restricted to:

- Refined and updated versions of the Architecture Vision phase deliverables, where applicable:

<!-- page: 81 -->

- Validated data principles (see the TOGAF Standard — ADM Techniques), or new data principles (if generated here)

- Draft Architecture Definition Document (see the TOGAF Standard — Architecture Content), including:

- Baseline Data Architecture, Approved, if appropriate

- Target Data Architecture, Approved, including:

  - Business data model

  - Logical data model

  - Data management process models

  - Data Entity/Business Function matrix

- Views corresponding to the selected viewpoints addressing key stakeholder concerns

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including such Data Architecture requirements as:

- Gap analysis results

- Data interoperability requirements

- Relevant technical requirements that will apply to this evolution of the architecture development cycle

- Constraints on the Technology Architecture about to be designed

- Updated business requirements, if appropriate

- Updated application requirements, if appropriate

- Data Architecture components of an Architecture Roadmap (see the TOGAF Standard — Architecture Content)

The TOGAF Standard — Architecture Content contains a detailed description of architectural artifacts which might be produced in this phase.

### 6.5. Approach

#### 6.5.1. Data Structure

A Data Architecture should be able to handle:

- Data at rest — data in stores

- Data in motion — data in transactions or services/APIs

- Data in use — data at the border of the application (e.g., GUI)

- Open data — data that the organization provides for public usage and which it is voluntarily or legally required to provide

<!-- page: 82 -->

Different alternate ways of working with these types of Data Architecture will be added.

Data Architecture is created by using three metamodel entities: data entity, logical data component, and physical data component.

Data entities can be used to create conceptual data models to help the IT developers understand the concepts they will be dealing with. Often the entity relationship models also contain some requirements on the relations (e.g., a customer can only have one address).

Logical data components can be used to create logical data models. Often it is important for the IT area to have a clear view of all data that is used in the IT environment. The logical data model is often used as a requirement on the data stored in applications (at rest), data moved between applications (in motion), or data at the user interface of applications (data in use).

Physical data components are clusters of logical data components that have been implemented by some earlier project (links to, for example, XML message, database schemas) or requirements for new implementation projects.

All three data entities can be used in data exchange models for data passed between/into/out of IS services, logical application components, or physical application components.

All data entities can have quality attributes for specific situations.

#### 6.5.2. Key Considerations for Data Architecture

##### 6.5.2.1. Data Management

When an enterprise has chosen to undertake large-scale architectural transformation, it is important to understand and address data management issues. A structured and comprehensive approach to data management enables the effective use of data to capitalize on its competitive advantages.

Considerations include:

- A clear definition of which application components in the landscape will serve as the system of record or reference for enterprise master data

- Will there be an enterprise-wide standard that all application components, including software packages, need to adopt?

(In the main, packages can be prescriptive about the data models and may not be flexible.)

- Clearly understand how data entities are utilized by business capabilities, business functions, processes, and business and application services

- Clearly understand how and where enterprise data entities are created, stored, transported, and reported

- What is the level and complexity of data transformations required to support the information exchange needs between applications?

<!-- page: 83 -->

- What will be the requirement for software in supporting data integration with the enterprise’s customers and suppliers (e.g., use of Extract, Transform, Load (ETL) tools during data migration, data profiling tools to evaluate data quality, etc.)?

More guidance on data management can be found in the TOGAF® Series Guide: Information Architecture — Customer Master Data Management.

##### 6.5.2.2. Data Migration

When an existing application is replaced, there will be a critical need to migrate data (master, transactional, and reference) to the new application. The Data Architecture should identify data migration requirements and also provide indicators as to the level of transformation, weeding, and cleansing that will be required to present data in a format that meets the requirements and constraints of the target application. The objective being that the target application has quality data when it is populated. Another key consideration is to ensure that an enterprise-wide common data definition is established to support the transformation.

##### 6.5.2.3. Data Governance

Data governance considerations ensure that the enterprise has the necessary dimensions in place to enable the transformation, as follows:

- Structure: this dimension pertains to whether the enterprise has the necessary organizational structure and the standards bodies to manage data entity aspects of the transformation

- Management System: here enterprises should have the necessary management system and datarelated programs to manage the governance aspects of data entities throughout its lifecycle

- People: this dimension addresses what data-related skills and roles the enterprise requires for the transformation

If the enterprise lacks such resources and skills, the enterprise should consider either acquiring those critical skills or training existing internal resources to meet the requirements through a welldefined learning program.

#### 6.5.3. Architecture Repository

As part of this phase, the architecture team will need to consider what relevant Data Architecture resources are available in the organization’s Architecture Repository (see the TOGAF Standard — Architecture Content); in particular, generic data models relevant to the organization’s industry “vertical” sector.

<!-- page: 84 -->

## 7. Phase C: Information Systems Architectures — Application Architecture

This chapter describes the Application Architecture part of Phase C.

### 7.1. Objectives

The objectives of the Application Architecture part of Phase C are to:

- Develop the Target Application Architecture that enables the Business Architecture and the Architecture Vision, in a way that addresses the Statement of Architecture Work and stakeholder concerns

- Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Application Architectures

### 7.2. Inputs

This section defines the inputs to Phase C (Application Architecture).

#### 7.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

#### 7.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

- Communications Plan (see the TOGAF Standard — Architecture Content)

#### 7.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

<!-- page: 85 -->

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Application principles (see the TOGAF Standard — ADM Techniques), if existing

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

- Re-usable building blocks

- Publicly available reference models

- Organization-specific reference models

- Organization standards

- Draft Architecture Definition Document, which may include Baseline and/or Target Architectures of any architecture domain

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Gap analysis results (from Business Architecture and Data Architecture, if available)

- Relevant technical requirements that will apply to this phase

- Business and Data Architecture components of an Architecture Roadmap, if available (see the TOGAF Standard — Architecture Content)

### 7.3. Steps

The level of detail addressed in Phase C will depend on the scope and goals of the overall architecture effort.

New application building blocks being introduced as part of this effort will need to be defined in detail during Phase C. Existing application building blocks to be carried over and supported in the target environment may already have been adequately defined in previous architectural work; but, if not, they too will need to be defined in Phase C.

The order of the steps in this phase as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance. In particular, determine whether in this situation it is appropriate to conduct Baseline Description or Target Architecture development first, as described in the TOGAF Standard — Applying the ADM.

<!-- page: 86 -->

All activities that have been initiated in these steps should be closed during the Finalize the Application Architecture step; see Section 7.3.8. The documentation generated from these steps must be formally published in the Create/Update the Architecture Definition Document step; see Section 7.3.9.

The steps in Phase C (Application Architecture) are as follows:

- Select reference models, viewpoints, and tools; see Section 7.3.1

- Develop Baseline Application Architecture Description; see Section 7.3.2

- Develop Target Application Architecture Description; see Section 7.3.3

- Perform gap analysis; see Section 7.3.4

- Define candidate roadmap components; see Section 7.3.5

- Resolve impacts across the Architecture Landscape; see Section 7.3.6

- Conduct formal stakeholder review; see Section 7.3.7

- Finalize the Application Architecture; see Section 7.3.8

- Create/Update the Architecture Definition Document; see Section 7.3.9

#### 7.3.1. Select Reference Models, Viewpoints, and Tools

Review and validate (or generate, if necessary) the set of application principles. These will normally form part of an overarching set of Architecture Principles. Guidelines for developing and applying principles, and a sample set of application principles, are given in the TOGAF Standard — ADM Techniques.

Select relevant Application Architecture resources (reference models, patterns, etc.) from the Architecture Repository, on the basis of the business drivers, the stakeholders, and their concerns.

Select relevant Application Architecture viewpoints (for example, stakeholders of the applications — viewpoints relevant to functional and individual users of applications, etc.); i.e., those that will enable the architect to demonstrate how the stakeholder concerns are being addressed in the Application Architecture.

Identify appropriate tools and techniques to be used for capture, modeling, and analysis, in association with the selected viewpoints. Depending on the degree of sophistication warranted, these may comprise simple documents or spreadsheets, or more sophisticated modeling tools and techniques.

Consider using platform-independent descriptions of business logic. For example, the OMG Model- Driven Architecture® (MDA®) offers an approach to modeling Application Architectures that preserves the business logic from changes to the underlying platform and implementation technology.

##### 7.3.1.1. Determine Overall Modeling Process

For each viewpoint, select the models needed to support the specific view required, using the selected tool or method.

<!-- page: 87 -->

Ensure that all stakeholder concerns are covered. If they are not, create new models to address concerns not covered, or augment existing models (see above).

The recommended process for developing an Application Architecture is as follows:

- Understand the list of applications or application components that are required, based on the baseline Application Portfolio, what the requirements are, and the Business Architecture scope

- Simplify complicated applications by decomposing them into two or more applications

- Ensure that the set of application definitions is internally consistent, by removing duplicate functionality as far as possible, and combining similar applications into one

- Identify logical applications and the most appropriate physical applications

- Develop matrices across the architecture by relating applications to business services, business capabilities, data, processes, etc.

- Elaborate a set of Application Architecture views by examining how the application will function, capturing integration, migration, development, and operational concerns

The level and rigor of decomposition needed varies from enterprise to enterprise, as well as within an enterprise, and the architect should consider the enterprise’s goals, objectives, scope, and purpose of the Enterprise Architecture effort to determine the level of decomposition.

The level of granularity should be sufficient to enable identification of gaps and the scope of candidate work packages.

##### 7.3.1.2. Identify Required Catalogs of Application Building Blocks

The organization’s Application Portfolio is captured as a catalog within the Architecture Repository. Catalogs are hierarchical in nature and capture a decomposition of a metamodel entity and also decompositions across related model entities (e.g., logical application component → physical application component → application service).

Catalogs form the raw material for the development of matrices and diagrams and also act as a key resource for managing the business and IT capability.

The structure of catalogs is based on the attributes of metamodel entities, as defined in the TOGAF Standard — Architecture Content.

The TOGAF Standard — Architecture Content contains a detailed description of catalogs which should be considered for development within an Application Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

<!-- page: 88 -->

##### 7.3.1.3. Identify Required Matrices

Matrices show the core relationships between related model entities.

Matrices form the raw material for development of diagrams and also act as a key resource for impact assessment.

Once the baseline Application Portfolio has been assembled, it is necessary to map the applications to their purpose in supporting the business. The initial mapping should focus on business services within the Business Architecture, as this is the level of granularity where architecturally significant decisions are most likely to be needed.

Once applications are mapped to business services, it will also be possible to make associations from applications to data, through the business-information diagrams developed during Business Architecture.

If readily available, baseline application data models may be used to validate the Business Architecture and also to identify which data is held locally and which is accessed remotely.

The Data Architecture phase will focus on these issues, so at this point it may be appropriate to drop into a short iteration of the Data Architecture if it is deemed to be valuable to the scope of the architecture engagement.

Using existing information in the baseline application catalog, the Application Architecture should identify user and organizational dependencies on applications. This activity will support future state planning by determining impacted user communities and also facilitating the grouping of applications by user type or user location.

A key user community to be specifically considered is the operational support organization. This activity should examine application dependencies on shared operations capabilities and produce a diagram on how each application is effectively operated and managed.

Specifically considering the needs of the operational community may identify requirements for new or extended governance capabilities and applications.

The TOGAF Standard — Architecture Content contains a detailed description of matrices which should be considered for development within an Application Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 7.3.1.4. Identify Required Diagrams

Diagrams present the Application Architecture information from a set of different perspectives (viewpoints) according to the requirements of the stakeholders. Once the desired functionality of an application is known, it is necessary to perform an internal assessment of how the application should be best structured to meet its requirements.

In the case of packaged applications, it is likely to be the case that the application supports a number of configuration options, add-on modules, or application services that may be applied to the solution. For

<!-- page: 89 -->

custom developed applications, it is necessary to identify the high-level structure of the application in terms of modules or subsystems as a foundation to organize design activity.

The TOGAF Standard — Architecture Content contains a detailed description of diagrams which should be considered for development within an Application Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 7.3.1.5. Identify Types of Requirement to be Collected

Once the Application Architecture catalogs, matrices, and diagrams have been developed, architecture modeling is completed by formalizing the application-focused requirements for implementing the Target Architecture.

These requirements may:

- Relate to the application domain

- Provide requirements input into the Data and Technology Architectures

- Provide detailed guidance to be reflected during design and implementation to ensure that the solution addresses the original architecture requirements

Within this step, the architect should identify requirements that should be met by the architecture; see

### Section 13.5.2.

#### 7.3.2. Develop Baseline Application Architecture Description

Develop a Baseline Description of the existing Application Architecture, to the extent necessary to support the Target Application Architecture. The scope and level of detail to be defined will depend on the extent to which existing applications are likely to be carried over into the Target Application Architecture, and on whether Architecture Descriptions exist, as described in Section 7.5. To the extent possible, identify the relevant Application Architecture building blocks, drawing on the Architecture Repository (see the TOGAF Standard — Architecture Content). If not already existing within the Architecture Repository, define each application in line with the Application Portfolio catalog (see the TOGAF Standard — Architecture Content).

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 7.3.1) as a guideline for creating new architecture content to describe the Baseline Architecture.

#### 7.3.3. Develop Target Application Architecture Description

Develop a Target Description for the Application Architecture, to the extent necessary to support the Architecture Vision, Target Business Architecture, and Target Data Architecture. The scope and level of detail to be defined will depend on the relevance of the application elements to attaining the Target Architecture Vision, and on whether architectural descriptions exist. To the extent possible, identify the relevant Application Architecture building blocks, drawing on the Architecture Repository (see the TOGAF Standard — Architecture Content).

<!-- page: 90 -->

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 7.3.1) as a guideline for creating new architecture content to describe the Target Architecture.

If appropriate, investigate different Target Architecture alternatives and discuss these with stakeholders using the Architecture Alternatives and Trade-offs technique (see the TOGAF Standard — ADM Techniques).

#### 7.3.4. Perform Gap Analysis

Verify the architecture models for internal consistency and accuracy:

- Perform trade-off analysis to resolve conflicts (if any) among the different views

- Validate that the models support the principles, objectives, and constraints

- Note changes to the viewpoint represented in the selected models from the Architecture Repository, and document

- Test architecture models for completeness against requirements

Identify gaps between the baseline and target, using the gap analysis technique as described in the TOGAF Standard — ADM Techniques.

#### 7.3.5. Define Candidate Roadmap Components

Following the creation of a Baseline Architecture, Target Architecture, and gap analysis, an application roadmap is required to prioritize activities over the coming phases.

This initial Application Architecture roadmap will be used as raw material to support more detailed definition of a consolidated, cross-discipline roadmap within the Opportunities & Solutions phase.

#### 7.3.6. Resolve Impacts Across the Architecture Landscape

Once the Application Architecture is finalized, it is necessary to understand any wider impacts or implications.

At this stage, other architecture artifacts in the Architecture Landscape should be examined to identify:

- Does this Application Architecture create an impact on any pre-existing architectures?

- Have recent changes been made that impact the Application Architecture?

- Are there any opportunities to leverage work from this Application Architecture in other areas of the organization?

- Does this Application Architecture impact other projects (including those planned as well as those currently in progress)?

- Will this Application Architecture be impacted by other projects (including those planned as well as those currently in progress)?

<!-- page: 91 -->

#### 7.3.7. Conduct Formal Stakeholder Review

Check the original motivation for the architecture project and the Statement of Architecture Work against the proposed Application Architecture. Conduct an impact analysis, to identify any areas where the Business and Data Architectures (e.g., business practices) may need to change to cater for changes in the Application Architecture (for example, changes to forms or procedures, applications, or database systems). If the impact is significant, this may warrant the Business and Data Architectures being revisited.

Identify any constraints on the Technology Architecture (especially the infrastructure) about to be designed.

#### 7.3.8. Finalize the Application Architecture

- Select standards for each of the building blocks, re-using as much as possible from the reference models selected from the Architecture Repository

- Fully document each building block

- Conduct a final cross-check of overall architecture against business requirements; document the rationale for building block decisions in the architecture document

- Document the final requirements traceability report

- Document the final mapping of the architecture within the Architecture Repository; from the selected building blocks, identify those that might be re-used, and publish via the Architecture Repository

- Finalize all the work products, such as gap analysis

#### 7.3.9. Create/Update the Architecture Definition Document

- Document the rationale for building block decisions in the Architecture Definition Document

- Prepare the Application Architecture sections of the Architecture Definition Document; if appropriate, use reports and/or graphics generated by modeling tools to demonstrate key views of the architecture; route the document for review by relevant stakeholders, incorporate feedback

<!-- page: 92 -->

### 7.4. Outputs

The outputs of Phase C (Application Architecture) may include, but are not restricted to:

- Refined and updated versions of the Architecture Vision phase deliverables, where applicable:

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content), updated if necessary

- Validated application principles, or new application principles (if generated here)

- Draft Architecture Definition Document (see the TOGAF Standard — Architecture Content), including:

- Baseline Application Architecture, Approved, if appropriate

- Target Application Architecture, Approved

- Views corresponding to the selected viewpoints, addressing key stakeholder concerns

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including such Application Architecture requirements as:

- Gap analysis results

- Applications interoperability requirements

- Relevant technical requirements that will apply to this evolution of the architecture development cycle

- Constraints on the Technology Architecture about to be designed

- Updated business requirements, if appropriate

- Updated data requirements, if appropriate

- Application Architecture components of an Architecture Roadmap (see the TOGAF Standard — Architecture Content)

The TOGAF Standard — Architecture Content contains a detailed description of architectural artifacts which might be produced in this phase.

<!-- page: 93 -->

### 7.5. Approach

#### 7.5.1. Architecture Repository

As part of this phase, the architecture team will need to consider what relevant Application Architecture resources are available in the Architecture Repository (see the TOGAF Standard — Architecture Content). In particular:

- Generic business models and related application models relevant to the organization’s industry sector

- Application models relevant to common high-level business functions, such as electronic commerce, supply chain management, etc.

The Open Group has a Reference Model for Integrated Information Infrastructure (III-RM) — see the TOGAF® Series Guide: The TOGAF Integrated Information Infrastructure Reference Model (III-RM) — that focuses on the application-level components and services necessary to provide an integrated information infrastructure.

<!-- page: 94 -->

## 8. Phase D: Technology Architecture

This chapter describes the development of a Technology Architecture for an architecture project.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00094_img001.png)

*Figure 8-1: Phase D: Technology Architecture*

### 8.1. Objectives

The objectives of Phase D are to:

- Develop the Target Technology Architecture that enables the Architecture Vision, target business, data, and application building blocks to be delivered through technology components and technology services, in a way that addresses the Statement of Architecture Work and stakeholder concerns

<!-- page: 95 -->

- Identify candidate Architecture Roadmap components based upon gaps between the Baseline and Target Technology Architectures

### 8.2. Inputs

This section defines the inputs to Phase D.

#### 8.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

- Product information on candidate products

#### 8.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

- Communications Plan (see the TOGAF Standard — Architecture Content)

#### 8.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Tailored Architecture Framework (see the TOGAF Standard — Architecture Content), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Technology principles (see the TOGAF Standard — ADM Techniques), if existing

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

- Publicly available reference models

<!-- page: 96 -->

- Organization-specific reference models

- Draft Architecture Definition Document, which may include Baseline and/or Target Architectures of any architecture domain

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Gap analysis results (from Business, Data, and Application Architectures)

- Relevant technical requirements from previous phases

- Business, Data, and Application Architecture components of an Architecture Roadmap (see the TOGAF Standard — Architecture Content)

### 8.3. Steps

The level of detail addressed in Phase D will depend on the scope and goals of the overall architecture effort.

New technology building blocks being introduced as part of this effort will need to be defined in detail during Phase D. Existing technology building blocks to be supported in the target environment may need to be redefined in Phase D to ensure interoperability and fit-for-purpose within this specific Technology Architecture.

The order of the steps in Phase D as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance. In particular, determine whether it is appropriate to conduct Baseline Description or Target Architecture development first, as described in the TOGAF Standard — Applying the ADM.

All activities that have been initiated in these steps should be closed during the Finalize the Technology Architecture step; see Section 8.3.8. The documentation generated from these steps must be formally published in the Create/Update the Architecture Definition Document step; see Section 8.3.9. The steps in Phase D are as follows:

- Select reference models, viewpoints, and tools; see Section 8.3.1

- Develop Baseline Technology Architecture Description; see Section 8.3.2

- Develop Target Technology Architecture Description; see Section 8.3.3

- Perform gap analysis; see Section 8.3.4

- Define candidate roadmap components; see Section 8.3.5

- Resolve impacts across the Architecture Landscape; see Section 8.3.6

- Conduct formal stakeholder review; see Section 8.3.7

- Finalize the Technology Architecture; see Section 8.3.8

- Create/Update the Architecture Definition Document; see Section 8.3.9

<!-- page: 97 -->

#### 8.3.1. Select Reference Models, Viewpoints, and Tools

Review and validate the set of technology principles. These will normally form part of an overarching set of Architecture Principles. Guidelines for developing and applying principles, and a sample set of technology principles, are given in the TOGAF Standard — ADM Techniques.

Select relevant Technology Architecture resources (reference models, patterns, etc.) from the Architecture Repository (see the TOGAF Standard — Architecture Content), on the basis of the business drivers, stakeholders, and their concerns.

Select relevant Technology Architecture viewpoints that will enable the architect to demonstrate how the stakeholder concerns are being addressed in the Technology Architecture.

Identify appropriate tools and techniques to be used for capture, modeling, and analysis, in association with the selected viewpoints. Depending on the degree of sophistication required, these may comprise simple documents and spreadsheets, or more sophisticated modeling tools and techniques.

##### 8.3.1.1. Determine Overall Modeling Process

For each viewpoint, select the models needed to support the specific view required, using the selected tool or method. Ensure that all stakeholder concerns are covered. If they are not, create new models to address them, or augment existing models (see above).

The process to develop a Technology Architecture incorporates the following steps:

- Define a taxonomy of technology services and logical technology components (including standards)

- Identify relevant locations where technology is deployed

- Carry out a physical inventory of deployed technology and abstract up to fit into the taxonomy

- Look at application and business requirements for technology

- Is the technology in place fit-for-purpose to meet new requirements (i.e., does it meet functional and non-functional requirements)?

- Refine the taxonomy

- Product selection (including dependent products)

- Determine configuration of the selected technology

- Determine impact:

- Sizing and costing

- Capacity planning

- Installation/governance/migration impacts

<!-- page: 98 -->

In the earlier phases of the ADM, certain decisions made around service granularity and service boundaries will have implications on the technology component and the technology service. The areas where the Technology Architecture may be impacted will include the following:

- Performance: the granularity of the service will impact on technology service requirements

Coarse-grained services contain several units of functionality with potentially varying nonfunctional requirements, so platform performance should be considered. In addition, coarsegrained services can sometimes contain more information than actually required by the requesting system.

- Maintainability: if service granularity is too coarse, then introducing changes to that service becomes difficult and impacts the maintenance of the service and the platform on which it is delivered

- Location and Latency: services might interact with each other over remote links and inter-service communication will have in-built latency

Drawing service boundaries and setting the service granularity should consider platform/location impact of these inter-service communications.

- Availability: service invocation is subject to network and/or service failure

High communication availability is an important consideration during service decomposition and defining service granularity.

Product selection processes may occur within the Technology Architecture phase where existing products are re-used, incremental capacity is being added, or product selection decisions are a constraint during project initiation.

Where product selection deviates from existing standards, involves significant effort, or has wideranging impact, this activity should be flagged as an opportunity and addressed through the Opportunities & Solutions phase.

##### 8.3.1.2. Identify Required Catalogs of Technology Building Blocks

Catalogs are inventories of the core assets of the business. Catalogs are hierarchical in nature and capture a decomposition of a metamodel entity and also decompositions across related model entities (e.g., technology service → logical technology component → physical technology component).

Catalogs form the raw material for development of matrices and diagrams and also act as a key resource for managing the business and IT capability.

<!-- page: 99 -->

The Technology Architecture should create technology catalogs as follows:

- Based on existing technology catalogs and analysis of applications carried out in the Application Architecture phase, collect a list of products in use

- If the requirements identified in the Application Architecture are not met by existing products, extend the product list by examining products available on the market that provide the functionality and meet the required standards

- Classify products against the selected taxonomy if appropriate, extending the model as necessary to fit the classification of technology products in use

- If technology standards are currently in place, apply these to the technology component catalog to gain a baseline view of compliance with technology standards

The TOGAF Standard — Architecture Content contains a detailed description of catalogs which should be considered for development within a Technology Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 8.3.1.3. Identify Required Matrices

Matrices show the core relationships between related model entities.

Matrices form the raw material for development of diagrams and also act as a key resource for impact assessment.

The TOGAF Standard — Architecture Content contains a detailed description of matrices which should be considered for development within a Technology Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 8.3.1.4. Identify Required Diagrams

Diagrams present the Technology Architecture information from a set of different perspectives (viewpoints) according to the requirements of the stakeholders.

This activity provides a link between platform requirements and hosting requirements, as a single application may need to be physically located in several environments to support local access, development lifecycles, and hosting requirements.

For major baseline applications or application platforms (where multiple applications are hosted on the same infrastructure stack), produce a stack diagram showing how hardware, operating system, software infrastructure, and packaged applications combine.

If appropriate, extend the Application Architecture diagrams of software distribution to show how applications map onto the technology platform.

For each environment, produce a logical diagram of hardware and software infrastructure showing the contents of the environment and logical communications between components. Where available, collect capacity information on the deployed infrastructure.

<!-- page: 100 -->

For each environment, produce a physical diagram of communications infrastructure, such as routers, switches, firewalls, and network links. Where available, collect capacity information on the communications infrastructure.

The TOGAF Standard — Architecture Content contains a detailed description of diagrams which should be considered for development within a Technology Architecture, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

##### 8.3.1.5. Identify Types of Requirement to be Collected

Once the Technology Architecture catalogs, matrices, and diagrams have been developed, architecture modeling is completed by formalizing the technology-focused requirements for implementing the Target Architecture.

These requirements may:

- Relate to the technology domain

- Provide detailed guidance to be reflected during design and implementation to ensure that the solution addresses the original architecture requirements

Within this step, the architect should identify requirements that should be met by the architecture; see

### Section 13.5.2.

##### 8.3.1.6. Select Services

The services portfolios are combinations of basic services from the service categories in the defined taxonomy that do not conflict. The combination of services are again tested to ensure support for the applications. This is a prerequisite to the later step of defining the architecture fully.

The previously identified requirements can provide more detailed information about:

- Requirements for organization-specific elements or pre-existing decisions (as applicable)

- Pre-existing and unchanging organizational elements (as applicable)

- Inherited external environment constraints

Where requirements demand definition of specialized services that are not identified in the TOGAF Standard, consideration should be given to how these might be replaced if standardized services become available in the future.

For each building block, build up a service description portfolio as a set of non-conflicting services. The set of services must be tested to ensure that the functionality provided meets application requirements.

<!-- page: 101 -->

#### 8.3.2. Develop Baseline Technology Architecture Description

Develop a Baseline Description of the existing Technology Architecture, to support the Target Technology Architecture. The scope and level of detail to be defined will depend on the extent to which existing technology components are likely to be carried over into the Target Technology Architecture, and on whether architectural descriptions exist, as described in Section 8.5.

Identify the relevant Technology Architecture building blocks, drawing on any artifacts held in the Architecture Repository. If nothing exists within the Architecture Repository, define each application in line with the Technology Portfolio catalog (see the TOGAF Standard — Architecture Content).

Begin by converting the description of the existing environment into the terms of the organization’s taxonomy of technology services and technology components (e.g., the TOGAF Technical Reference Model (TRM)). This will allow the team developing the architecture to gain experience and understanding of the taxonomy. The team may be able to take advantage of a previous architectural definition, but it is assumed that some adaptation may be required to match the architectural definition techniques described as part of this process. Another important task is to set down a list of key questions which can be used later in the development process to measure the effectiveness of the new architecture.

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 8.3.1) as a guideline for creating new architecture content to describe the Baseline Architecture.

#### 8.3.3. Develop Target Technology Architecture Description

Develop a Target Description for the Technology Architecture, to the extent necessary to support the Architecture Vision, Target Business Architecture, and Target Information Systems Architecture. The scope and level of detail to be defined will depend on the relevance of the technology elements to attaining the Target Architecture, and on whether architectural descriptions exist. To the extent possible, identify the relevant Technology Architecture building blocks, drawing on the Architecture Repository (see the TOGAF Standard — Architecture Content).

A key process in the creation of a broad architectural model of the target system is the conceptualization of building blocks. ABBs describe the functionality and how they may be implemented without the detail introduced by configuration or detailed design. The method of defining building blocks, along with some general guidelines for their use in creating an architectural model, is described in the TOGAF Standard — Architecture Content.

Where new architecture models need to be developed to satisfy stakeholder concerns, use the models identified within the first step in this phase (see Section 8.3.1) as a guideline for creating new architecture content to describe the Target Architecture. If appropriate, investigate different Target Architecture alternatives and discuss these with stakeholders using the Architecture Alternatives and Trade-offs technique (see the TOGAF Standard — ADM Techniques).

<!-- page: 102 -->

#### 8.3.4. Perform Gap Analysis

Verify the architecture models for internal consistency and accuracy:

- Perform trade-off analysis to resolve conflicts (if any) among the different views

- Validate that the models support the principles, objectives, and constraints

- Note changes to the viewpoint represented in the selected models from the Architecture Repository, and document

- Test architecture models for completeness against requirements

Identify gaps between the baseline and target, using the gap analysis technique as described in the TOGAF Standard — ADM Techniques.

#### 8.3.5. Define Candidate Roadmap Components

Following the creation of a Baseline Architecture, Target Architecture, and gap analysis, a Technology Roadmap is required to prioritize activities over the coming phases.

This initial Technology Architecture roadmap will be used as raw material to support more detailed definition of a consolidated, cross-discipline roadmap within the Opportunities & Solutions phase.

#### 8.3.6. Resolve Impacts Across the Architecture Landscape

Once the Technology Architecture is finalized, it is necessary to understand any wider impacts or implications.

At this stage, other architecture artifacts in the Architecture Landscape should be examined to identify:

- Does this Technology Architecture create an impact on any pre-existing architectures?

- Have recent changes been made that impact the Technology Architecture?

- Are there any opportunities to leverage work from this Technology Architecture in other areas of the organization?

- Does this Technology Architecture impact other projects (including those planned as well as those currently in progress)?

- Will this Technology Architecture be impacted by other projects (including those planned as well as those currently in progress)?

#### 8.3.7. Conduct Formal Stakeholder Review

Check the original motivation for the architecture project and the Statement of Architecture Work against the proposed Technology Architecture, asking if it is fit for the purpose of supporting subsequent work in the other architecture domains. Refine the proposed Technology Architecture only

<!-- page: 103 -->

#### 8.3.8. Finalize the Technology Architecture

- Select standards for each of the building blocks, re-using as much as possible from the reference models selected from the Architecture Repository

- Fully document each building block

- Conduct a final cross-check of overall architecture against business goals; document the rationale for building block decisions in the architecture document

- Document the final requirements traceability report

- Document the final mapping of the architecture within the Architecture Repository; from the selected building blocks, identify those that might be re-used (working practices, roles, business relationships, job descriptions, etc.), and publish via the Architecture Repository

- Finalize all the work products, such as gap analysis

#### 8.3.9. Create/Update the Architecture Definition Document

Document the rationale for building block decisions in the Architecture Definition Document.

Prepare the technology sections of the Architecture Definition Document, comprising some or all of:

- Fundamental functionality and attributes — semantic, unambiguous including security capability and manageability

- Dependent building blocks with required functionality and named interfaces

- Interfaces — chosen set, supplied (APIs, data formats, protocols, hardware interfaces, standards)

- Map to business/organizational entities and policies

If appropriate, use reports and/or graphics generated by modeling tools to demonstrate key views of the architecture. Route the document for review by relevant stakeholders, and incorporate feedback.

### 8.4. Outputs

The outputs of Phase D may include, but are not restricted to:

- Refined and updated versions of the Architecture Vision phase deliverables, where applicable:

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content), updated if necessary

- Validated technology principles, or new technology principles (if generated here)

- Draft Architecture Definition Document (see the TOGAF Standard — Architecture Content), including:

- Baseline Technology Architecture, Approved, if appropriate

- Target Technology Architecture, Approved, including:

  - Technology Components and their relationships to information systems

<!-- page: 104 -->

- Technology platforms and their decomposition, showing the combinations of technology required to realize a particular technology “stack”

- Environments and locations — a grouping of the required technology into computing environments (e.g., development, production)

  - Expected processing load and distribution of load across technology components

  - Physical (network) communications

  - Hardware and network specifications

- Views corresponding to the selected viewpoints addressing key stakeholder concerns

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including such Technology Architecture requirements as:

- Gap analysis results

- Requirements output from Phases B and C

- Updated technology requirements

- Technology Architecture components of an Architecture Roadmap (see the TOGAF Standard — Architecture Content)

The TOGAF Standard — Architecture Content contains a detailed description of architectural artifacts which might be produced in this phase.

### 8.5. Approach

#### 8.5.1. Emerging Technologies

The evolution of new technologies is a major driver for change in enterprises looking for new innovative ways of operating and improving their business. The Technology Architecture needs to capture the transformation opportunities available to the enterprise through the adoption of new technology.

While the Enterprise Architecture is led by business concerns, drivers for change are often found within evolving technology capabilities. As more digital innovations reach the market, stakeholders need to both anticipate and be open to technology-driven change. Part of Digital Transformation has arisen due to the convergence of telecommunications and computer capabilities which have opened up new ways of implementing infrastructures.

Solution development methods are also evolving to challenge traditional development methods and are putting pressure on the shared services and common use benefits of the traditional Enterprise Architecture approach. Without a strong Enterprise Architecture approach, the rapid adoption of changing technologies will cause discontinuities across the enterprise.

<!-- page: 105 -->

The flexibility of the TOGAF ADM enables technology change to become a driver and strategic resource rather than a recipient of Change Requests. As a result, the Technology Architecture may both drive business capabilities and respond to information system requirements at the same time.

#### 8.5.2. Architecture Repository

As part of Phase D, the architecture team will need to consider what relevant Technology Architecture resources are available in the Architecture Repository (see the TOGAF Standard — Architecture Content).

In particular:

- Existing IT services as documented in the IT repository or IT service catalog

- The adopted technical reference model, if applicable

- Generic technology models relevant to the organization’s industry sector

- Technology models relevant to Common Systems Architectures

- The Open Group has a Reference Model for Integrated Information Infrastructure (III-RM) — see the TOGAF® Series Guide: The TOGAF Integrated Information Infrastructure Reference Model (III-RM) — that focuses on the application-level components and underlying services necessary to provide an integrated information infrastructure

<!-- page: 106 -->

## 9. Phase E: Opportunities & Solutions

This chapter describes the process of identifying delivery vehicles (projects, programs, or portfolios) that effectively deliver the Target Architecture identified in previous phases.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00106_img001.png)

*Figure 9-1: Phase E: Opportunities & Solutions*

### 9.1. Objectives

The objectives of Phase E are to:

- Generate the initial complete version of the Architecture Roadmap, based upon the gap analysis and candidate Architecture Roadmap components from Phases B, C, and D

<!-- page: 107 -->

- Determine whether an incremental approach is required, and if so identify Transition Architectures that will deliver continuous business value

- Define the overall Solution Building Blocks (SBBs) to finalize the Target Architecture based on the ABBs

### 9.2. Inputs

This section defines the inputs to Phase E.

#### 9.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

- Product information

#### 9.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

- Communications Plan (see the TOGAF Standard — Architecture Content)

- Planning methodologies

#### 9.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Governance models and frameworks for:

- Corporate Business Planning

- Enterprise Architecture

- Portfolio, Program, Project Management

- System Development/Engineering

- Operations (Service)

<!-- page: 108 -->

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

- Re-usable building blocks

- Publicly available reference models

- Organization-specific reference models

- Organization standards

- Draft Architecture Definition Document, which may include Baseline and/or Target Architectures of any architecture domain

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Architectural requirements

- Gap analysis results (from Business, Data, Application, and Technology Architecture)

- IT Service Management requirements

- Change Requests for existing business programs and projects (see the TOGAF Standard — Architecture Content)

- Candidate Architecture Roadmap components from Phases B, C, and D

### 9.3. Steps

The level of detail addressed in Phase E will depend on the scope and goals of the overall architecture effort.

The order of the steps in Phase E as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance.

All activities that have been initiated in these steps must be closed during the Create the Architecture Roadmap & Implementation and Migration Plan step; see Section 9.3.11.

<!-- page: 109 -->

The steps in Phase E are as follows:

- Determine/confirm key corporate change attributes; see Section 9.3.1

- Determine business constraints for implementation; see Section 9.3.2

- Review and consolidate gap analysis results from Phases B to D; see Section 9.3.3

- Review consolidated requirements across related business functions; see Section 9.3.4

- Consolidate and reconcile interoperability requirements; see Section 9.3.5

- Refine and validate dependencies; see Section 9.3.6

- Confirm readiness and risk for business transformation; see Section 9.3.7

- Formulate Implementation and Migration Strategy; see Section 9.3.8

- Identify and group major work packages; see Section 9.3.9

- Identify Transition Architectures; see Section 9.3.10

- Create the Architecture Roadmap & Implementation and Migration Plan; see Section 9.3.11

#### 9.3.1. Determine/Confirm Key Corporate Change Attributes

This step determines how the Enterprise Architecture can be best implemented to take advantage of the organization’s business culture. This should include the creation of an Implementation Factor catalog (see the TOGAF Standard — Architecture Content) to serve as a repository for architecture implementation and migration decisions. The step also includes assessments of the transition capabilities of the organization units involved (including culture and abilities), and assessments of the enterprise (including culture and skill sets).

The resulting factors from the assessments should be documented in the Implementation Factor catalog. For organizations where Enterprise Architecture is well established, this step can be simple, but the catalog has to be established so that it can be used as an archive and record of decisions taken.

#### 9.3.2. Determine Business Constraints for Implementation

Identify any business drivers that would constrain the sequence of implementation. This should include a review of the business and strategic plans, at both a corporate and line-of-business level, and a review of the Enterprise Architecture Maturity Assessment.

#### 9.3.3. Review and Consolidate Gap Analysis Results from Phases B to D

Consolidate and integrate the gap analysis results from the Business, Information Systems, and Technology Architectures (created in Phases B to D) and assess their implications with respect to potential solutions and inter-dependencies. This should be done by creating a Consolidated Gaps, Solutions, and Dependencies matrix, as shown in the TOGAF Standard — Architecture Content, which will enable the identification of SBBs that could potentially address one or more gaps and their associated ABBs.

<!-- page: 110 -->

The SBBs are created based on the candidate roadmap components from Phases B, C, and D.

If appropriate, investigate different Target Architecture alternatives and discuss these with stakeholders using the Architecture Alternatives and Trade-offs technique (see the TOGAF Standard — ADM Techniques).

Review the Phase B, C, and D gap analysis results and consolidate them in a single list. The gaps should be consolidated along with potential solutions to the gaps and dependencies. A recommended technique for determining the dependencies is to use sets of views such as the Business Interaction matrix, the Data Entity/Business Function matrix, and the Application/Function matrix to completely relate elements from different architecture domains.

Rationalize the Consolidated Gaps, Solutions, and Dependencies matrix. Once all of the gaps have been documented, re-organize the gap list and place similar items together. When grouping the gaps, refer to the Implementation Factor catalog and review the implementation factors. Any additional factors should be added to the Implementation Factor catalog.

#### 9.3.4. Review Consolidated Requirements Across Related Business Functions

Assess the requirements, gaps, solutions, and factors to identify a minimal set of requirements whose integration into work packages would lead to a more efficient and effective implementation of the Target Architecture across the business functions that are participating in the architecture. This functional perspective leads to the satisfaction of multiple requirements through the provision of shared solutions and services. The implications of this consolidation of requirements with respect to architectural components can be significant with respect to the provision of resources. For example, several requirements raised by several lines of business can be resolved through the provision of a shared set of Business Services and Application Services within a work package or project.

#### 9.3.5. Consolidate and Reconcile Interoperability Requirements

Consolidate the interoperability requirements identified in previous phases. The Architecture Vision and Target Architectures, as well as the Implementation Factor catalog and Consolidated Gaps, Solutions, and Dependencies matrix, should be consolidated and reviewed to identify any constraints on interoperability required by the potential set of solutions.

A key outcome is to minimize interoperability conflicts, or to ensure such conflicts are addressed in the architecture. Re-used SBBs, Commercial Off-The-Shelf (COTS) products, and third-party service providers typically impose interoperability requirements that conflict. Any such conflicts must be addressed in the architecture, and conflicts must be considered across all architecture domains (Business, Data, Application, Technology).

There are two basic approaches to interoperability conflicts; either create a building block that transforms or translates between conflicting building blocks, or make a change to the specification of the conflicting building blocks.

<!-- page: 111 -->

#### 9.3.6. Refine and Validate Dependencies

Refine the initial dependencies, ensuring that any constraints on the Implementation and Migration Plans are identified. There are several key dependencies that should be taken into account, such as dependencies on existing implementations of Business Services and Application Services or changes to them. Dependencies should be used for determining the sequence of implementation and identifying the co-ordination required. A study of the dependencies should group activities together, creating a basis for projects to be established. Examine the relevant projects and see whether logical increments of deliverables can be identified. The dependencies will also help to identify when the identified increments can be delivered. Once finished, an assessment of these dependencies should be documented as part of the Architecture Roadmap and any necessary Transition Architectures.

Addressing dependencies serves as the basis for most migration planning.

#### 9.3.7. Confirm Readiness and Risk for Business Transformation

Review the findings of the Business Transformation Readiness Assessment previously conducted in Phase A and determine their impact on the Architecture Roadmap and the Implementation and Migration Strategy. It is important to identify, classify, and mitigate risks associated with the transformation effort. Risks should be documented in the Consolidated Gaps, Solutions, and Dependencies matrix.

#### 9.3.8. Formulate Implementation and Migration Strategy

Create an overall Implementation and Migration Strategy that will guide the implementation of the Target Architecture, and structure any Transition Architectures. The first activity is to determine an overall strategic approach to implementing the solutions and/or exploiting opportunities. There are three basic approaches as follows:

- Greenfield: a completely new implementation

- Revolutionary: a radical change (i.e., switch on, switch off)

- Evolutionary: a strategy of convergence, such as parallel running or a phased approach to introduce new capabilities

Next, determine an approach for the overall strategic direction that will address and mitigate the risks identified in the Consolidated Gaps, Solutions, and Dependencies matrix. The most common implementation methodologies are:

- Quick win (snapshots)

- Achievable targets

- Value chain method

These approaches and the identified dependencies should become the basis for the creation of the work packages. This activity terminates with agreement on the Implementation and Migration Strategy for the enterprise.

<!-- page: 112 -->

#### 9.3.9. Identify and Group Major Work Packages

Key stakeholders, planners, and the Enterprise Architects should assess the missing business capabilities identified in the Architecture Vision and Target Architecture.

Using the Consolidated Gaps, Solutions, and Dependencies matrix together with the Implementation Factor catalog, logically group the various activities into work packages.

Fill in the “Solution” column in the Consolidated Gaps, Solutions, and Dependencies matrix to recommend the proposed solution mechanisms. Indicate for every gap/activity whether the solution should be oriented towards a new development, or be based on an existing product, and/or use a solution that can be purchased. An existing system may resolve the requirement with minor enhancements. For new development this is a good time to determine whether the work should be conducted in-house or through a contract.

Classify every current system that is under consideration as:

- Mainstream: part of the future information system

- Contain: expected to be replaced or modified in the planning horizon (next three years)

- Replace: to be replaced in the planning horizon

Supporting top-level work packages should then in turn be decomposed into increments to deliver the capability increments. Analyze and refine these work packages or increments with respect to their business transformation issues and the strategic implementation approach. Finally, group the work packages into portfolios and projects within a portfolio, taking into consideration the dependencies and the strategic implementation approach.

#### 9.3.10. Identify Transition Architectures

Where the scope of change to implement the Target Architecture requires an incremental approach, then one or more Transition Architectures may be necessary. These provide an ability to identify clear targets along the roadmap to realizing the Target Architecture. The Transition Architectures should provide measurable business value. The time-span between successive Transition Architectures does not have to be of uniform duration.

Development of Transition Architectures must be based upon the preferred implementation approach, the Consolidated Gaps, Solutions, and Dependencies matrix, the listing of projects and portfolios, as well as the enterprise’s capacity for creating and absorbing change.

Determine where the difficult activities are, and unless there are compelling reasons, implement them after other activities that most easily deliver missing capability.

#### 9.3.11. Create the Architecture Roadmap & Implementation and Migration Plan

Consolidate the work packages and Transition Architectures into the Architecture Roadmap, Draft, which describes a timeline of the progression from the Baseline Architecture to the Target

<!-- page: 113 -->

Architecture. The timeline informs the Implementation and Migration Plan. The Architecture Roadmap frames the migration planning in Phase F. Identified Transition Architectures and work packages should have a clear set of outcomes. The Architecture Roadmap must demonstrate how the selection and timeline of Transition Architectures and work packages realizes the Target Architecture.

The detail of the Architecture Roadmap, Draft, should be expressed at a similar level of detail to the Architecture Definition Document developed in Phases B, C, and D. Where significant additional detail is required before implementation the architecture is likely transitioning to a different level. See the TOGAF Standard — Applying the ADM for techniques to manage iteration and different levels of detail.

The Implementation and Migration Plan must demonstrate the activity necessary to realize the Architecture Roadmap. The Implementation and Migration Plan forms the basis of the migration planning in Phase F. The detail of the Implementation and Migration Plan, Draft, must be aligned to the detail of the Architecture Roadmap and be sufficient to identify the necessary projects and resource requirements to realize the roadmap.

When creating the Implementation and Migration Plan there are many approaches to consider, such as a data-driven sequence, where application systems that create data are implemented first, then applications that process the data. A clear understanding of the dependencies and lifecycle of in-place SBBs is required for an effective Implementation and Migration Plan.

Finally, update the Architecture Vision, Architecture Definition Document, and Architecture Requirements Specification with any additional relevant outcomes from this phase.

### 9.4. Outputs

The outputs of Phase E may include, but are not restricted to:

- Refined and updated version of the Architecture Vision phase deliverables, where applicable, including:

- Architecture Vision, including definition of types and degrees of interoperability

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content), updated if necessary

- Draft Architecture Definition Document (see the TOGAF Standard — Architecture Content), including:

- Baseline Business Architecture, Approved, updated if necessary

- Target Business Architecture, Approved, updated if necessary

- Baseline Data Architecture, Approved, updated if necessary

- Target Data Architecture, Approved, updated if necessary

- Baseline Application Architecture, Approved, updated if necessary

- Target Application Architecture, Approved, updated if necessary

- Baseline Technology Architecture, Approved, updated if necessary

<!-- page: 114 -->

- Target Technology Architecture, Approved, updated if necessary

- Transition Architecture, number and scope as necessary

- Views corresponding to the selected viewpoints addressing key stakeholder concerns

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Consolidated Gaps, Solutions, and Dependencies Assessment

- Capability Assessments, including:

- Business Capability Assessment

- IT Capability Assessment

- Architecture Roadmap (see the TOGAF Standard — Architecture Content), including:

- Work package portfolio:

  - Work package description (name, description, objectives)

  - Functional requirements

  - Dependencies

  - Relationship to opportunity

- Relationship to Architecture Definition Document and Architecture Requirements Specification

  - Relationship to any capability increments

  - Business value

  - Implementation Factor catalog

  - Impact

- Identification of Transition Architectures, if any, including:

  - Relationship to Architecture Definition Document

- Implementation recommendations:

  - Criteria measures of effectiveness

  - Risks and issues

  - Solution Building Blocks (SBBs)

- Implementation and Migration Plan, Draft, including:

- Implementation and Migration Strategy

The TOGAF Standard — Architecture Content contains a detailed description of architectural artifacts which might be produced in this phase, describing them in detail and relating them to entities,

<!-- page: 115 -->

### 9.5. Approach

Phase E concentrates on how to deliver the architecture. It takes into account the complete set of gaps between the Target and Baseline Architectures in all architecture domains, and logically groups changes into work packages within the enterprise’s portfolios. This is an effort to build a best-fit roadmap that is based upon the stakeholder requirements, the enterprise’s business transformation readiness, identified opportunities and solutions, and identified implementation constraints. The key is to focus on the final target while realizing incremental business value.

Phase E is the initial step in the creation of the Implementation and Migration Plan which is completed in Phase F. It provides the basis of a well considered Implementation and Migration Plan that is integrated into the enterprise’s portfolio in Phase F.

The following four concepts are key to transitioning from developing to delivering a Target Architecture:

- Architecture Roadmap

- Work Packages

- Transition Architectures

- Implementation and Migration Plan

The Architecture Roadmap lists individual work packages in a timeline that will realize the Target Architecture.

Each work package identifies a logical group of changes necessary to realize the Target Architecture.

A Transition Architecture describes the enterprise at an architecturally significant state between the Baseline and Target Architectures. Transition Architectures provide interim Target Architectures upon which the organization can converge.

The Implementation and Migration Plan provides a schedule of the projects that will realize the Target Architecture.

<!-- page: 116 -->

## 10. Phase F: Migration Planning

This chapter addresses migration planning; that is, how to move from the Baseline to the Target Architectures by finalizing a detailed Implementation and Migration Plan.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00116_img001.png)

*Figure 10-1: Phase F: Migration Planning*

<!-- page: 117 -->

### 10.1. Objectives

- Finalize the Architecture Roadmap and the supporting Implementation and Migration Plan

- Ensure that the Implementation and Migration Plan is co-ordinated with the enterprise’s approach to managing and implementing change in the enterprise’s overall change portfolio

- Ensure that the business value and cost of work packages and Transition Architectures is understood by key stakeholders

### 10.2. Inputs

This section defines the inputs to Phase F.

#### 10.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

#### 10.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

- Communications Plan (see TOGAF Standard — Architecture Content)

#### 10.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Governance models and frameworks for:

- Corporate Business Planning

- Enterprise Architecture

- Portfolio, Program, Project Management

- System Development/Engineering

<!-- page: 118 -->

- Operations (Service)

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

- Re-usable building blocks

- Publicly available reference models

- Organization-specific reference models

- Organization standards

- Draft Architecture Definition Document, which may include Baseline and/or Target Architectures of any architecture domain, and/or Transition Architectures

- Draft Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Architectural requirements

- Gap analysis results (from Business, Data, Application, and Technology Architecture)

- IT Service Management requirements

- Change Requests for existing business programs and projects (see the TOGAF Standard — Architecture Content)

- Architecture Roadmap, Draft (see the TOGAF Standard — Architecture Content), including:

- Identification of work packages

- Identification of Transition Architectures

- Implementation Factor catalog

- Capability Assessment (see the TOGAF Standard — Architecture Content), including:

- Business Capability Assessment

- IT Capability Assessment

- Implementation and Migration Plan, Draft (see the TOGAF Standard — Architecture Content), including the high-level Implementation and Migration Strategy

<!-- page: 119 -->

### 10.3. Steps

The level of detail addressed in Phase F will depend on the scope and goals of the overall architecture effort.

The order of the steps in Phase F as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance.

All activities that have been initiated in these steps must be closed during the “Complete the Architecture Development Cycle and Document Lessons Learned” step; see Section 10.3.7.

The steps in Phase F are as follows:

- Confirm management framework interactions for Implementation and Migration Plan; see Section 10.3.1

- Assign a business value to each work package; see Section 10.3.2

- Estimate resource requirements, project timings, and availability/delivery vehicle; see Section 10.3.3

- Prioritize the migration projects by conducting a cost/benefit assessment and risk assessment; see

### Section 10.3.4

- Confirm Architecture Roadmap and update Architecture Definition Document; see Section 10.3.5

- Complete the Implementation and Migration Plan; see Section 10.3.6

- Complete the architecture development cycle and document lessons learned; see Section 10.3.7

#### 10.3.1. Confirm Management Framework Interactions for the Implementation and Migration Plan

This step is about co-ordinating the Implementation and Migration Plan with the management frameworks within the organization. There are typically four management frameworks that have to work closely together for the Implementation and Migration Plan to succeed:

- Business Planning that conceives, directs, and provides the resources for all of the activities required to achieve concrete business objectives/outcomes

- Enterprise Architecture that structures and gives context to all enterprise activities delivering concrete business outcomes primarily but not exclusively in the IT domain

- Project/Portfolio Management that co-ordinates, designs, and builds the business systems that deliver the concrete business outcomes

- Operations Management that integrates, operates, and maintains the deliverables that deliver the concrete business outcomes

The Implementation and Migration Plan will impact the outputs of each of these frameworks and consequently has to be reflected in them. In the course of this step, understand the frameworks within

<!-- page: 120 -->

the organization and ensure that these plans are co-ordinated and inserted (in a summary format) within the plans of each one of these frameworks.

The outcome of this step may well be that the Implementation and Migration Plan could be part of a different plan produced by another one of the frameworks with Enterprise Architecture participation.

#### 10.3.2. Assign a Business Value to Each Work Package

Establish and assign a business value to each of the work packages. The intent is to first establish what constitutes business value within the organization, how value can be measured, and then apply this to each one of the projects and project increments.

There are several issues to address in this activity:

- Performance Evaluation Criteria are used by portfolio and capability managers to approve and monitor the progress of the architecture transformation

- Return-on-Investment Criteria have to be detailed and signed off by the various executive stakeholders

- Business Value has to be defined as well as techniques, such as the value chain, which are to be used to illustrate the role in achieving tangible business outcomes

Business value will be used by portfolio and capability managers to allocate resources and, in cases where there are cutbacks, business value in conjunction with return on investment can be used to determine whether an endeavor proceeds, is delayed, or is canceled.

- Critical Success Factors (CSFs) should be established to define success for a project and/or project increment

These will provide managers and implementers with a gauge as to what constitutes a successful implementation.

- Measures of Effectiveness (MOE) are often performance criteria and many corporations include them in the CSFs

Where they are treated discretely, it should be clear as to how these criteria are to be grouped.

- Strategic Fit based upon the overall Enterprise Architecture (all tiers) will be the critical factor for allowing the approval of any new project or initiative and for determining the value of any deliverable

Use the work packages as a basis of identifying projects that will be in the Implementation and Migration Plan. The identified projects will be fully developed in other steps in Phase F. The projects, and project increments, may require adjustment of the Architecture Roadmap and Architecture Definition Document.

Risks should then be assigned to the projects and project increments by aggregating risks identified in the Consolidated Gaps, Solutions, and Dependencies Matrix (from Phase E).

<!-- page: 121 -->

Estimate the business value for each project using the Business Value and Risk Matrix (see the TOGAF Standard — Architecture Content).

#### 10.3.3. Estimate Resource Requirements, Project Timings, and Availability/Delivery Vehicle

This step determines the required resources and times for each project and their increments and provides the initial cost estimates. The costs should be broken down into capital (to create the capability) and operations and maintenance (to run and sustain the capability). Opportunities should be identified where the costs associated with delivering new and/or better capability can be offset by decommissioning existing systems. Assign required resources to each activity and aggregate them at the project increment and project level.

#### 10.3.4. Prioritize the Migration Projects by Conducting a Cost/Benefit Assessment and Risk Assessment

Prioritize the projects by ascertaining their business value against the cost of delivering them. The approach is to first determine, as clearly as possible, the net benefit of all of the SBBs delivered by the projects, and then verify that the risks have been effectively mitigated and factored in. Afterwards, the intent is to gain the requisite consensus to create a prioritized list of projects that will provide the basis for resource allocation.

It is important to discover all costs, and to ensure that decision-makers understand the net benefit over time.

Review the risks to ensure that the risks for the project deliverables have been mitigated as much as possible. The project list is then updated with risk-related comments.

Have the stakeholders agree upon a prioritization of the projects. Prioritization criteria will use elements identified in the creation of the draft Architecture Roadmap in Phase E as well as those relating to individual stakeholder agendas. Notice that it is possible for a project to earn a high priority if it provides a critical deliverable on the path to some large benefit, even if the immediate benefit of the project itself is small.

Formally review the risk assessment and revise it as necessary ensuring that there is a full understanding of the residual risk associated with the prioritization and the projected funding line.

#### 10.3.5. Confirm Architecture Roadmap and Update Architecture Definition Document

Update the Architecture Roadmap including any Transition Architectures. Review the work to date to assess what the time-spans between Transition Architecture should be, taking into consideration the increments in business value and capability and other factors, such as risk. Once the capability increments have been finalized, consolidate the deliverables by project. This will result in a revised Architecture Roadmap.

<!-- page: 122 -->

This is needed in order to co-ordinate the development of several concurrent instances of the various architectures. A Transition Architecture State Evolution Table (see the TOGAF Standard — Architecture Content) can be used to show the proposed state of the domain architectures at various levels of detail.

If the implementation approach has shifted as a result of confirming the implementation increments, update the Architecture Definition Document. This may include assigning project objectives and aligning projects and their deliverables with the Transition Architectures to create an Architecture Definition Increments Table (see the TOGAF Standard — Architecture Content).

#### 10.3.6. Complete the Implementation and Migration Plan

Generate the completed Implementation and Migration Plan. Much of the detail for the plan has already been gathered and this step brings it all together using accepted planning and management techniques. This should include integrating all of the projects and activities as well as dependencies and impact of change into a project plan. Any Transition Architectures will act as portfolio milestones.

All external dependencies should be captured and included, and the overall availability of resources assessed. Project plans may be included within the Implementation and Migration Plan.

#### 10.3.7. Complete the Architecture Development Cycle and Document Lessons Learned

This step transitions governance from the development of the architecture to the realization of the architecture. If the maturity of the Architecture Capability warrants, an Implementation Governance Model may be produced (see the TOGAF Standard — Architecture Content).

Lessons learned during the development of the architecture should be documented and captured by the appropriate governance process in Phase H as inputs to managing the Architecture Capability.

The detail of the Architecture Roadmap and the Implementation and Migration Plan should be expressed at a similar level of detail to the Architecture Definition Document developed in Phases B, C, and D. Where significant additional detail is required by the next phase the architecture is likely transitioning to a different level. Depending upon the level of the Target Architecture and Implementation and Migration Plan it may be necessary to iterate another ADM cycle at a lower level of detail. See the TOGAF Standard — Applying the ADM for techniques to manage iteration and different levels of detail.

### 10.4. Outputs

The outputs of Phase F may include, but are not restricted to:

- Implementation and Migration Plan, Approved (see the TOGAF Standard — Architecture Content), including:

- Implementation and Migration Strategy

- Project and portfolio breakdown of the implementation:

<!-- page: 123 -->

  - Allocation of work packages to project and portfolio

  - Capabilities delivered by projects

  - Relationship to Target Architecture and any Transition Architectures

  - Milestones and timing

  - Work breakdown structure

- Project charters (optional):

  - Related work packages

  - Business value

  - Risk, issues, assumptions, dependencies

  - Resource requirements and costs

  - Benefits of migration

  - Estimated costs of migration options

- Finalized Architecture Definition Document (see the TOGAF Standard — Architecture Content), including:

- Finalized Transition Architectures, if any

- Finalized Architecture Requirements Specification (see the TOGAF Standard — Architecture Content)

- Finalized Architecture Roadmap (see the TOGAF Standard — Architecture Content)

- Re-Usable ABBs (see the TOGAF Standard — Architecture Content)

- Requests for Architecture Work (see the TOGAF Standard — Architecture Content) for a new iteration of the ADM cycle (if any)

- Implementation Governance Model (if any) (see the TOGAF Standard — Architecture Content)

- Change Requests for the Architecture Capability arising from lessons learned

### 10.5. Approach

The focus of Phase F is the creation of an Implementation and Migration Plan in co-operation with the project and portfolio managers.

Phase E provides an incomplete Architecture Roadmap and Implementation and Migration Plan that address the Statement of Architecture Work. In Phase F this Roadmap and the Implementation and Migration Plan are integrated with the enterprise’s other change activity.

<!-- page: 124 -->

Activities include assessing the dependencies, costs, and benefits of the various migration projects within the context of the enterprise’s other activity. The Draft Architecture Roadmap, and Draft Implementation and Migration Plan, from Phase E will form the basis of the final Implementation and Migration Plan that will include portfolio and project-level detail.

The architecture development cycle should then be completed and lessons learned documented to enable continuous process improvement.

<!-- page: 125 -->

## 11. Phase G: Implementation Governance

This chapter provides an architectural oversight of the implementation.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00125_img001.png)

*Figure 11-1: Phase G: Implementation*

<!-- page: 126 -->

### 11.1. Objectives

- Ensure conformance with the Target Architecture by implementation projects

- Perform appropriate Architecture Governance functions for the solution and any implementationdriven architecture Change Requests

### 11.2. Inputs

This section defines the inputs to Phase G.

#### 11.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

#### 11.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

- Capability Assessment (see the TOGAF Standard — Architecture Content)

#### 11.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Tailored Architecture Framework (see TOGAF Standard — Architecture Content), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

<!-- page: 127 -->

- Publicly available reference models

- Organization-specific reference models

- Architecture Definition Document (see the TOGAF Standard — Architecture Content)

- Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Architectural requirements

- Gap analysis results (from Business, Data, Application, and Technology Architectures)

- Architecture Roadmap (see the TOGAF Standard — Architecture Content)

- Architecture Governance Framework (see the TOGAF Standard — EA Capability and Governance)

- Implementation Governance Model (see the TOGAF Standard — Architecture Content)

- Architecture Contract (standard) (see the TOGAF Standard — EA Capability and Governance)

- Request for Architecture Work (see the TOGAF Standard — Architecture Content) identified during Phases E and F

- Implementation and Migration Plan (see the TOGAF Standard — Architecture Content)

### 11.3. Steps

The level of detail addressed in Phase G will depend on the scope and goals of the overall architecture effort.

The order of the steps in Phase G as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance.

The steps in Phase G are as follows:

- Confirm scope and priorities for deployment with development management; see Section 11.3.1

- Identify deployment resources and skills; see Section 11.3.2

- Guide development of solutions deployment; see Section 11.3.3

- Perform Enterprise Architecture Compliance reviews; see Section 11.3.4

- Implement business and IT operations; see Section 11.3.5

- Perform post-implementation review and close the implementation; see Section 11.3.6

<!-- page: 128 -->

#### 11.3.1. Confirm Scope and Priorities for Deployment with Development Management

- Review migration planning outputs and produce recommendations on deployment

- Identify Enterprise Architecture priorities for development teams

- Identify deployment issues and make recommendations

- Identify building blocks for replacement, update, etc.

- Perform gap analysis on Enterprise Architecture and solutions framework

The gaps in the existing enterprise solutions framework need to be identified and the specific SBBs required to fill these gaps will be identified by the Solution Architects. These SBBs may have a oneto-one or many-to-one relationship with the projects. The Solution Architects need to define exactly how this will be done. There may be other projects working on these same capabilities and the Solution Architects need to ensure that they can leverage best value from these investments.

- Produce a gap analysis report

#### 11.3.2. Identify Deployment Resources and Skills

The project resources will include the development resources which will need to be educated in the overall Enterprise Architecture deliverables and expectations from the specific development and implementation projects.

The following considerations should be addressed in this step:

- Identify system development methods required for solutions development

Note: There are a range of systems development methods and tools available to the project teams. The method should ideally be able to interoperate with the architecture outputs; for example, generate code from architecture artifacts delivered to date. This could be achieved through the use of modeling languages used for the Enterprise Architecture development that may be captured as inputs to the systems development tools and thereby reduce the cost of solutions development.

- Ensure that the systems development method enables feedback to the architecture team on designs

#### 11.3.3. Guide Development of Solutions Deployment

- Formulate project recommendation

For each separate implementation and deployment project, do the following:

- Document scope of individual project in impact analysis

- Document strategic requirements (from the architectural perspective) in impact analysis

<!-- page: 129 -->

- Document Change Requests (such as support for a standard interface) in impact analysis

- Document rules for conformance in impact analysis

- Document timeline requirements from roadmap in impact analysis

- Document Architecture Contract

- Obtain signature from all developing organizations and sponsoring organization

- Update Enterprise Continuum directory and repository for solutions

- Guide development of business & IT operating models for services

- Provide service requirements derived from Enterprise Architecture

- Guide definition of business & IT operational requirements

- Carry out gap analysis between the Solution Architecture and operations

- Produce Implementation Plan

#### 11.3.4. Perform Enterprise Architecture Compliance Reviews

- Review ongoing implementation governance and Architecture Compliance for each building block

- Conduct post-development reviews

- Close development part of deployment projects

#### 11.3.5. Implement Business and IT Operations

- Carry out the deployment projects including: IT services delivery implementation; business services delivery implementation; skills development & training implementation; communications documentation publication

- Publish new Baseline Architectures to the Architecture Repository and update other impacted repositories, such as operational configuration management stores

#### 11.3.6. Perform Post-Implementation Review and Close the Implementation

- Conduct post-implementation reviews

- Publish reviews and close projects

Closure on Phase G will be when the solutions are fully deployed once.

### 11.4. Outputs

The outputs of Phase G may include, but are not restricted to:

- Architecture Contract (signed) (see the TOGAF Standard — EA Capability and Governance), as recommended in the architecture-compliant implemented architectures

- Compliance Assessments (see the TOGAF Standard — Architecture Content)

<!-- page: 130 -->

- Change Requests (see the TOGAF Standard — Architecture Content)

- Architecture-compliant solutions deployed including:

- The architecture-compliant implemented system

Note: The implemented system is actually an output of the development process. However, given the importance of this output, it is stated here as an output of the ADM. The direct involvement of architecture staff in implementation will vary according to organizational policy, as described in the TOGAF Standard — EA Capability and Governance.

- Populated Architecture Repository

- Architecture compliance recommendations and dispensations

- Recommendations on service delivery requirements

- Recommendations on performance metrics

- Service-Level Agreements (SLAs)

- Architecture Vision, updated post-implementation

- Architecture Definition Document, updated post-implementation

- Business and IT operating models for the implemented solution

- Architecture Building Blocks (ABBs)

### 11.5. Approach

It is here that all the information for successful management of the various implementation projects is brought together. Note that, in parallel with Phase G, there is the execution of an organizationalspecific development process, where the actual development happens.

To enable early realization of business value and benefits, and to minimize the risk in the transformation and migration program, the favored approach is to deploy the Target Architecture as a series of transitions. Each transition represents an incremental step towards the target, and each delivers business benefit in its own right. Therefore, the overall approach in Phase G is to:

- Establish an implementation program that will enable the delivery of the Transition Architectures agreed for implementation during the Migration Planning phase

- Adopt a phased deployment schedule that reflects the business priorities embodied in the Architecture Roadmap

- Follow the organization’s standard for corporate, IT, and Architecture Governance

- Use the organization’s established portfolio/program management approach, where this exists

- Define an operations framework to ensure the effective long life of the deployed solution

<!-- page: 131 -->

Phase G establishes the connection between architecture and implementation organization, through the Architecture Contract.

Project details are developed, including:

- Name, description, and objectives

- Scope, deliverables, and constraints

- Measures of effectiveness

- Acceptance criteria

- Risks and issues

Implementation governance is closely allied to overall Architecture Governance, which is discussed in the TOGAF Standard — EA Capability and Governance.

A key aspect of Phase G is ensuring compliance with the defined architecture(s), not only by the implementation projects, but also by other ongoing projects within the enterprise. The considerations involved with this are explained in detail in the TOGAF Standard — EA Capability and Governance.

<!-- page: 132 -->

## 12. Phase H: Architecture Change Management

This chapter looks at establishing procedures for managing change to the new architecture.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00132_img001.png)

*Figure 12-1: Phase H: Architecture Change Management*

<!-- page: 133 -->

### 12.1. Objectives

- Ensure that the architecture development cycle is maintained

- Ensure that the Architecture Governance Framework is executed

- Ensure that the Enterprise Architecture Capability meets current requirements

### 12.2. Inputs

This section defines the inputs to Phase H.

#### 12.2.1. Reference Materials External to the Enterprise

- Architecture reference materials (see the TOGAF Standard — Architecture Content)

#### 12.2.2. Non-Architectural Inputs

- Request for Architecture Work (see the TOGAF Standard — Architecture Content)

#### 12.2.3. Architectural Inputs

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Tailored Architecture Framework (see the TOGAF Standard — Architecture Content), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture Repository (see the TOGAF Standard — Architecture Content), including:

- Publicly available reference models

<!-- page: 134 -->

- Organization-specific reference models

- Architecture Definition Document (see the TOGAF Standard — Architecture Content)

- Architecture Requirements Specification (see the TOGAF Standard — Architecture Content), including:

- Gap analysis results (from Business, Data, Application, and Technology Architectures)

- Architectural requirements

- Architecture Roadmap (see the TOGAF Standard — Architecture Content)

- Change Request (see the TOGAF Standard — Architecture Content) — technology changes:

- New technology reports

- Asset management cost reduction initiatives

- Technology withdrawal reports

- Standards initiatives

- Change Request (see the TOGAF Standard — Architecture Content) — business changes:

- Business developments

- Business exceptions

- Business innovations

- Business technology innovations

- Strategic change developments

- Change Request (see the TOGAF Standard — Architecture Content) — from lessons learned

- Implementation Governance Model (see the TOGAF Standard — Architecture Content)

- Architecture Contract (signed) (see the TOGAF Standard — EA Capability and Governance)

- Compliance Assessments (see the TOGAF Standard — Architecture Content)

- Implementation and Migration Plan (see the TOGAF Standard — Architecture Content)

<!-- page: 135 -->

### 12.3. Steps

The level of detail addressed in Phase H will depend on the scope and goals of the overall architecture effort.

The order of the steps in Phase H as well as the time at which they are formally started and completed should be adapted to the situation at hand in accordance with the established Architecture Governance.

The steps in Phase H are as follows:

- Establish value realization process; see Section 12.3.1

- Deploy monitoring tools; see Section 12.3.2

- Manage risks; see Section 12.3.3

- Provide analysis for architecture change management; see Section 12.3.4

- Develop change requirements to meet performance targets; see Section 12.3.5

- Manage governance process; see Section 12.3.6

- Activate the process to implement change; see Section 12.3.7

#### 12.3.1. Establish Value Realization Process

Influence business projects to exploit the Enterprise Architecture for value realization (outcomes).

#### 12.3.2. Deploy Monitoring Tools

Ensure monitoring tools are deployed and applied to enable the following:

- Monitor technology changes which could impact the Baseline Architecture

- Monitor business changes which could impact the Baseline Architecture

- Business value tracking; e.g., investment appraisal method to determine value metrics for the business objectives

- Monitor Enterprise Architecture Capability maturity

- Track and assess asset management programs

- Track the Quality of Service (QoS) performances and usage

- Determine and track business continuity requirements

#### 12.3.3. Manage Risks

Manage Enterprise Architecture risks and provide recommendations for IT strategy.

<!-- page: 136 -->

#### 12.3.4. Provide Analysis for Architecture Change Management

Provide analysis for architecture change management:

- Analyze performance

- Conduct Enterprise Architecture performance reviews with service management

- Assess Change Requests and reporting to ensure that the expected value realization and Service- Level Agreement (SLA) expectations of the customers are met

- Undertake a gap analysis of the performance of the Enterprise Architecture

- Ensure change management requests adhere to the Enterprise Architecture Governance and framework

#### 12.3.5. Develop Change Requirements to Meet Performance Targets

Make recommendations on change requirements to meet performance targets and development of position to act.

#### 12.3.6. Manage Governance Process

Manage governance process and framework for architecture:

- Arrange meeting of Architecture Board (or other Governing Council)

- Hold meeting of the Architecture Board with the aim of the meeting to decide on handling changes (technology and business and dispensations)

#### 12.3.7. Activate the Process to Implement Change

Activate the architecture process to implement change:

- Produce a new Request for Architecture Work and request for investment

- Ensure any changes implemented in this phase are captured and documented in the Architecture Repository

### 12.4. Outputs

The outputs of Phase H may include, but are not restricted to:

- Architecture updates (for maintenance changes)

- Changes to architecture framework and principles (for maintenance changes)

- New Request for Architecture Work (see the TOGAF Standard — Architecture Content), to move to another cycle (for major changes)

<!-- page: 137 -->

- Architecture Contract (see the TOGAF Standard — EA Capability and Governance), updated if necessary

- Compliance Assessments (see the TOGAF Standard — Architecture Content), updated if necessary

### 12.5. Approach

The goal of an architecture change management process is to ensure that the architecture achieves its original target business value. This includes managing changes to the architecture in a cohesive and architected way.

This process will typically provide for the continual monitoring of such things as governance requests, new developments in technology, and changes in the business environment. When changes are identified, change management will determine whether to formally initiate a new architecture evolution cycle.

Additionally, the architecture change management process aims to establish and support the implemented Enterprise Architecture as a dynamic architecture; that is, one having the flexibility to evolve rapidly in response to changes in the technology and business environment.

Monitoring business growth and decline is a critical aspect of this phase. Usage of the Enterprise Architecture is the most important part of the architecture development cycle. All too often the business has been left with an Enterprise Architecture that works for the organization of yesterday but may not give back sufficient capability to meet the needs of the enterprise of today and tomorrow.

In many cases the architecture continues to fit, but the solutions underlying them may not, and some changes are required. The Enterprise Architect needs to be aware of these change requirements and considers this an essential part of constant renewal of the architecture.

Capacity measurement and recommendations for planning are a key aspect of this phase. While the architecture has been built to deliver a steady state Business Architecture with agreed capacity during the lifecycle of this Enterprise Architecture, the growth or decline in usage needs to be continually assessed to ensure that maximum business value is achieved.

For example, some Solution Architectures may not lend themselves to be scalable by a large factor — say 10 — or alternative solutions may be more economic when scaled up. While the architecture specifications may not change, the solutions or their operational context may change.

If the performance management and reporting has been built into the work products through previous phases, then this phase is about ensuring the effectiveness of these. If there needs to be additional monitoring or reporting, then this phase will handle the changes.

<!-- page: 138 -->

The value and change management process, once established, will determine:

- The circumstances under which the Enterprise Architecture, or parts of it, will be permitted to change after deployment, and the process by which that will happen

- The circumstances under which the architecture development cycle will be initiated again to develop a new architecture

The architecture change management process is very closely related to the Architecture Governance processes of the enterprise, and to the management of the Architecture Contract (see the TOGAF Standard — EA Capability and Governance) between the architecture function and the business users of the enterprise.

In Phase H it is critical that the governance body establish criteria to judge whether a Change Request warrants just an architecture update or whether it warrants starting a new cycle of the ADM. It is especially important to avoid “creeping elegance”, and the governance body must continue to look for changes that relate directly to business value.

An Architecture Compliance report should state whether the change is compliant to the current architecture. If it is non-compliant, an exemption may be granted with valid rationale. If the change has high impact on the architecture, then a strategy to manage its impact should be defined.

Guidelines for establishing these criteria are difficult to prescribe, as many companies accept risk differently, but as the ADM is exercised, the maturity level of the governance body will improve, and criteria will become clear for specific needs.

#### 12.5.1. Drivers for Change

The main purpose for the development of the Enterprise Architecture so far has been strategic direction and top-down architecture and project generation to achieve corporate capabilities. However, Enterprise Architecture does not operate in a vacuum. There is usually an existing infrastructure and business which is already providing value.

There are also probably drivers for change which are often bottom-up, based upon modifying the existing infrastructure to enhance functionality. Enterprise Architecture changes this paradigm by a strategic top-down approach to a degree, although the delivery of increments makes the equation more complex.

There are three ways to change the existing infrastructure that have to be integrated:

- Strategic, top-down directed change to enhance or create new capability (capital)

- Bottom-up changes to correct or enhance capability (operations and maintenance) for infrastructure under operations management

- Experiences with the previously delivered project increments in the care of operations management, but still being delivered by ongoing projects

<!-- page: 139 -->

Governance will have to handle the co-ordination of these Requests for Change, plus there needs to be a lessons learned process to allow for problems with the recently delivered increments to be resolved and changes made to the Target Architectures being designed and planned.

A lessons learned process ensures that mistakes are made once and not repeated. They can come from anywhere and anyone and cover any aspect of the Enterprise Architecture at any level (strategic, Enterprise Architecture definition, transition, or project). Often an Enterprise Architecture-related lesson may be an indirect outcome of a lesson learned elsewhere in the organization.

The Architecture Board (see the TOGAF Standard — EA Capability and Governance) assesses and approves Requests for Change (RFC). An RFC is typically in response to known problems but can also include improvements. A challenge for the Architecture Board when handling an RFC is to determine whether it should be approved or whether a project in a Transition Architecture will resolve the issue.

When assessing project or solution fit into the architecture, there may also be the case when an innovative solution or RFC drives a change in the architecture.

In addition, there are many technology-related drivers for architecture Change Requests. For example:

- New technology reports

- Asset management cost reductions

- Technology withdrawal

- Standards initiatives

This type of Change Request is normally manageable primarily through an enterprise’s change management and Architecture Governance processes.

In addition, there are business drivers for architecture change, including:

- Business-as-usual developments

- Business exceptions

- Business innovations

- Business technology innovations

- Strategic change

This type of Change Request often results in a complete re-development of the architecture, or at least in an iteration of a part of the architecture development cycle, as explained below.

<!-- page: 140 -->

#### 12.5.2. Enterprise Architecture Change Management Process

The Enterprise Architecture change management process needs to determine how changes are to be managed, what techniques are to be applied, and what methodologies used. The process also needs a filtering function that determines which phases of the architecture development process are impacted by requirements. For example, changes that affect only migration may be of no interest in the architecture development phases.

There are many valid approaches to change management, and various management techniques and methodologies that can be used to manage change; for example, project management methods such as PRINCE2, service management methods such as ITIL, management consultancy methods such as Catalyst, and many others.

An enterprise that already has a change management process in place in a field other than architecture (for example, in systems development or project management) may well be able to adapt it for use in relation to architecture.

The following describes an approach to change management, aimed particularly at the support of a dynamic Enterprise Architecture, which may be considered for use if no similar process currently exists. The approach is based on classifying required architectural changes into one of three categories:

- Simplification change: a simplification change can normally be handled via change management techniques

- Incremental change: an incremental change may be capable of being handled via change management techniques, or it may require partial re-architecting, depending on the nature of the change (see Section 12.5.3 for guidelines)

- Re-architecting change: a re-architecting change requires putting the whole architecture through the architecture development cycle again

Another way of looking at these three choices is to say that a simplification change to an architecture is often driven by a requirement to reduce investment; an incremental change is driven by a requirement to derive additional value from existing investment; and a re-architecting change is driven by a requirement to increase investment in order to create new value for exploitation.

To determine whether a change is simplification, incremental, or re-architecting, the following activities are undertaken:

1. Registration of all events that may impact the architecture

2. Resource allocation and management for architecture tasks

3. The process or role responsible for architecture resources has to make an assessment of what should be done

4. Evaluation of impacts

<!-- page: 141 -->

#### 12.5.3. Guidelines for Maintenance versus Architecture Redesign

A good guideline is:

- If the change impacts two stakeholders or more, then it is likely to require an architecture redesign and re-entry to the ADM

- If the change impacts only one stakeholder, then it is more likely to be a candidate for change management

- If the change can be allowed under a dispensation, then it is more likely to be a candidate for change management

For example:

- If the impact is significant for the business strategy, then there may be a need to redo the whole Enterprise Architecture — thus a re-architecting approach

- If a new technology or standards emerge, then there may be a need to refresh the Technology Architecture, but not the whole Enterprise Architecture — thus an incremental change

- If the change is at an infrastructure level — for example, ten systems reduced or changed to one system — this may not change the architecture above the physical layer, but it will change the Baseline Description of the Technology Architecture; this would be a simplification change handled via change management techniques

In particular, a refreshment cycle (partial or complete re-architecting) may be required if:

- The Foundation Architecture needs to be re-aligned with the business strategy

- Substantial change is required to components and guidelines for use in deployment of the architecture

- Significant standards used in the product architecture are changed which have significant end-user impact; e.g., regulatory changes

If there is a need for a refreshment cycle, then a new Request for Architecture Work must be issued (to move to another cycle).

<!-- page: 142 -->

## 13. ADM Architecture Requirements Management

This chapter looks at the process of managing architecture requirements throughout the ADM.

![插图](C220-Part1e-Architecture%20Development%20Method_images/p00142_img001.png)

*Figure 13-1: ADM Architecture Requirements*

<!-- page: 143 -->

### 13.1. Objectives

The objectives of the Requirements Management phase are to:

- Ensure that the Requirements Management process is sustained and operates for all relevant ADM phases

- Manage architecture requirements identified during any execution of the ADM cycle or a phase

- Ensure that relevant architecture requirements are available for use by each phase as the phase is executed

### 13.2. Inputs

Inputs to the Requirements Management phase are:

- A populated Architecture Repository (see the TOGAF Standard — Architecture Content)

- Organizational Model for Enterprise Architecture (see the TOGAF Standard — Architecture Content), including:

- Scope of organizations impacted

- Maturity assessment, gaps, and resolution approach

- Roles and responsibilities for architecture team(s)

- Constraints on architecture work

- Budget requirements

- Governance and support strategy

- Tailored Architecture Framework (see the TOGAF Standard — Architecture Content), including:

- Tailored architecture method

- Tailored architecture content (deliverables and artifacts)

- Configured and deployed tools

- Statement of Architecture Work (see the TOGAF Standard — Architecture Content)

- Architecture Vision (see the TOGAF Standard — Architecture Content)

- Architecture requirements, populating an Architecture Requirements Specification (see the TOGAF Standard — Architecture Content)

- Requirements Impact Assessment (see the TOGAF Standard — Architecture Content)

<!-- page: 144 -->

### 13.3. Steps

The steps in the Requirements Management phase are described in the table below:

|  |  | Requirements Management Steps | ADM Phase Steps |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
|  | Step 1 |  | Identify requirements (typically by analyzing how<br>business goals/objectives can be met through the<br>design of value streams, business scenarios, user<br>experiences, or the provision of management |  |  |  |
| information) and document them in the<br>Architecture Requirements Specification and<br>Requirements Repository.<br>Step 2 Establish baseline requirements: determine<br>priorities, confirm stakeholder agreement to<br>priorities, and document them in the Architecture<br>Requirements Specification and Requirements<br>Repository.<br>Step 3 Monitor baseline requirements.<br>Step 4 Identify new and changed requirements:<br>a. Remove or re-assess priorities<br>b. Add requirements and re-assess priorities<br>c. Modify existing requirements |  |  | experiences, or the provision of management<br>information) and document them in the<br>Architecture Requirements Specification and<br>Requirements Repository. |  |  |  |
|  | Step 2 | Establish baseline requirements: determine<br>priorities, confirm stakeholder agreement to<br>priorities, and document them in the Architecture<br>Requirements Specification and Requirements<br>Repository. |  |  |  |  |
|  | Step 3 | Monitor baseline requirements. |  |  |  |  |
|  | Step 4 |  | Identify new and changed requirements:<br>a. Remove or re-assess priorities<br>b. Add requirements and re-assess priorities<br>c. Modify existing requirements |  |  |  |

<!-- page: 145 -->

|  |  | Requirements Management Steps | ADM Phase Steps |  |
| --- | --- | --- | --- | --- |
|  | Step 5 | Identify changed requirements and record<br>priorities:<br>a. Identify changed requirements and ensure the<br>requirements are prioritized by the architect(s)<br>responsible for the current phase, and by the<br>relevant stakeholders<br>b. Record new priorities | d |  |
|  |  | c. Ensure that any conflicts are identified and<br>managed through the phases to a successful<br>conclusion and prioritization<br>d. Generate Requirements Impact Assessment (see<br>the TOGAF Standard — Architecture Content)<br>for steering the architecture team<br>Notes<br>• Changed requirements can come in through any<br>route<br>To ensure that the requirements are properly<br>assessed and prioritized, this process needs to<br>direct the ADM phases and record the decisions<br>related to the requirements.<br>• The Requirements Management phase needs to<br>determine stakeholder satisfaction with the<br>decisions<br>Where there is dissatisfaction, the phase<br>remains accountable to ensure the resolution of<br>the issues and determine next steps. | e<br>y<br>y<br>o<br>s<br>e<br>of |  |
|  | Step 6 |  | a. Assess impact of changed requirements on<br>current (active) phase<br>b. Assess impact of changed requirements on<br>previous phases<br>c. Determine whether to implement change, or<br>defer to later ADM cycle; if decision is to<br>implement, assess timescale for change<br>management implementation |  |
|  |  |  | d. Issue Requirements Impact Assessment, Version<br>n +1 |  |

<!-- page: 146 -->

|  |  | Requirements Management Steps | ADM Phase Steps |  |
| --- | --- | --- | --- | --- |
|  | Step 7 |  | Implement requirements arising from Phase H.<br>The architecture can be changed through its<br>lifecycle by the Architecture Change Management<br>phase (Phase H). The Requirements Management<br>process ensures that new or changing requirements<br>that are derived from Phase H are managed<br>accordingly. |  |
| Step 8 Update the Architecture Requirements Repository<br>with information relating to the changes requested,<br>including stakeholder views affected.<br>Step 9 Implement change in the current phase.<br>Step 10 Assess and revise gap analysis for past phases.<br>The gap analysis in the ADM Phases B through D<br>identifies the gaps between Baseline and Target<br>Architectures. Certain types of gap can give rise to<br>gap requirements.<br>The ADM describes two kinds of gap:<br>• Something that is present in the baseline, but<br>not in the target (i.e., eliminated — by accident<br>or design)<br>• Something not in the baseline, but present in<br>the target (i.e., new)<br>A “gap requirement” is anything that has been<br>eliminated by accident, and therefore requires a<br>change to the Target Architecture.<br>If the gap analysis generates gap requirements, then<br>this step will ensure that they are addressed,<br>documented, and recorded in the Architecture<br>Requirements Repository, and that the Target<br>Architecture is revised accordingly.<br>13.4. Outputs<br>The outputs of the Requirements Management process may include, but are not restricted to: | Step 8 | Update the Architecture Requirements Repository<br>with information relating to the changes requested,<br>including stakeholder views affected. |  |  |
|  | Step 9 |  | Implement change in the current phase. |  |
|  | Step 10 |  | Assess and revise gap analysis for past phases.<br>The gap analysis in the ADM Phases B through D<br>identifies the gaps between Baseline and Target<br>Architectures. Certain types of gap can give rise to<br>gap requirements.<br>The ADM describes two kinds of gap:<br>• Something that is present in the baseline, but<br>not in the target (i.e., eliminated — by accident<br>or design)<br>• Something not in the baseline, but present in<br>the target (i.e., new)<br>A “gap requirement” is anything that has been<br>eliminated by accident, and therefore requires a<br>change to the Target Architecture.<br>If the gap analysis generates gap requirements, then<br>this step will ensure that they are addressed,<br>documented, and recorded in the Architecture<br>Requirements Repository, and that the Target<br>Architecture is revised accordingly. |  |

- Requirements Impact Assessment (see the TOGAF Standard — Architecture Content)

- Updated Architecture Requirements Specification (see the TOGAF Standard — Architecture Content: Architecture Requirements Specification), if necessary

<!-- page: 147 -->

The TOGAF Standard — Architecture Content contains a detailed description of architectural artifacts which may be produced in this phase, describing them in detail and relating them to entities, attributes, and relationships in the TOGAF Enterprise Metamodel.

The Architecture Requirements Repository will be updated as part of the Requirements Management phase and should contain all requirements information.

When new requirements arise, or existing ones are changed, a Requirements Impact Assessment is generated, which identifies the phases of the ADM that need to be revisited to address the changes. The statement goes through various iterations until the final version, which includes the full implications of the requirements (e.g., costs, timescales, and business metrics) on the architecture development. Once requirements for the current ADM cycle have been finalized then the Architecture Requirements Specification should be updated.

### 13.5. Approach

#### 13.5.1. General

As indicated by the “Requirements Management” circle at the center of the ADM graphic, the ADM is continuously driven by the Requirements Management process.

It is important to note that the Requirements Management circle denotes not a static set of requirements, but a dynamic process whereby requirements for Enterprise Architecture and subsequent changes to those requirements are identified, stored, and fed into and out of the relevant ADM phases, and also between cycles of the ADM.

The ability to deal with changes in requirements is crucial. Architecture is an activity that by its very nature deals with uncertainty and change — the “grey area” between what stakeholders aspire to and what can be specified and engineered as a solution. Architecture requirements are therefore invariably subject to change in practice. Moreover, architecture often deals with drivers and constraints, many of which by their very nature are beyond the control of the enterprise (changing market conditions, new legislation, etc.), and which can produce changes in requirements in an unforeseen manner.

Note also that the Requirements Management process itself does not dispose of, address, or prioritize any requirements; this is done within the relevant phase of the ADM. It is merely the process for managing requirements throughout the overall ADM.

It is recommended that an Architecture Requirements Repository (see the TOGAF Standard — Architecture Content) is used to record and manage all architecture requirements. Unlike the Architecture Requirements Specification, and the Requirements Impact Assessment, the Architecture Requirements Repository can hold information from multiple ADM cycles.

<!-- page: 148 -->

#### 13.5.2. Requirements Development

The first high-level requirements are articulated as part of the Architecture Vision, generated by means of the business scenario or analogous technique.

Each phase of the ADM, from Preliminary to Phase H, must select the approved requirements for that phase as held in the Architecture Requirements Repository and Architecture Requirements Specification. At the completion of the phase the status of all such requirements needs to be updated. During the phase execution, new requirements generated for future architecture work within the scope of the current Statement of Architecture Work need to be documented within the Architecture Requirements Specification, and new requirements which are outside of the scope of the current Statement of Architecture Work must be input to the Architecture Requirements Repository for management through the Requirements Management process.

In each relevant phase of the ADM the architect should identify types of requirement that must be met by the architecture, including applicable:

- Functional requirements

- Non-functional requirements

When defining requirements the architect should take into account:

- Assumptions for requirements

- Constraints for requirements

- Domain-specific principles that drive requirements

- Policies affecting requirements

- Standards that requirements must meet

- Organization guidelines for requirements

- Specifications for requirements

Deliverables in later ADM phases also contain mappings to the design requirements, and may also generate new types of requirements (for example, conformance requirements, time windows for implementation).

#### 13.5.3. Resources

The world of requirements engineering is rich with emerging recommendations and processes for Requirements Management. The TOGAF Standard does not mandate or recommend any specific process or tool; it simply states what an effective Requirements Management process should achieve (i.e., the “requirements for requirements”, if you like).

<!-- page: 149 -->

##### 13.5.3.1. Business Scenarios

A technique used to analyze how a business goal or objective can be met by a process or value stream. Analyzing where the activities in that process are performed by human and computer actors is a highly effective way to identify and clarify architecture requirements. The technique is detailed in the TOGAF® Series Guide: Business Scenarios.

##### 13.5.3.2. Requirements Tools

There is a large, and increasing, number of Commercial Off-The-Shelf (COTS) tools available for the support of Requirements Management, albeit not necessarily designed for architecture requirements.

<!-- page: 150 -->

## Index

A

| ADM, 1, 2, 25 | Implementation Governance, 110 |
| --- | --- |
| ADM Architecture Requirements Management, | Information Mapping, 53 |
| 127 | Information Systems Architectures, 56 |
| Application Architecture, 69 | M |
| architecture | management frameworks, 26 |
| scoping, 8 | Migration Planning, 101 |
| Architecture Change Management, 117 | N |
| Architecture Development Method, 1 | NASCIO, 28 |
| architecture domains, 11 | O |
| Architecture Governance, 7, 24 | operations management, 27 |
| architecture integration, 13 | Opportunites & Solutions, 91 |
| architecture partition, 8 | Organization Mapping, 52 |
| Architecture Principles, 24, 38 | Organization Maps, 39 |
| Architecture Vision, 5, 33 | P |
| audit information, 7 | Phase A, 29 |
| B | Phase C, 57 |
| Balanced Scorecard technique, 20 | Phase E, 91 |
| breadth | Phase F, 102 |
| enterprise, 8, 9 | Phase G, 111 |
| Business Architecture, 41 | Phase H, 118 |
| business capabilities, 33, 39, 51 | Preliminary Phase, 16 |
| business planning, 27 | process status, 7 |
| business principles, 24 | process tailoring, 19 |
| C | project management, 27 |
| content tailoring, 20 | R |
| D | Requirement for Architecture Work, 24 |
| Data Architecture, 58 | Requirements Management, 128 |
| enterprise, 8, 10 | S |
| Enterprise, 23 | T |
| Enterprise Continuum, 1 | Target Architecture Description, 11 |

<!-- page: 151 -->

Technology Architecture, 79 terminology tailoring, 19 time period enterprise, 8, 10 TOGAF ADM, 1 tools standardization, 20 Transition Architecture Description, 11

V value streams, 39, 52

Z Zachman Framework, 5
