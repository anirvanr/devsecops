
📌 Overview

Software Development Life Cycle (**SDLC**)
The traditional process used to plan, build, test, and deliver software.

Secure Software Development Life Cycle (**SSDLC**)
An enhanced SDLC approach where security is integrated into every phase, not just at the end.

🔄 Phases of SDLC / SSDLC

1️⃣ Planning : Defines the overall foundation of the project.

**Key Activities:**

- Define project scope & objectives
- Estimate resources
- Set timeline & budget
- Identify risks and constraints

2️⃣ Requirements: Document what the system should do and how it should behave.

**Key Activities:**

- Gather functional requirements
- Gather non-functional requirements
- Create use cases & user stories
- Define acceptance criteria

3️⃣ Design: Create the blueprint of the system.

**Key Activities:**

- Create system architecture
- Select technology stack
- Design deployment architecture
- Identify integrations & data flows

4️⃣ Development: Actual coding of the application.

**Key Activities:**

- Write code following standards & best practices
- Implement unit tests
- Use secure coding practices

🔐 Security in Development (Shift-Left Security Tools)

Static Application Security Testing (SAST): Analyzes source code
Examples: `SonarQube`

Software Composition Analysis (SCA): Scans open-source and third-party libraries
Examples: `Snyk, JFrog Xray`

Container Security: Scans Docker container images
Examples: `Trivy, Anchore, Clair`

Infrastructure as Code (IaC) Security: Scans Terraform, Kubernetes, CloudFormation, etc.
Examples: `Checkov`

Secret Scanning: Detects hardcoded secrets
Example: `Gitleaks`

5️⃣ Testing: Confirms the system works as expected and meets requirements.

**Key Activities:**

- Create test plans and test cases
- Perform integration testing
- Execute system testing
- Conduct user acceptance testing (UAT)
- Perform performance and load testing
- Regression testing


🔐 Security Testing Methods

Dynamic Application Security Testing (DAST): Tests a running application from the outside
Examples: `OWASP ZAP, Burp Suite, Acunetix`

Interactive Application Security Testing (IAST): Tests from inside the application using sensors/agents

6️⃣ Deployment: Release the application to production.

**Key Activities:**

- Deploy using CI/CD
- Configure infrastructure
- Perform final validation
- Release to end users

7️⃣ Maintenance: Ongoing improvements after release.

**Key Activities:**

- Patch bugs
- Monitor system performance and availability
- Optimize performance
- Maintain documentation
- Release updates
