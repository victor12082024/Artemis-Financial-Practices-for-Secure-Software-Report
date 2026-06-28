# Artemis-Financial-Practices-for-Secure-Software-Report

Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?

Artemis Financial was the client. The company needed its web application improved because it handles sensitive financial information and needed stronger protection during communication and data transfer. The issue I addressed was making the application more secure by adding a SHA-256 checksum at the /hash endpoint and converting the application from HTTP to HTTPS on port 8443.

What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?

I did well by matching the security fixes to the client’s actual needs. Instead of just changing the code, I added SHA-256 checksum verification to check data integrity and configured HTTPS so communication between the browser and server was encrypted. Secure coding is important because Artemis Financial handles financial data, and weak security could expose client information, create legal problems, cause financial loss, and hurt customer trust.

Which part of the vulnerability assessment was challenging or helpful to you?

The most helpful part was running the OWASP Dependency-Check report after refactoring the application. It showed that even when my own SHA-256 and HTTPS code worked correctly, the project could still have risk from older third-party dependencies. This helped me understand that secure software depends on both the code I write and the outside libraries the project uses.

How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?

I increased security by generating a certificate, configuring the application to run through HTTPS on port 8443, adding SHA-256 checksum verification in the Java code, testing the /hash endpoint in the browser, manually reviewing the code, and running OWASP Dependency-Check. In the future, I would use OWASP Dependency-Check, CVE and CVSS scores, Maven test results, code review, and secure coding standards to decide whether to update dependencies, replace libraries, change configuration settings, or add stronger security controls.

How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?

I checked functionality by running the Spring Boot application and confirming it started without errors. I then opened https://localhost:8443/hash in the browser and verified that the page displayed my data string, the SHA-256 algorithm, and the generated checksum. After refactoring, I checked for security issues by manually reviewing the Java code and configuration files, then running OWASP Dependency-Check to confirm the scan completed and to see whether any new vulnerability concerns appeared after my changes.

What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?

The main tools and practices I used were Java’s MessageDigest class for SHA-256 hashing, Spring Boot for the web application, application.properties for the HTTPS configuration, keytool for certificate generation, Maven for running the project, OWASP Dependency-Check for dependency scanning, and manual code review. These will help in future work because they gave me practice with adding security features, configuring HTTPS, testing endpoints, and checking third-party dependencies.

Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?

From this assignment, I could show future employers my completed Artemis Financial Practices for Secure Software Report, the refactored Java code for the /hash endpoint, the SHA-256 checksum output, the HTTPS configuration on port 8443, the certificate setup, and the OWASP Dependency-Check report. These examples show that I can apply secure coding practices, test the application after making changes, use security tools, and explain why each security improvement matters.
