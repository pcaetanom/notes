
Copy pasta draft from txt

########################################################################################
EN 62304 - SOP 18 - Software Product Development
########################################################################################
---------------------------
Customer Requirements:
(Medical-device) user needs, defined as 'validatable'
parameters to then use as design input.

---------------------------
Requirements Specification:

In EN 62304 this is referred to as the System Requirements Specification. It is comprised of:
    - Customer Requirements
    - Business Requirements
    - Regulatory Requirements
    - Risk Control Measures
    
The Software Product verification is conducted against these requirements.

---------------------------
SwRS
Software Requirements Specification
High-level description of the behaviour required from the software. This is in the form of both
functional and non-functional requirements for the software.
Design Validation is conducted against these requirements.
The SwRS is a subset of the Requirements Specification.
---------------------------

########################################################################################
---------------------------
Design Review
Design reviews are intended to:
· provide a systematic assessment of design results, including the device design and the
associated designs for production and support processes;
· provide feedback to designers on existing or emerging problems;
· assess project progress; and/or
· provide confirmation that the project is ready to move on to the next stage of development.
The design review should include at least one individual who does not have direct responsibility
for the design phase under review.

---------------------------
Design verification

Objective: Provide evidence that specified requirements have been fulfilled
Scope: elements of a product
Base: Sub-system Software Requirements specification

---------------------------
Design validation
Objective: Provide evidence that device specifications conform to user needs and
intended use(s)
Scope: elements of the product
Base: System Software Requirements specification?

---------------------------
Product verification
Objective: Provide evidence that specified requirements have been fulfilled
Scope: Finished product
Base: System Requirements Specification

---------------------------
Product validation
Objective: Provide evidence that device specifications conform to user needs and
intended use(s)
Scope: finished product
Base: User Requirements
---------------------------

########################################################################################

---------------------------
Technical File / Design Dossier
Objective: Demonstrates conformity of the design and development of a product to the Medical Device
Directive.

---------------------------
Design History File (DHF)

A compilation of records, which describes the Design History of a finished device. The DHF shall
contain or refer to records that show that the design was developed in accordance with the
approved plan and the company procedures.

---------------------------
PMP Project Management Plan
A narrative document which explains how the project is to be undertaken.

---------------------------
SwDP
Software Development Plan
A plan for conducting the activities of the software development process appropriate to the
scope, magnitude, and software safety classifications of the software system to be developed.
---------------------------

########################################################################################

#  Planning 


KEY CONCEPT >>>>>>>>>>>>>>>>>>>>>>>>

5 phases
    1. Business research and capturing customer requirements
    2. Defining design inputs and planning development
    3. Generating design output (Software Design and Development)
    4. Product verification and validation
    5. Product launch
    
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
    
Phase planning is captured in PMP.

PMP should contain:

    a. Phase Purpose – Gives a short bullet point list of the key objectives of the phase
    b. V-model – Shows the part of the V-model covered by the phase and any lower level V-models that
        apply
    c. Activity Swim-lanes – Who is doing what within this phase
    d. Activity Details – Detailed information on what is involved in each activity and where supporting
        information is available
    e. Design review – Guidance on the content of and expected project state ahead of the end of phase
        design review. This sub-section also provides guidance on how to format the documents produced,
        where to find out what should go in them and where they should be stored following approvals

########################################################################################

# Phase 1 - Business research and capturing customer requirements

a. Purpose

    - Problem to be solved
    - Business case
    - Customer Requirements
    - Project team and Project Management Plan
    - To identify all stakeholders and their importance

b. --
c. --

d. Activity Details

    - Proposal: 
        An Opportunity Proposal must be completed for new projects, but is an optional activity when conducting scheduled maintenance to an existing product.
        
    - Project Planning: 
        A Project Management Representative is appointed and a core project team is formed, including Marketing, Design, Purchasing, Production and Regulatory Affairs. All sections of a PMP are populated but the Plan is not formally issued.
        
    - Customer Requirements: Output to User Requirements (UR) document.
        UR is prioritised and reviewed for {completeness, correctness, self-consistency, 'validability'}. The customer or representative must be consulted. The UR will evolve and be refined throughout the project AND the changes will be communicated to all those involved.
        
    - Impact Assessment: Section A of a 'Feasibility Review Form' for Potential Software Product Change (FRF) is completed for each
        proposed feature/change (if applicable), this activity allows an initial impact assessment to be conducted this allows to more fully understand the implication of approving the work.

e. Design Review 

    Phase #1 checklist:
    - Review the Customer requirements to ensure they are valid
    - Check that the Customer requirements are sufficiently complete and well understood
    - Check that all inputs to this review are in the correct state (see table below)
    - Ensure the wider use environment is known so that compatibility issues can be taken into account
    - Review project schedule and resource estimates

    
########################################################################################

# Phase 2 - Defining design inputs and planning development


a. Purpose

    - Design concepts leading to the selection of the product concept to be developed
    - Requirements specification
    - Detailed plan for the development of the product
    - Regulatory Strategy
    - Marketing Strategy

b. --
c. --

d. Activity Details

    - Project Planning:
        Update PMP to include timescales for development, project risks and expected deliverables. 
        Create a 'Software Development Plan' (SwDP) and populated with best known information. Software development items will be documented in the SwDP.
        Create a 'Software Tool Validation Plan' (SwTVP) which identifies and plans the use/validation of any
        software tools that are to be used.
        Create a 'Configuration Management Plan' (CMP must be complete and approve by the end of this phase)

    - Risk Management: 
        Create a Risk Management Plan (RMP) and 'User Risk Assessment' (URA) with a focus on users, customers and in particular patient safety. 
        (RMP must be complete and approve by the end of this phase)
        An initial assessment of the software safety classification shall be performed.

    - Regulatory Compliance:
        Create Regulatory Strategy, consider intended markets, compliance requirements, product classifications and possible routes to approvals (complete and approve by the end of this phase). If CE marked, start 'Essential Requirements for the Medical Device Directive', which requirements are relevant justifying the ones that are not, for non-relevant ones, add references to the design process standards.
        If not CE mark, detail other necessary regulatory considerations 
    
    - Requirements Specification:
        Create Requirements Specification (RS) (must complete and approve by the end of this phase)
        In EN 62304 -> alias "system requirements specification", It is comprised of:
            a. Customer Requirements
            b. Business Requirements
            c. Regulatory Requirements
            d. Risk Control Measures –> outputs from the initial risk assessment
            
        The Software Requirements Specification (SwRS) is a subset of the RS (must start at in this phase).


    - Product Verification and Validation (V&V)
        Create a Product Verification Plan (PVerP) (must be complete in this phase)- confirms the product satisfies the RS.
        Create a Product Validation Plan (PVaP) (must be complete in this phase)- confirms the product satisfies the UR, 
        (PVaP should be updated if the UR changes)
        Ideally include a Usability study, as part of the product V&V planning.
        Create Product V&V protocols to provide a means of implementing the PVerP and PVaP.

    - Marketing
        Include/create - Marketing info - competitor analysis, benchmarking, patentable features, product
        costs, selling prices, forecast unit sales, marketing collateral plan

    - Supply Chain Development
        Create 'Project Commercial Analysis' - Purchasing representative -> identify potential material/component vendors. Assess risks (supply, quality and capability) and quotations.
    
    - Concept design study
        May conduct 'Concept feasibility' studies to understand product development implementation -> output -> Concept Feasibility Summary Report (CFSR).
        The CFSR should be used to justify the decisions made to adopt certain technologies or approaches.
        Any concept feasibility work carried out should be complete and approved by the end of this phase.

e. Design Review 

    Phase #2 checklist:
    - Review the status of all actions raised against the project
    - Discuss any changes to the status of the project since the previous design review
    - Check that all inputs to this review are in the correct state
    - Ensure the wider use environment is known so that compatibility issues can be taken into account
    - Confirm that safety, reliability, service and maintenance requirements are known
    - Ensure that the regulatory requirements are considered
    - Consider aspects of risk analysis
    - Discuss any problems and propose solutions


########################################################################################

# Phase 3 -


a. Purpose
    - Conduct the detailed software design and development
    - Conduct the software design verification and validation
    - Conduct the initial design and verification of the production processes driving design decisions
    - Complete all design outputs required to freeze the design prior to product verification and validation

b. --
c. --

d. Activity Details

    - Project Planning:
        PMP - update and reassess timescales and project risks.
        SwDP - complete with detailed planning of the design activities
        Software tools are validated in accordance with the SwTVP and a Software Tool Validation Report is
        created (must be complete in this phase).

    - Risk Management:
        Continue process in accordance with the RMP. Refine mitigation strategies into lower level as design requirements.
        Technical Lead Representative or Project Management Representative should assess issues raised by Design team and propagate into RMP and requirements if appropriate. (Risk assessment should be complete in this phase)

    - Regulatory Compliance
        Start 'Clinical Evaluation', may include identifying and compiling the evidence required for clinical trial applications.

    - Product Verification and Validation
        Product V&V Protocols are completed and approved by the end of this phase, as well as, a Usability Study Plan (&& Usability Study Protocols).
        Start Instructions For Use (IFU) and Product Labelling where applicable.
        
    - Design:
    Create and complete a Design V&V Plan - must provide clear evidence that the software requirements have been
    satisfied. Must maintain traceability between SwRS and design V&V activities throughout development. SwRS may be
    updated but both DV&V and SwRS should be complete and approved prior to design verification and validation activities.
    Third Party Software Components (TPSC) must be managed based on SOP19 - Third Party Component Validation.
    Also need to raise Third Party Component Validation Forms (must be complete in this phase)
    
    - Design Verification and Validation:    
        Need to have a Test Readiness Review (TRR) before starting design verification and validation activities. The
        software baseline is defined, the design V&V protocol(s) is complete, and the software is ready
        for the formal design verification and validation to be conducted. A TRR will include a review of:
            - Any open items from previous reviews and audits
            - Changes to the development plans & definition documents
            - Changes to the RS and the cascade of the resulting changes through the design/document set
            - The risk analysis to ensure that it has been taken into account in the design
            - Design V&V Protocol(s)
            - Open bug list
            - Any uncompleted development items

        Inputs to the TRR:
        - RS
        - SwRS
        - Design documents
        - Traceability matrix
        - Design V&V Protocol(s)
        - Risk analyses

        Outputs of the TRR:
        - Review minutes, including a statement on whether to conduct the formal Design Verification and Validation activities.

        Execute Design V&V Protocol and produce Design V&V Report(s) (must complete in this phase). These activity provide evidence that the SwRS has been satisfied.

        The traceability matrix will link the SwRS to the design V&V activities to demonstrate
        that all software requirements have been tested. The Traceability of Software Requirements and Test
        Cases document must be complete and approved in this phase.

    - Software Development Summary Report:
        Create/complete/approve a Software Development Summary Report (SwDSR)to summarise SwDP work must include justifications behind any/all deviations from the SwDP.

    - Supply Chain Development:
        The purchasing representative continues same as phase 2

    - Production:
        The 'Manufacturing or Assembly Strategy' is created covering production of the device, process requirements, work instructions/training needs.
        The 'Installation, Service and Maintenance Strategy' is created, covering installation of the device, services available, frequency of maintenance visits, work instructions/training needs. Also consider product support in the field when components (from vendors) reach end-of-life.
    
    Marketing:
        The Marketing Strategy continues to update same as phase 2
        
e. Design Review 

    Phase #3 checklist:
    
    - Review the status of all actions raised against the project
    - Discuss any changes to the status of the project since the previous design review
    - Check that all inputs to this review (including the TRR minutes) are in the correct state
    - Ensure the wider use environment is known so that compatibility issues can be taken into account
    - Confirm that safety, reliability, service and maintenance requirements are known
    - Ensure that all regulatory requirements are considered
    - Consider aspects of risk analysis
    - Discuss any problems and propose solutions

########################################################################################

# Phase 4 - Product Verification and Validation

a. Purpose

    - Complete full product verification and validation
    - Gain agreement to transfer into production
    - Gain agreement to submit product for regulatory approval
    - Residual risk analysis and risk-benefit statement

b. --
c. --

d. Activity Details

    - Project Planning:
        Update PMP with timescales and define how new project risks are managed
        
    - Risk Management:
        Update same as previous phase. When Product V&V is complete create 'Anomaly list risk assessment'.
        If required a customer facing anomaly list should also be created.

    - Product V&V:
        Complete/approve IFU, complete/approve 'Usability File' (according to 'Usability Study Plan')
        Execute V&V protocol and create/approve Product V&V Report(s).
        
    - Post-Market Surveillance Plan:    
        Start/Create PMSP
        
    - Regulatory Compliance:
        Complete/approve {Clinical Evaluation, Essential Requirements} and includede in Technical File/Design Dossier.
        Start 'Regulatory submission' with Technical File/Design Dossier or with Summary Technical Document (STED)
        
    - Production:
        Establish production proccesses; complete Work instructions; create/complete BOM lists; 
        
    - Installation:
        develop in-field service processes. Create Service and Maintenance Strategy + Field Service work instructions
    
    - Marketing:
        The Marketing Strategy continues to update same as phase 3
    
    - Supply Chain Development:
        Transfer supplier info from Suplly chain Dev to Production
        Update Project Commercial analysis (must complete in this phase)
    
e. Design Review 

    Phase #4 checklist:
    
    - Review the status of all actions raised against the project
    - Discuss any changes to the status of the project since the previous design review
    - Check that all inputs to this review are in the correct state
    - Confirm that safety, reliability, service and maintenance requirements are known and have been met
    - Ensure that all regulatory requirements have been met
    - Ensure that all risk management activities are complete including the risk benefit statement
    - Discuss any problems and propose solutions    


########################################################################################

# Phase 5 - Product Launch

a. Purpose

    - Complete transfer into production
    - Make Regulatory Submission
    - Launch product for sale
    - Enter post market surveillance

b. --
c. --

d. Activity Details

    - Post-Market Surveillance Plan:    
        Complete/approve.
    
    - Marketing
        Complete/approve marketing materials, Product training materials, price lists
    
    - Regulatory submission
        Create 'Declaration of Conformity'. Update Technical File/Design Dossier or STED and submit for regulatory approval.
        Issue 'Declaration of Conformity'after approval.
    
    - Product Launch
        Issue 'Technical change' for manufacturing/production systems
        Issue 'Production Control' forms
        Start PMS activity
        Review Risk Management File agains PMS data
        Update Manufacturing System {parts costings; safe stock levels}
    - Project Management
        Complete/approve PMP
        Formally close 'Design History File'
        Close all actions in 'Action Tracking Log', if not closed provide rationale
        Conduct 'Project Document Configuration Audit', define configuration baseline
        Conduct project Post-Mortem if applicable 
        
e. Design Review 

    Phase #4 checklist:
    
    - Review the status of all actions raised against the project
    - Discuss any changes to the status of the project since the previous design review
    - Check that all inputs to this review are in the correct state
    - Ensure that all regulatory requirements have been met and the product is ready for submission
    - Materials required to support the sales and manufacturing of the product are complete
        
########################################################################################
#//////////////////////////////////////////////////////////////////////////////////////#
#//////////////////////////////////////////////////////////////////////////////////////#
########################################################################################

########################################################################################

EN 62304 - WI48 - Software [ Product Requirements / System Requirements ] 

########################################################################################

---------------------------
Software Unit

A software item that is not subdivided into other items for configuration management or
testing purposes.

---------------------------
Software Item

An element of the software. The term is generic and can be used to mean: a single
software unit, any grouping of software units or the entire software system.

---------------------------
Software Requirement Specification (SRS)

The Software Requirement Specification (SRS) is a subset of the SysRS. The SRS is a
description of the software behaviour. This is in the form of both functional and nonfunctional
requirements for the software.

---------------------------
COTS - Commercial Off-The-Shelf Software.

---------------------------
SOUP - Software Of Unknown Provenance. A software item that is already developed and that has
not been developed for the purpose of being incorporated into the Medical device or
software previously developed for which adequate records of the development processes
are not available.

---------------------------

########################################################################################

Sources of 
    Product Requirements OR
    System Requirements
    
    1. Customer Requirements
    2. Business Requirements
    3. Regulatory Requirements
    4. Risk Control Measures

1. Customer/User Requirements - UR
    When: during lifecycle phase 1 
    Source: One/Many customers OR subject matter expert (surrogate customer)
    Types:
    - Functional UR - 'what the device must do'
    - Performance UR - 'how well the device must do'
    
2. Business Requirements
    When: during lifecycle phase 2 
    Source: Management team
    
3. Regulatory Requirements
    When: during lifecycle phase 2
    Source: Regulatory bodies from the intended market's territory 
    -> NB Software requirements must comply with EN62304

4. Risk Control Measures
    When: during lifecycle phase 2, and iterated on from phase 2 onwards
    Source: proj stakeholders -> risk analysis
    
---------------------------

-> 'Requirements change' Can originate from any stakeholder, must implement FM71 (Feasibility review form)


-> 'Requirements Management' and 'Change Authority' stakeholders ('Change Board') should be defined in PMP (may vary proj to proj). These may also vary depending on cost/impact threshold levels. (Low/Medium/High)

---------------------------
########################################################################################
---------------------------
Sys Requirements Capture

Attributes for each Sys Req:
    - Unique Identifier (UUID?)
    - Source of the requirement.
    - Type of requirement (customer, business, regulatory or risk control measure).
    - Requirement description.
    - Reference to Verification and Validation (V&V) method(s) covering this requirement.
    - Rationale for the requirement (only mandatory at top level requirements e.g. UR).

Sys Req review Checklist:
    - Unique – requirements should not be duplicated.
    - Concise – each requirement should be expressed in as few words as practicable.
    - Unambiguous – there should be no doubt over the meaning.
    - Non-contradictory – there should be no conflict between requirements
    - Justified – each requirement must be there for a valid reason.
    - Measurable

---------------------------
-> Must define functional and performance requirements for SOUP/COTS items

---------------------------
-> Apply risk assessment to initial Sys Req.

---------------------------
-> 'Refinement' process is required in phase 2 to create Sys Req Spec -> from Sys Req source

---------------------------

########################################################################################
---------------------------
Requirement Change Control Process (FM71) 

    >> Should include:

    - Change request detail
    - Impact analysis
        - A description of the change
        - Items (artefacts) that will be changed 
        - How the change will be funded
        - Effect on the risk analysis
        - Effect on other requirements
        - Documentation that will be impacted
        - Effect on other areas of the product/software
    - Reviewer recommendation (e.g. change is approved, rejected, deferred)
    - Decision on recommendation
    - Implementation
    - Docs changeset
    - Close change request

---------------------------
-> Software Maintenance - Feasibility review form for potential software change

---------------------------
########################################################################################

---------------------------
Records - aka outputs from the Sys Requirement process:
-> UR
-> System Requirement Spec
-> Software Requirements specification
-> Risk assessment records
-> FM71 (change requests)

---------------------------

########################################################################################
#//////////////////////////////////////////////////////////////////////////////////////#
#//////////////////////////////////////////////////////////////////////////////////////#
########################################################################################

########################################################################################

EN 62304 - SOP19 - Third Party Software Component Validation

########################################################################################
---------------------------
2x types of TPSC:
    - SW Tools used in development and production of a device
    - SW components developed outside the project which are include/integrated in the device

---------------------------

FM142 - third party software component form 
    - product line were TPSC is intended to be used;
    - TPSC name;
    - TPSC manufacturer;
    - TPSC identifier (include part number, version, release date, patch number and/or upgrade designation).

---------------------------
-> Considerations regarding TPSC purpose:

    - Functional – this includes all the capabilities that the software must exhibit in order to be fit for purpose.
    - Audit Trail – Who did what and when
    - Security – might include for example:
        # Access control, either software or physical or both
        # Backup and restore
        # Encryption
    - Archiving
    - Performance
    
---------------------------

Risk categories:
    A: There is no risk associated with using the TPSC that could impact the product or any quality process.
    B: There is a risk associated with the use of the TPSC, but it is verified by other processes.
    C: There is a risk associated with the use of the TPSC and it needs specific validation activities

-> Classify risk category taking into account intended use of TPSC
-> Record a justification
-> Review data supplied by TSPC supplier
-> Record verification activities
-> (For C risk items) Validate TPSC
    Checklist:
    - How can the purpose/use of the TPSC (i.e. its requirements) be validated?
    - What results, both positive and negative, are expected when the TPSC is subjected to the validation activities?
    - What are the range of conditions under which the TPSC should be validated?
    - Perform Validation
    - Record Evidence
-> (For B or C) Maintenance
    - create Maintenance policy - defines TPSC update control
    - TPSC updates during dev process should generally be avoided
    - TPSC's + dependencies should be archived to recreate product baselines for regression
-> Records
    - Create a TPSC activity log     

---------------------------

########################################################################################
#//////////////////////////////////////////////////////////////////////////////////////#
#//////////////////////////////////////////////////////////////////////////////////////#
########################################################################################

########################################################################################

EN 62304 - WI 49 - Software Problem Resolution

########################################################################################

---------------------------
Anomaly: Any condition that deviates from the expected behaviour. 
Expected behaviour here is derived from - Sys Requirements Spec, design docs, standards, expert perception or experience.
---------------------------
Bug: Any observed unexpected software behaviour ?(!) (very misleading definition)

---------------------------
RCA: Root Cause Analysis

---------------------------
External anomaly: (external to development?) software faults in production or third party tools

---------------------------
Internal anomaly: software faults identified in the current development

---------------------------
Change Control Board (CCB): body which reviews and approves changes to implement (SW product owners?)

---------------------------

-> 2x types of software problems:
    - Internal anomaly
    - External anomaly

-> Classification procedure: Verify that an issue is internal by reproducing it on baseline external software.

-> If external: 
    - Perform External Anomaly impact assessment (within 48h of identifying)
        If no risk : keep in work management tool backlog
        If risk associated: Follow 'SOP45 - Issue Resolution Handling'
            Output either 'Issue resolution (FM118) or CAPA (FM19)
               
-> CCB should review and prioritise bug related backlog items


########################################################################################
#//////////////////////////////////////////////////////////////////////////////////////#
#//////////////////////////////////////////////////////////////////////////////////////#
########################################################################################

########################################################################################

EN 62304 - WI 50 - Iterative Software Development Process

########################################################################################

---------------------------
Acceptance Criteria: These are the criteria that the development of a feature must fulfil before it is classed as
complete. These criteria are used during Design Verification.

---------------------------
Backlog: Set of work to be done. A backlog is usually a list of user/customer-meaningful
functionality or features that is ordered in terms of product value and encompasses the
breadth of the system or product to be built. Backlog items are typically in user story form.

---------------------------
‘Done’: is a state that a story enters when there is no longer any outstanding work related
to delivering the scope of the work. This includes all development, administration and
verification activities including acceptance 

---------------------------
Ready: A ‘ready’ story is a detailed user story with a narrative description and acceptance criteria.
It has the relevant constraints attached to it, story-specific operational qualities such as
performance constraints and a rough user interface design sketch if required

---------------------------
Retrospective: A meeting held by a project team at the end of a project, sprint or process to discuss what
was successful about the activities covered by that retrospective, what could be improved,
and how to incorporate the successes and improvements in future processes/sprints/projects

---------------------------
Sys Requirements Spec: The system requirements are developed and managed by the project team in accordance
with SOP18 and QP23 and documented in the Requirements Specification. The SwRS implements a subset of these requirements. Product verification is conducted against these requirements.

---------------------------
SwRS : Description of the software behaviour required. This is in the form of both functional and non-functional requirements for the software. Design Validation is conducted against these requirements.

---------------------------
Support task: This is a task that is required to support development but is not due to any specific user story or defect. (e.g. toolchain related work)

---------------------------
User Story: Describes through the use of a scenario how the software will be used. Derived from the requirements defined in the SW requirement specification. 

---------------------------
V&V: 
    Verification - the component does what its requirements define
    Validation - component does what the User needed it to do
    
---------------------------
Work Items: Collection of user stories / defects / support tasks

---------------------------

-> 3x layers of granularity
    - Releases
    - Sprints
    - User-stories
    
-> A 'story' should include the following information:
    - written description of the scenario
    - additional rationale on why it is required
    - Acceptance Criteria details to determine it is correct and complete

-> Checklist for a 'story' to be 'ready':
    - Performed Hazard Analysis
    - Assessed Regulatory Impact
    - (If a bug) Included test case / steps to reproduce

-> Checklist for a 'story' to be 'done':
    - Coding tasks are completed
    - Coding standards have been applied
    - Refactoring has been applied
    - Unit Tests are passing
    - Unit Tests exercise the code delivered
    - Software system tests are passing
    - Code has been peer-reviewed (or developed by a pair from the team)
    - Required new documentation has been created and reviewed
    - Existing documentation has been reviewed and updated (includes test documentation)
    - Any outstanding tasks are raised as bugs/tasks
    - QA activities have been completed

-> Records output:
    - SwRS
    - SW arch / detailed design
    - Software test protocol
    - Software test results
    - Traceability matrix

########################################################################################
#//////////////////////////////////////////////////////////////////////////////////////#
#//////////////////////////////////////////////////////////////////////////////////////#
########################################################################################

########################################################################################

EN 62304 - WI52 - Software Verification and Validation

########################################################################################

---------------------------
Black Box Testing: functional or non-functional test, without reference to internal structure of a component or system - aka Structural testing (agains 'Detailed Design'/'Sw Arch' Spec)

---------------------------
White Box Testing: exercises the internal structure of a software component - aka Specification-based Testing (against SwRS)

---------------------------
Exploratory Testing: Test scenarios based on the tester’s experience, knowledge and intuition.

---------------------------
Software Unit - A software item that is not subdivided into other items for configuration management or testing purposes

---------------------------
Software Item - A generic element of the software. Can be used to mean a single software unit / group of software units/ whole software
sys
---------------------------
SDP - Software Development Plan, specifies software dev activities plan. Adjusts processes to the scope, magnitude, and software safety classifications

---------------------------

-> Product Validation 
    - Should be performed under actual or simulated conditions of device use
    - If device has a User-Interface: apply EN 62366 (Usability)
    - Not all validation may be possible/practical to do earlier in dev

-> Product Verification
    - Based on Sys Req spec
    
-> Desing Validation
    - Based on SwRS
    - proves software meets Sys RS and traceability between Sys RS and SwRS
    - Output review goes to Design History File

-> Design Verification
    - Based on 'Detailed Design' / 'Sw Arch'
    - Proves the software design outputs meets the software design input requirements
    - activities:
        > tests (e.g., bench tests, lab analysis)
            specify representative conditions, including boundary conditions, and robustness tests
        > comparisons with proven designs
        > analyses
        > inspections
        > document reviews (e.g. plans, specifications, reports)

-> V&V planning checklist:
    - which development items require V&V
    - the required V&V activity needed for each life cycle task
    - milestones at which the development items are V&V’d
    - the acceptance criteria needed for the V&V of the development items
    - how the traceability will be recorded

-> V&V considerations for 'Detailed Design' / 'SW Arch' documentation:
    - Should implement SwRS including risk control requirements
    - Defines interfaces between software items and between software items and hardware (if/when appropriate)
    - Defines the correct use of SOUP/COTS items (supported by third party V&V activities - SOP 19)
    - Review for self-consistency, sufficient detail, and unequivocal info
    
-> SOUP items V&V checklist: 
    - defined user requirements;
    - validation protocol used;
    - acceptance criteria;
    - test cases and results; and
    - a validation summary
    
-> V&V levels and methods are project and sub-system specific 

##############################################################

-> V&V phase: Product Validation

    ---------------------------
    Activity : Review of customer requirements
    Output   : 
        - User Requirements Document Control Form (DCF)
        - Software Product Change Impact Assessment form (FM71)
        - Milestone 1 review minutes

    ---------------------------
    Activity : Confirm all user requirements are captured 
    Output   : Traceability matrix

    ---------------------------
    Activity : Confirm completed product complies with user requirements.
    Output   : 
        - Product Validation Report DCF
        - Workflow Test Report DCF
        - Accuracy Test Report DCF
        - Usability Study Report DCF
        - Traceability matrix
        - Milestone 4 minutes

    ---------------------------

##############################################################

-> V&V phase: Product Verification

    ---------------------------
    Activity : Review System Requirements, ensuring all user requirements have been addressed
    Output   : 
        - System Requirements DCF
        - Traceability matrix
        - Milestone 2 review minutes

    ---------------------------
    Activity : Ensure all system requirements have been captured 
    Output   : Traceability matrix

    ---------------------------
    Activity : Detailed product verification activities.
    Output   : 
        - Product Verification Report DCF
        - Workflow Test Report DCF
        - Accuracy Test Report DCF
        - System Test Report DCF
        - Traceability matrix
        - Milestone 4 review minutes

    ---------------------------
   
##############################################################

-> V&V phase: Design Validation

    ---------------------------
    Activity : Review Software Requirements ensuring all System Requirements have been addressed
    Output   : 
        - Software Requirement Specification DCF
        - Milestone 3 review minutes
        - Traceability matrix

    ---------------------------
    Activity : Ensure all Software requirements have been captured 
    Output   : Traceability matrix

    ---------------------------
    Activity : Review software system test specification
    Output   : 
        - System Test Specification DCF
        - Test Readiness Review Minutes

    ---------------------------
    Activity : Confirm software complies with SwRS
    Output   : 
        - System Test Report DCF
        - Traceability matrix
        - Milestone 3 minutes

    ---------------------------
    
##############################################################

-> V&V phase: Design Verification

    ---------------------------
    Activity : Review SW Arch
    Output   : Architecture Document DCF

    ---------------------------
    Activity : Review 'Detailed Design'
    Output   : Detailed Design Documents DCF

    ---------------------------
    Activity : Code Review
    Output   : 
        - Software Code Review Document DCF
        - Coding Standard (Automated tools / Static analysis/ Dynamic analysis)

    ---------------------------
    Activity : Confirm software complies with detailed design
    Output   : Unit Test Report DCF

    ---------------------------
    
##############################################################
    
-> V&V instruments for Review:
    - Pair programming (!)
    - Code Review
    - Software Inspection (large scale code review)
    - Static code analysis
    - Dynamic code analysis
    - 'SW Arch' review
    - 'Detailed Design' review

->  V&V instruments for Testing (ordered by granularity):
    - Unit test
    - Integration Test
    - Sys test
    - Regression test
    - Session based test
    - Workflow test (usability biased)
    - Ad-hoc test (Exploratory)
    - Accuracy investigation (biased for Algorithm and tolerance testing
    
    
-> Review/Testing instruments V&V checklist:
    - Event sequence
    - Data and Control flow
    - Fault Handling (Error def, isolation, recovery)
    - Initialisation of variables
    - Self-Diagnostics
    - Memory Management
    - Memory overflow
    - Boundary conditions

-> V&V Defect recording - apply WI 49 - SW Problem Resolution
    
-> V&V Records output:
    - Product V&V plan, procedure and results documents
    - Design V&V plan, procedure and results documents
    - Third party software V&V documents
    - Software development artefact document control forms (FM09)
    - Design review meeting minutes
    - Traceability matrix
    
########################################################################################
#//////////////////////////////////////////////////////////////////////////////////////#
#//////////////////////////////////////////////////////////////////////////////////////#
########################################################################################
    
    
    
    
    
