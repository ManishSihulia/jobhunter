# Training Plan for MS Dynamics NAV / Business Central Developer Role

Based on the job requirements and current skill gaps, here are the priority areas for training and skill development to maximize success in this ERP developer position.

## 🔴 HIGH PRIORITY - Critical for Role

### 1. Microsoft Dynamics NAV & Business Central Fundamentals
**Relevance:** REQUIRED - Core platform knowledge for the role.

#### Overview
Microsoft Dynamics NAV (now rebranded as Dynamics 365 Business Central) is a comprehensive ERP solution for small to medium-sized businesses. Understanding its architecture, development environment, and customization capabilities is essential.

#### Training Topics
- [ ] **NAV/BC Architecture:** Multi-tier architecture, database layer, application server, client layer
- [ ] **Navigation:** Tables, Pages, Reports, Codeunits, XMLports, Queries
- [ ] **Development Environment:** Visual Studio Code with AL Language extension vs. C/SIDE (legacy)
- [ ] **Data Model:** Understanding standard NAV tables, primary keys, relationships, table extensions
- [ ] **Page Design:** Card pages, List pages, Document pages, page extensions, actions, triggers
- [ ] **Business Logic:** Codeunits, procedures, functions, event subscribers
- [ ] **Licensing & Versioning:** Understanding NAV versions (2013, 2015, 2016, 2017, 2018) vs. Business Central

#### Resources
- Microsoft Learn: Introduction to Dynamics 365 Business Central
- Microsoft Docs: Dynamics NAV Developer Documentation
- Hands-on: Install BC sandbox environment, explore standard modules
- Book: "Programming Microsoft Dynamics NAV" by David Studebaker

### 2. C/AL Programming Language (NAV Legacy)
**Relevance:** REQUIRED - Many NAV implementations still use C/AL for customizations.

#### Overview
C/AL (Client/Server Application Language) is the proprietary programming language for Microsoft Dynamics NAV. While legacy, it's still widely used in existing NAV installations.

#### Training Topics
- [ ] **Syntax Fundamentals:** Variables, data types, operators, control structures
- [ ] **Triggers:** OnInsert, OnModify, OnDelete, OnValidate, OnAfterGetRecord
- [ ] **Functions:** Built-in functions (FIND, SETRANGE, CALCFIELDS, MESSAGE), custom functions
- [ ] **Record Operations:** INSERT, MODIFY, DELETE, GET, SETFILTER, SETRANGE
- [ ] **Forms & Reports:** Classic forms, request pages, sections, data items
- [ ] **Error Handling:** ERROR function, CONFIRM dialogs, validation
- [ ] **C/AL vs C#:** Understanding differences and similarities for faster learning

#### Resources
- Microsoft Dynamics NAV C/AL Programming Guide
- C/AL Symbol Reference documentation
- Practice: Modify standard NAV objects, create custom reports
- Online tutorials: C/AL basics for C# developers

### 3. AL Programming Language (Business Central Modern)
**Relevance:** REQUIRED - Modern development language for Business Central cloud and on-premises.

#### Overview
AL is the modern successor to C/AL, designed for extension-based development in Business Central. It uses Visual Studio Code and supports modern development practices like Git version control.

#### Training Topics
- [ ] **AL Basics:** Syntax, data types, variables, procedures, expressions
- [ ] **Extension Development:** Creating table extensions, page extensions, codeunit extensions
- [ ] **Events & Subscribers:** Publishing and subscribing to business events, integration events
- [ ] **Enums & Interfaces:** Modern OOP concepts in AL
- [ ] **Queries:** Creating and consuming query objects for data retrieval
- [ ] **Testing:** AL Test framework, test codeunits, test pages
- [ ] **Deployment:** Extension packages (.app files), AppSource, per-tenant extensions
- [ ] **AL vs C#:** Leveraging C# knowledge for faster AL learning

#### Resources
- Microsoft Learn: AL Language Development
- AL Language Extension for VS Code
- GitHub: AL code samples and templates
- Practice: Convert C/AL customizations to AL extensions
- Book: "Programming Business Central" (modern AL development)

### 4. NAV/BC Standard Modules & Business Processes
**Relevance:** REQUIRED - Understanding standard functionality before customization.

#### Overview
Deep knowledge of NAV/BC standard modules helps in customization, integration, and troubleshooting.

#### Training Topics
- [ ] **Financial Management:** G/L, Bank Management, Receivables, Payables, Fixed Assets
- [ ] **Sales & Marketing:** Customers, Sales Quotes/Orders/Invoices, CRM integration
- [ ] **Purchase:** Vendors, Purchase Orders/Invoices, Requisitions
- [ ] **Inventory Management:** Items, Stockkeeping, Item Tracking, Warehouse Management
- [ ] **Manufacturing:** BOMs, Production Orders, Capacity Planning, Shop Floor Control
- [ ] **Jobs & Projects:** Job costing, resource planning, time sheets
- [ ] **Service Management:** Service Orders, Service Contracts, Resource allocation
- [ ] **HR Management (if applicable):** Employee records, absence tracking

#### Resources
- Dynamics NAV/BC User Documentation
- Application functional training courses
- Demo database exploration
- Business process flow diagrams
- Hands-on: Complete standard transactions in each module

## 🟡 MEDIUM PRIORITY - Strengthen Existing Skills

### 5. NAV/BC Development Tools & Debugging
**Relevance:** Essential for efficient development and troubleshooting.

#### Training Topics
- [ ] **Development Environments:** C/SIDE for legacy NAV, VS Code with AL for modern BC
- [ ] **Debugging:** Breakpoints, watch variables, call stack analysis, debugger in C/SIDE and AL
- [ ] **Object Designer:** Understanding object numbers, creating/modifying objects
- [ ] **Version Control:** Git integration with AL development, branching strategies
- [ ] **Testing Tools:** NAV Test Tool, AL Test Runner, automated testing
- [ ] **Performance Profiling:** SQL Server Profiler, NAV/BC performance monitoring
- [ ] **Data Upgrade:** Version upgrade tools, data migration strategies

#### Resources
- Microsoft Docs: Debugging in AL and C/SIDE
- NAV Development Tools documentation
- Hands-on: Debug custom code, analyze performance bottlenecks
- Practice: Set up proper development environment

### 6. NAV/BC Integration & Web Services
**Relevance:** Critical for connecting NAV/BC with external systems.

#### Training Topics
- [ ] **Web Services:** SOAP vs OData, exposing pages/codeunits as web services
- [ ] **REST API:** Business Central API v2.0, authentication, consuming external APIs
- [ ] **XMLports:** Data import/export, XML structure, field mapping
- [ ] **Dataverse Integration:** Power Platform connection, virtual tables
- [ ] **File Handling:** Import/export CSV, XML, JSON files
- [ ] **API Development:** Creating custom APIs in Business Central
- [ ] **Authentication:** OAuth 2.0, service-to-service authentication

#### Resources
- Microsoft Docs: Business Central Web Services
- API documentation and examples
- Hands-on: Create and consume web services
- Project: Build integration with external system

### 7. SQL Server Optimization for NAV/BC
**Relevance:** NAV/BC relies heavily on SQL Server performance.

#### Training Topics
- [ ] **NAV Table Structure:** Understanding SIFT tables, FlowFields, FlowFilters
- [ ] **Index Management:** SIFT indexes, SQL indexes, index optimization
- [ ] **Query Optimization:** Analyzing NAV-generated SQL, optimizing AL code for performance
- [ ] **Database Maintenance:** Backup strategies, index rebuilding, statistics updates
- [ ] **Locking & Deadlocks:** Understanding NAV locking mechanisms, resolving deadlocks
- [ ] **SQL Profiling:** Identifying slow queries generated by NAV/BC
- [ ] **Database Tuning:** Memory allocation, tempdb configuration for NAV

#### Resources
- "Optimizing Dynamics NAV Database" guides
- SQL Server performance tuning for NAV/BC
- Hands-on: Analyze and optimize NAV database performance
- SQL Server Profiler with NAV workload

## 🟢 LOW PRIORITY - Nice to Have

### 8. NAV/BC Reporting & BI
**Relevance:** Beneficial for comprehensive ERP solutions.

#### Training Topics
- [ ] **NAV Report Design:** Classic reports vs RDLC reports, dataset design
- [ ] **Request Pages:** Parameters, filters, options
- [ ] **Report Extensions:** Extending standard reports in AL
- [ ] **Power BI Integration:** Embedding Power BI in Business Central pages
- [ ] **Excel Reports:** Using Excel layouts for reports
- [ ] **Word Layouts:** Creating document templates with Word

#### Resources
- NAV Reporting documentation
- RDLC report designer tutorials
- Power BI integration guides
- Sample report customizations

### 9. NAV/BC Certification Preparation
**Relevance:** Professional credential for career advancement.

#### Training Topics
- [ ] **MB-800:** Microsoft Dynamics 365 Business Central Functional Consultant
- [ ] **MB-820:** Microsoft Dynamics 365 Business Central Developer (coming soon)
- [ ] Exam preparation materials and practice tests

#### Resources
- Microsoft Learn certification paths
- Official practice exams
- Study groups and forums

## 📚 Recommended Learning Path

### Week 1-2: NAV/BC Fundamentals & Architecture
- Study NAV/BC architecture and navigation
- Install sandbox environment
- Explore standard modules and business processes
- Understand table structures and relationships

### Week 3-4: C/AL Programming (Legacy NAV)
- Learn C/AL syntax and fundamentals
- Practice with simple customizations
- Study triggers and built-in functions
- Modify standard objects in test environment

### Week 5-6: AL Programming (Modern BC)
- Set up VS Code with AL extension
- Learn AL syntax (leverage C# knowledge)
- Create simple table and page extensions
- Understand event-driven architecture

### Week 7-8: Hands-On Development Project
- Build complete NAV/BC customization:
  - Custom table for business entity
  - Card and List pages with proper UI
  - Codeunit with business logic
  - Report with RDLC layout
  - Web service exposure
  - Integration with external API
  - Testing and debugging
  - Documentation

### Week 9-10: Integration & Advanced Topics
- Practice XMLport development
- Create and consume web services
- Study OData APIs
- Work on SQL Server optimization for NAV

### Week 11-12: Real-World Scenarios
- Study common customization patterns
- Review production NAV/BC solutions
- Practice troubleshooting techniques
- Build portfolio project

## 🎯 Success Metrics

- [ ] Successfully install and configure NAV/BC development environment
- [ ] Complete 5+ C/AL programming exercises
- [ ] Build 3+ AL extensions (table, page, codeunit)
- [ ] Create end-to-end custom module in NAV/BC
- [ ] Expose and consume web services
- [ ] Optimize NAV database with SQL Server techniques
- [ ] Debug and resolve complex issues in NAV/BC
- [ ] Document complete customization with best practices
- [ ] Complete Microsoft Learn NAV/BC learning paths
- [ ] Join NAV/BC community forums and contribute

## 💼 Immediate Actions (First Week on Job)

1. **Environment Setup:** Configure development environment, access to NAV/BC instances
2. **Standard Processes:** Understand company's coding standards and deployment procedures
3. **Shadow Senior Developers:** Learn company-specific customizations and patterns
4. **Documentation Review:** Study existing customization documentation
5. **Small Tasks:** Start with bug fixes and minor enhancements to get familiar
6. **Ask Questions:** Build relationships with team members and clarify doubts early

## 📖 Essential Resources

- **Official Documentation:** Microsoft Docs for Dynamics NAV and Business Central
- **Community:** Dynamics Community forums, NAVUG, BC User Group
- **Blogs:** Follow NAV/BC MVPs and experienced developers
- **GitHub:** Explore open-source AL projects and code samples
- **Books:** "Programming Microsoft Dynamics NAV", "Mastering Business Central"
- **YouTube:** NAV/BC development tutorials and conference sessions