# CS305 Software Security - Module 8 Journal

## Client Summary
> Artemis Financial is a consulting firm that develops individualized financial plans, including savings management, retirement strategies, investments, and insurance products. The organization wanted to modernize its RESTful web application to better protect sensitive data from external threats. My responsibility was to evaluate the application for vulnerabilities and implement secure coding practices that would strengthen its overall security posture. 
> 
## What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?
> When I identified vulnerabilities in the application, I think I did well in slowing down and analyzing them instead of immediately attempting to suppress or patch everything. I reviewed CVE documentation, evaluated severity levels, and documented my reasoning before implementing mitigation strategies. This process helped me understand not just what the vulnerability was, but why it mattered in the context of a financial institution.
>
> This assignment reinforced for me that secure coding is not optional but essential, especially in financial systems. Without proper input validation, encryption, and dependency management, software can quickly become a direct attack surface. Development with a security focus adds long-term value to a company by protecting the integrity of the company's relationship with its clients. By preventing costly security breaches and reducing operational and legal risk, it strengthens a company's credibility and overall stability. 

## Which part of the vulnerability assessment was challenging or helpful to you?
> The most challenging part of this project was interpreting the OWASP Dependency-Check report. At first glance, the number of reported vulnerabilities felt overwhelming. But learning to distinguish between legitimate risks and false positives required me to carefully analyze versioning, exploit context, and documentation. This ultimately became one of the most useful parts of the assignment because it allowed me to critically assess each vulnerability rather than rely entirely on automated tools. 

## How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?
> After my initial assessment of the code base, I performed a baseline dependency-check to determine the total number of vulnerabilities. Then I started by developing a single endpoint with strict input validation and incorporated SHA-256 hashing to verify data integrity using a checksum. Once this endpoint had the desired functionality and restrictions, I implemented HTTPS with TLS to establish a secure connection using a self-signed certificate and a configured keystore.
>
> In the future, I would continue using tools such as OWASP Dependency-Check, but I would also explore additional static and dynamic analysis tools. I would apply structured guidance such as NIST frameworks to better prioritize vulnerabilities based on real-world applicability. This assignment showed me that an incremental layered security approach  and risk-based thinking are far more effective than reactive patching. 

## How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?
> After refactoring the code, I verified that the HTTPS endpoint functioned correctly and that secure communication was properly established in the browser. I confirmed that the SHA-256 hashing endpoint produced consistent results, ensuring that functionality was not broken by security enhancements.
>
> I then generated an updated dependency-check report to confirm that my changes did not introduce new high-severity vulnerabilities. This iterative testing process helped me understand that secure development requires constant validation. Security improvements must support functionality, not disrupt it. 

## What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?
> This project strengthened my hands-on experience with Maven dependency management, OWASP Dependency-Check, TLS configuration, and Java's MessageDigest API. I practiced input validation, encryption in transit, and dependency review. More importantly, I developed a more structured approach to analyzing security risks instead of relying solely on automated output. These skills will directly carry forward into future development and security-focused projects. 

## Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?
> From this assignment, I would show my vulnerability assessment process, my reasoning behind mitigation decisions, and my implementation of secure communication within a Java-based web application. This project demonstrates that I can integrate security practices into development rather than treating them as an afterthought. It also reflects my ability to learn new tools, interpret security documentation, and apply structured thinking to reduce risk while maintaining functionality. 
