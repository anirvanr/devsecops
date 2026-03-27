
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

**How do you implement security in a CI/CD pipeline?**

Security is implemented by:

Using SAST and SCA scans during build

Using secrets vaults, not storing secrets in code

Enforcing branch protection, MFA, and signed commits

Scanning IaC templates (Terraform, Kubernetes, CloudFormation)

Scanning container images before pushing

Enforcing policy gates (fail build on high vulnerabilities)

Running DAST in staging

Implementing runtime monitoring and artifact signing

**What tools can be used for CI/CD security?**


SAST: SonarQube

SCA: Snyk

Secrets Scanning: GitLeaks

Container Scanning: Trivy

IaC Scanning: Checkov, Terrascan

DAST: OWASP ZAP, Burp Suite

Secrets Vault: HashiCorp Vault, AWS Secrets Manager

**How do you secure container builds in CI/CD?**

Use minimal base images

Scan images for vulnerabilities before pushing

Disallow running containers as root

Sign images before deployment

Use policy engines (Kyverno) to enforce rules

**What is "shift-left security"?**

Shift-left security means detecting and fixing issues earlier in the development cycle rather than waiting until deployment.

**How do you ensure secure deployments?**

Use signed and verified artifacts

Implement RBAC for deployment environments

Use infrastructure automation (IaC) with scanning

Disable manual deployments

Encrypt data in transit and at rest

A **DDoS (Distributed Denial of Service)** attack is when someone tries to knock a website offline by flooding it with so much traffic that it can't handle real users anymore.

Think of it like:

A store where thousands of fake customers rush in at once,
making it impossible for real customers to get inside.

A **SQL injection** is when a hacker tricks a website into running harmful commands on its database by sneaking malicious code into a login form or search box.

Let's say a login form has this logic:
```
username: admin
password: password123
```

The website runs a command like:
```
SELECT * FROM users WHERE username = 'admin' AND password = 'password123'
```

But if a hacker enters:
```
username: admin' OR '1'='1
password: anything
```

The command becomes:
```
SELECT * FROM users WHERE username = 'admin' OR '1'='1' AND password = 'anything'
```

Since `'1'='1'` is always true, the database returns every user account! The hacker bypasses the login.
