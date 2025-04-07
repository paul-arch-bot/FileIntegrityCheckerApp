
PROJECT TITLE: FILE INTEGRITY CHECKER ONSONGO PAUL

This project is submitted to the department of computer science and IT of Kabarak University in partial fulfilment for the award of the Bsc Computer Security and Forensics degree

March 2025
 
DECLARATION
I hereby declare that this is my original work and that it has not been presented to any other learning institution for the award of academic qualification.
NAME: ONSONGO PAUL 
SIGNARURE:
DATE:3/4/2025

SUPERVISORS APPROVAL
This project has been submitted to the Kabarak University with my approval as the university supervisor.
NAME:JOSHUA MUTAI
SIGNATURE:
DATE:3/4/2025
 
RECOMMENDATION
This work was done under my supervision and is being submitted with my approval as the university supervisor.

Signature…………………………………….                  Date…………………………………….
Eng JOSHUA MUTAI
DEPARTMENT OF COMPUTER SCIENCE AND INFORMATION TECHNOLOGY KABARAK UNIVERSITY.


 
DEDICATION
We hereby dedicate our work to our ever supportive parents,siblings and lecturer for their constant guidance and support throughout the entire process. We also want to thank the Almighty God for giving us strength and the commitment to carry out our tasks responsibly.  
ACKNOWLEDGEMENT
We would like to express our sincere gratitude to each other as group members for diligently carrying out our tasks without failure, demonstrating exceptional teamwork and dedication. We also extend our heartfelt thanks to the entire School of Science, Engineering, and Technology for their encouragement in fostering our research and innovation, which played a pivotal role in our success. Our deepest appreciation goes to our supervisor, Mr. Joshua Mutai, for taking the time to guide us throughout this project, offering invaluable mentorship, and ensuring consistent follow-up on our progress. Finally, we are grateful to everyone else who supported us with their ideas and insights, helping to bring this task to fruition. Your contributions have been essential, and we truly appreciate your unwavering support.
 
ABSTRACT
This project focuses on the development of a file integrity checker designed to ensure the authenticity and integrity of files stored in computer systems. File integrity refers to the condition in which files remain unaltered and consistent over time. The integrity checker utilizes cryptographic hash functions to generate unique checksums for each file, allowing for the detection of any unauthorized changes, corruption, or tampering. By periodically verifying the integrity of critical files, the system provides an essential layer of security for both personal and organizational data. The project aims to enhance data protection, improve system reliability, and reduce the risk of security breaches. It also includes user-friendly interfaces for ease of use, alongside detailed logs that provide insights into file status and any detected anomalies. Through this tool, users can quickly identify and address potential issues, ensuring the preservation of data accuracy and security. 
        
         
Table of Contents
DECLARATION	2
RECOMMENDATION	3
DEDICATION	4
ACKNOWLEDGEMENT	5
ABSTRACT	6
Table of Figures	8
CHAPTER ONE:	9
1.1Introduction	9
1.2 Background of the study	9
1.3Statement of the problem	10
1.4 Purpose of the study	11
1.5 Research Objectives	12
1.6 Research Questions	12
1.7 Significance of the study	12
1.8 Expected outcomes of the study	13
1.9 Scope of the study	15
1.10 Limitations of the study	16
1.11 Scalability of the study	17
CHAPTER TWO: LITERATURE REVIEW	18
2.1 Introduction	18
2.2 Review of File Integrity and Security	18
2.3 Review of Cryptographic Hash Functions in File Integrity Verification	18
2.4 Review of File Integrity Monitoring (FIM) Techniques	19
2.5 Review of Challenges in File Integrity Monitoring	19
2.6 design Framework	20
2.7 Research Gap and Emerging Trends	21
2.8 Conclusion	21
CHAPTER THREE: RESEARCH METHODOLOGY	22
3.1 Introduction	22
3.2 Research Methodology	22
3.3 Development Methodology	22
3.4 Programming Methodology	22
3.5 System Analysis and Design	23
3.6 Context Diagram	23
3.7 Research Ethics	25
CHAPTER FOUR: SYSTEM DEVELOPMENT AND DEPLOYMENT	25
4.0 System Development and Deployment	25
4.1 System Description and Deployment	25
4.3Front-End Development	26
4.4 User Interface Design	26
4.5 Back-End Development	27
4.6 Database Design Models	28
4.7 System Testing	28
4.8 Conclusion	28
4.9 Recommendations	28
CHAPTER FIVE: CONCLUSION AND RECOMMENDATIONS	29
5.1 Introduction	29
5.2 Summary of Findings	29
5.3 Conclusion	29
5.4 Recommendations	29
5.5 Future Research Directions	29
References	30

	Table of Figures
Figure 1	20
Figure 2	24
Figure 3 login page of the file integrity system	26
Figure 4 : dashboard displaying file paths of monitored files	26
Figure 5: alerts on file changes	27
Figure 6: file status displayed	27




CHAPTER ONE:
1.1Introduction
This chapter provides an overview of the project, detailing its objectives, significance, and the motivation behind developing a cryptographic hashing-based File Integrity Checker. It highlights the key challenges associated with unauthorized file modifications, data corruption, and security threats, particularly in the finance sector. By leveraging advanced cryptographic techniques, the project establishes a proactive and intelligent monitoring framework to detect unauthorized changes, trigger real-time alerts, and ensure data security. Through continuous verification, this solution strengthens cybersecurity measures and safeguards critical information against tampering.

1.2 Background of the study
As technology advances, the volume of digital data being created, stored, and shared continues to grow exponentially. With this rise in data usage, the need to ensure its security and integrity becomes increasingly critical. File integrity, specifically, refers to the accuracy, consistency, and trustworthiness of data stored within files. Maintaining the integrity of files is essential for preventing data corruption, unauthorized modifications, or tampering, all of which can lead to serious security breaches, loss of data, or system malfunctions.
File integrity can be compromised in numerous ways, including accidental file corruption, software bugs, hardware failures, malicious attacks like ransomware or viruses, and human errors. Such alterations may go unnoticed unless there is an effective way to detect and verify the integrity of files on a regular basis. Without a reliable method to track and verify changes in files, organizations and individuals are at significant risk of data theft, loss, or manipulation.
One of the most common methods for ensuring file integrity is through the use of hashing algorithms. These algorithms generate a unique fixed-length string, or hash, that represents the content of a file. Even the slightest change in a file’s content will result in a completely different hash value. By storing the hash values of files and periodically recalculating them, any discrepancies between the stored and current hash values can indicate potential tampering or corruption. This provides an effective way of monitoring files for integrity over time.
Various file integrity checkers have been developed over the years, leveraging different hashing techniques, such as MD5, SHA-1, and SHA-256. However, the evolving nature of cyber threats and technological advancements means that file integrity tools must also continuously adapt to ensure that they remain effective and resilient against new forms of attacks.
This study aims to explore the importance of file integrity and develop a tool that helps in detecting any changes to files by using cryptographic techniques. By focusing on the design and implementation of an efficient, scalable, and secure file integrity checker, this research seeks to contribute to the ongoing efforts in safeguarding digital data from potential threats and errors.


1.3Statement of the problem
In an era where data is a cornerstone of both personal and organizational success, the security and integrity of digital information are paramount. However, the constant risk of file corruption, unauthorized modifications, or tampering threatens the reliability of files and the systems that depend on them. This problem is particularly critical for sensitive data, such as financial records, medical files, and intellectual property, where even a minor alteration can lead to severe consequences, including financial loss, reputational damage, or legal issues.
Currently, many systems lack an efficient and automated method to monitor and verify the integrity of files, making it difficult to detect unauthorized changes or file corruption in real-time. While some solutions exist, they may not provide the level of accuracy, reliability, or ease of use required by users. Furthermore, existing tools may be vulnerable to modern cyber threats, such as sophisticated malware and ransomware, which can bypass traditional integrity-checking methods.
As a result, the need for an advanced and accessible file integrity checker has become more urgent than ever. Without such a tool, users and organizations are left exposed to the risks of undetected data corruption or tampering, which can have far-reaching consequences on both data security and system performance.
This project aims to address these challenges by developing a robust file integrity checker that leverages cryptographic techniques to accurately detect file modifications and ensure the integrity of data. By providing an easy-to-use solution for real-time monitoring and detection, this tool seeks to mitigate the risks associated with file tampering and corruption, ensuring that digital data remains trustworthy and protected.

1.4 Purpose of the study
The purpose of this study is to design and develop a reliable and efficient file integrity checker that can help ensure the security and consistency of digital data. This tool aims to address the growing concerns regarding unauthorized file modifications, corruption, and tampering, which pose significant risks to the integrity of critical data stored in computer systems. By utilizing cryptographic hash functions and advanced detection methods, the study intends to create a solution that allows users to easily verify and monitor the integrity of files in real time.
The study seeks to explore and implement a system that can automatically detect any alterations to files, providing users with immediate alerts when discrepancies are identified. This will be achieved through a user-friendly interface that simplifies the process of tracking file changes, making it accessible even to non-technical users. The purpose of this tool is not only to protect data from malicious attacks but also to ensure that files remain uncorrupted and intact, reducing the risk of data loss or unauthorized access.
Additionally, the study aims to evaluate and compare the performance of different hashing algorithms in terms of their effectiveness and efficiency for file integrity checking. By doing so, the project will contribute valuable insights into the strengths and limitations of various cryptographic techniques for file integrity verification, ultimately enabling the development of a more robust and adaptable integrity checker.
Through this research, the study intends to provide an essential tool for individuals, businesses, and organizations to safeguard their digital assets and maintain the trustworthiness of their data in an increasingly vulnerable digital environment.

1.5	Research Objectives

 I. To design a file integrity checker that utilizes cryptographic hash functions to monitor and verify the integrity of files in real time.  
II. To develop a user-friendly interface that enables both technical and non-technical users to easily implement and use the file integrity checker while incorporating real-time monitoring and alerts for potential tampering or corruption.  
III. To test the effectiveness, performance, and efficiency of different hashing algorithms (such as MD5, SHA-1, and SHA-256) in detecting file modifications, assessing processing speed, resource usage, and accuracy, and providing recommendations for improving file security.
1.6 Research Questions
I.  How can a file integrity checker be designed to efficiently utilize cryptographic hash functions for real-time monitoring and verification of file integrity?
II What user interface features and system functionalities can be implemented to develop a user-friendly file integrity checker that supports both technical and non-technical users while providing real-time monitoring and alerts?
III. How can the performance, efficiency, and accuracy of different cryptographic hashing algorithms (e.g., MD5, SHA-1, SHA-256) be tested to determine the most effective approach for detecting file modifications with minimal resource consumption?
1.7 Significance of the study
This study is significant in addressing the growing need for secure and reliable methods of ensuring file integrity in a world where digital data is increasingly at risk of tampering, corruption, or loss. By developing a file integrity checker that uses cryptographic techniques, the study provides a practical solution to safeguard sensitive and critical files from unauthorized modifications or unintentional damage. With the rise of cyber threats, such as malware, ransomware, and hacking attempts, having a robust tool to detect file alterations in real-time is essential for maintaining the security and authenticity of data.
The findings of this study contribute to the field of data security by evaluating the effectiveness of various cryptographic hash functions, such as MD5, SHA-1, and SHA-256, for file integrity checking. The results will help determine which algorithms offer the best balance between security, efficiency, and performance. This knowledge can be leveraged to develop more secure and efficient integrity-checking tools for both personal and organizational use.
Furthermore, the development of a user-friendly interface in this study ensures that file integrity checking is accessible not only to IT professionals but also to everyday users with limited technical knowledge. This expands the potential user base and makes the tool more practical for a wider audience. By providing a simple yet effective way to monitor and protect files, the study helps individuals and organizations mitigate the risks of data loss, corruption, and unauthorized access.
In a broader context, this study also plays a role in raising awareness about the importance of file integrity and the need for proactive measures in the protection of digital data. The implications of this research are far-reaching, as file integrity is crucial across various sectors, including finance, healthcare, government, and education, where data accuracy and security are of utmost importance.
Ultimately, the significance of this study lies in its potential to enhance the security of digital information, reduce vulnerabilities in file storage systems, and contribute to the overall safety of the digital ecosystem.

1.8 Expected outcomes of the study
i.	Development of a Functional File Integrity Checker
The study expects to produce a fully functional file integrity checker that effectively monitors and verifies the integrity of files using cryptographic hashing techniques. This tool will allow users to detect unauthorized changes to files, providing a reliable method for ensuring data consistency and security.
ii.	Comparison of Hashing Algorithms
The study aims to compare the performance and effectiveness of different cryptographic hash functions (such as MD5, SHA-1, and SHA-256). It is expected to determine which algorithms offer the best balance of security, efficiency, and performance for file integrity checking, with SHA-256 likely emerging as the most robust for ensuring data integrity.
iii.	Real-time File Monitoring and Alerts
One of the key outcomes is the implementation of a real-time monitoring system that alerts users when a file’s integrity has been compromised. This will allow users to take immediate action if a file’s hash does not match the stored hash, thus providing an extra layer of security for critical data.
iv.	User-friendly Interface
The study expects to design a simple and intuitive interface that allows users, even those with minimal technical expertise, to easily monitor their files for integrity issues. The interface will offer straightforward functions such as setting up file monitoring, viewing alerts, and verifying file statuses, making the tool accessible to a broader audience.
v.	Assessment of Performance and Efficiency
The study will assess the efficiency and performance of the file integrity checker, focusing on processing speed, resource consumption, and scalability. It is expected that the tool will perform efficiently, even when monitoring large volumes of files, without placing a significant strain on system resources.
vi.	Enhanced Security Awareness and Practices
As a result of the study, there is an expectation of increased awareness about the importance of file integrity in the digital landscape. The tool will encourage individuals and organizations to adopt better security practices, leading to improved data protection and a reduction in the risk of data corruption or unauthorized access.
vii.	Practical Contribution to File Integrity Tools
This research is expected to contribute valuable insights into the development of more secure and efficient file integrity checkers. The study’s findings will provide a foundation for future improvements in file integrity monitoring tools, which can be adapted to meet evolving cybersecurity threats and the growing need for data protection.
viii.	Recommendations for Future Improvements
Based on the results of the study, recommendations will be made for improving file integrity checkers, particularly in terms of enhancing their resistance to emerging threats like sophisticated malware. These recommendations may also include suggestions for incorporating additional security features, such as encryption or automated backup systems, to further bolster file protection.
1.9 Scope of the study
I.	This study focuses on the design, development, and evaluation of a file integrity checker that leverages cryptographic hash functions to monitor and ensure the integrity of files stored on a computer system. The scope of this research is limited to the use of hashing algorithms such as MD5, SHA-1, and SHA-256, with the primary goal of comparing their performance in detecting file modifications, corruption, and unauthorized changes. While the study emphasizes file integrity monitoring, it does not delve into other aspects of data security such as encryption, access control, or authentication.
II.	The study's scope also encompasses the creation of a user-friendly interface that allows users, both technical and non-technical, to easily interact with the file integrity checker. The tool will be designed for use on personal computers and will target individual users, small businesses, and organizations that need to ensure the integrity of their files. It will be tested on a variety of file types, including documents, images, and system files, but will not extend to specialized file systems such as those used in cloud storage or large-scale enterprise systems.
III.	In terms of performance, the study evaluates the efficiency of the file integrity checker in terms of processing speed and resource consumption. The research will be limited to monitoring files on local systems and will not address network-based file monitoring or integration with remote servers. Additionally, while the tool aims to offer real-time alerts and notifications when file discrepancies are detected, it will not include advanced features such as automated file repair or backup restoration.
IV.	Lastly, the study will focus on a comprehensive comparison of the hashing algorithms in the context of file integrity, assessing their accuracy, computational efficiency, and resistance to collision attacks. The study will not explore advanced cryptographic techniques beyond hashing, such as digital signatures or public key infrastructure (PKI).

1.10 Limitations of the study
i.	While this study provides a comprehensive approach to developing a file integrity checker, there are several limitations to consider. First, the scope of the tool is limited to the use of cryptographic hash functions—specifically MD5, SHA-1, and SHA-256—without exploring more advanced cryptographic techniques such as digital signatures or public key infrastructure (PKI). This means the study does not cover all aspects of file security, such as encryption or secure file access control.
ii.	Secondly, the study is restricted to monitoring files stored locally on personal computers or small-scale business systems. It does not extend to monitoring files stored on cloud services, network drives, or large-scale enterprise file systems, which may involve different types of storage architectures and security concerns. Therefore, the file integrity checker may not be directly applicable to more complex, distributed systems.
iii.	Additionally, the tool developed in this study will focus on detecting unauthorized file modifications or corruption but will not have the capability to repair or restore altered files automatically. While the tool will notify users of discrepancies, it does not include functionality for automated backups or data recovery, which may be critical for some users.
iv.	Another limitation is that the study evaluates the performance of the integrity checker primarily based on file size and processing speed, without considering other factors such as the impact of the system's hardware or operating environment. This may affect the tool's scalability and efficiency in more resource-constrained or high-demand systems.
v.	Lastly, the study does not explore potential vulnerabilities in the hashing algorithms themselves, such as their susceptibility to collision attacks or their performance in real-world cyberattack scenarios. While the study compares the effectiveness of different hashing algorithms in terms of file integrity, it does not consider the broader implications of algorithm weaknesses in advanced threat scenarios.

1.11 Scalability of the study
The scalability of this study is focused on the ability of the developed file integrity checker to handle a growing number of files and larger file sizes efficiently. As digital storage grows and organizations accumulate vast amounts of data, the need for scalable solutions to monitor and maintain file integrity becomes increasingly critical. The study is designed to assess how well the file integrity checker can perform under different conditions, such as monitoring a larger volume of files or handling files of various sizes without significant performance degradation.
The scalability of the tool is evaluated in terms of both processing speed and system resource consumption. The file integrity checker is expected to function efficiently, even when tasked with monitoring multiple files simultaneously or with larger files that could potentially require more processing power. However, the study’s focus on local systems and small-scale environments limits the ability to fully test the tool’s scalability in large enterprise networks or cloud-based systems, where the volume of data and the complexity of file structures are much higher.
While the current design of the file integrity checker allows it to scale within personal and small business settings, future work may be required to optimize the tool for larger, more complex environments. This could include integration with cloud storage platforms, networked file systems, or distributed databases, where the challenges of monitoring file integrity across multiple locations and systems become more pronounced.
Overall, the scalability of the study is promising within the scope of personal and small-scale applications, but further development may be necessary to address the demands of larger, more complex systems.




CHAPTER TWO: LITERATURE REVIEW
2.1 Introduction
This chapter presents a comprehensive review of existing literature related to file integrity verification. The review focuses on cryptographic hashing techniques, file integrity monitoring (FIM) methods, and existing tools used for file integrity checking. It also highlights research gaps and emerging trends in data security. The discussion follows the structure outlined in the project guidelines, ensuring alignment with academic requirements.

2.2 Review of File Integrity and Security
File integrity is the assurance that digital files remain unaltered unless modified by authorized entities. Ensuring file integrity is critical for preventing unauthorized modifications, data corruption, and cyber threats such as malware and ransomware. Several factors contribute to file integrity threats, including:
•	Hardware Failures: Storage device malfunctions leading to unintended data corruption.
•	Malware and Ransomware: Malicious software encrypting or modifying files.
•	Insider Threats: Unauthorized modifications by employees or cybercriminals.
•	Transmission Errors: Data corruption during file transfers over networks.
Organizations deploy File Integrity Monitoring (FIM) solutions to detect and mitigate these risks, using cryptographic techniques for secure verification.
2.3 Review of Cryptographic Hash Functions in File Integrity Verification
Cryptographic hash functions play a fundamental role in ensuring file integrity. These functions generate a fixed-length hash value for a given file, ensuring that any modification results in a completely different hash value. Commonly used hash functions include:
•	MD5 (Message Digest Algorithm 5): Although widely used, it is now considered insecure due to collision vulnerabilities.
•	SHA-1 (Secure Hash Algorithm 1): More secure than MD5 but deprecated due to cryptographic weaknesses.
•	SHA-256 (Secure Hash Algorithm 256-bit): A strong hashing function recommended for secure file integrity verification.
The file integrity checker developed in this project employs SHA-256 due to its resilience against attacks and ability to ensure reliable monitoring.

2.4 Review of File Integrity Monitoring (FIM) Techniques
File Integrity Monitoring (FIM) tools provide mechanisms to detect unauthorized modifications in critical files. Various approaches are used in FIM, including:
1.	Baseline Hash Comparison: Generates an initial hash value and periodically compares it with the current hash to detect changes.
2.	Access Control Monitoring: Logs file access activities to identify unauthorized modifications.
3.	Real-Time Monitoring: Continuously monitors files and triggers alerts upon detecting changes.
4.	Version Control Systems: Maintains file history, allowing rollback to previous versions if integrity is compromised.
Several FIM tools, such as Tripwire, OSSEC, and AIDE (Advanced Intrusion Detection Environment), employ these techniques to enhance cybersecurity.

2.5 Review of Challenges in File Integrity Monitoring
Despite advancements in FIM technologies, several challenges persist:
•	Performance Overhead: Frequent hash computations on large datasets can slow system performance.
•	False Positives: Legitimate file modifications may trigger unnecessary alerts, leading to alert fatigue.
•	Storage Requirements: Storing hash values for numerous files consumes significant storage space.
•	Advanced Cyber Threats: Attackers continuously develop methods to evade traditional integrity checks.
Addressing these challenges requires innovative approaches, including AI-based anomaly detection and enhanced cryptographic methods.

2.6 design Framework





                                                                  
	
	




	
                                                           



                                                

2.7 Research Gap and Emerging Trends
The literature review identifies key research gaps in file integrity monitoring, including:
•	Blockchain-Based File Integrity Verification: The use of decentralized ledgers to store and validate hash values.
•	Artificial Intelligence (AI) in FIM: Leveraging machine learning models to distinguish between legitimate and unauthorized changes.
•	Hybrid Integrity Monitoring Systems: Combining cryptographic hashing with behavioral analysis for improved detection.
•	Quantum-Resistant Hashing: Developing cryptographic functions resistant to emerging quantum computing threats.
These trends present opportunities for further enhancements in file integrity verification, making monitoring systems more robust and resilient against evolving cyber threats.

2.8 Conclusion
Ensuring file integrity is essential for maintaining cybersecurity and preventing data manipulation. Cryptographic hashing is a core method for verifying file authenticity, with SHA-256 emerging as a preferred choice due to its security strength. Traditional FIM tools provide effective monitoring, but challenges such as performance overhead and false positives necessitate further innovation. Emerging trends, including blockchain and AI-based monitoring, offer promising directions for enhancing file integrity verification. This literature review lays the foundation for the development of an advanced file integrity checker tailored to modern security needs, addressing existing challenges and integrating cutting-edge cybersecurity technologies.










CHAPTER THREE: RESEARCH METHODOLOGY
3.1 Introduction
 This chapter outlines the methodology employed in developing the File Integrity Checker, a tool designed to ensure the authenticity and security of files through cryptographic hash functions. The chapter details the research design, location of the study, data collection methods, system development methodology, and ethical considerations.
3.2 Research Methodology 
A mixed-methods approach was adopted, combining both qualitative and quantitative research. The quantitative aspect involved evaluating the performance of different hashing algorithms (MD5, SHA-1, SHA-256) in detecting file modifications, while the qualitative aspect focused on user feedback regarding the usability and efficiency of the integrity checker.

3.3 Development Methodology
Development Approach: The software development methodology chosen for the File Integrity Checker is Agile. Agile development is suitable for this project due to its iterative nature, allowing continuous improvements, quick adaptability to feedback, and incremental development of features. Given the project’s requirements, including real-time file monitoring and hash comparison, Agile ensures that core functionalities are progressively refined.

3.4 Programming Methodology
 Modular programming was used, ensuring each component (hashing, file monitoring, real-time alerts) functioned independently while integrating seamlessly into the overall system.
3.5 System Analysis and Design 
The Agile approach allowed for continuous refinement, with defined user stories and sprint cycles focusing on improving functionality.



























3.6 Context Diagram
 
Figure 3



A high-level context diagram illustrates how the integrity checker interacts with users and system components.
3.7 Research Ethics 
Measures were taken to ensure the confidentiality and security of test data. Ethical considerations included:
•	Confidentiality: Ensuring test data was anonymized and encrypted.
•	Accountability: Acknowledging contributions from previous research.
•	Transparency: Documenting all methods and findings clearly.
•	Social Responsibility: Contributing to improved cybersecurity practices.













CHAPTER FOUR: SYSTEM DEVELOPMENT AND DEPLOYMENT
4.0 System Development and Deployment 
This chapter presents the system’s architecture, implementation, and testing procedures. It details the technologies used, system components, and deployment strategies.

4.1 System Description and Deployment
The File Integrity Checker is designed to monitor file changes using cryptographic hash functions. Users can select files for integrity monitoring, and the system automatically checks for alterations at defined intervals. If a file is modified, an alert is triggered to notify the user. The system consists of a front-end user interface (UI) and a back-end processing unit that handles file hashing, comparison, and reporting.
Deployment involves installing the application on client systems with necessary permissions to access files for monitoring. The system supports local and cloud-based storage, providing flexibility for different user needs. The deployment process includes configuration settings, user authentication, and scheduled monitoring setup.

4.3Front-End Development 
The front-end was developed using modern web technologies, ensuring a responsive and intuitive user experience. The UI was designed with simplicity in mind, allowing both technical and non-technical users to navigate the system efficiently.

4.4 User Interface Design  
The UI includes:
•	A login page for secure access.

 
Figure 4 login page of the file integrity system

•	A dashboard displaying monitored files.
 
Figure 5 : dashboard displaying file paths of monitored files

•	Real-time alerts for detected file modifications.

 
Figure 6: alerts on file changes
 
Figure 7: file status displayed

4.5 Back-End Development 
The back-end handles data processing, authentication, and integrity checks. It was developed using:
-SHA-256 Cryptographic Hash Algorithm for file integrity verification.
-Python and Flask for server-side logic and API development.
-MONGODB for database management

4.6 Database Design Models
 The system stores hashed values and logs of file integrity checks in a structured database to enable efficient retrieval and analysis.
4.7 System Testing
 Testing included:
•	Unit Testing: Evaluating individual components for correctness.
•	Integration Testing: Ensuring seamless interaction between modules.
•	User Acceptance Testing: Gathering feedback on usability and performance.
4.8 Conclusion
 The system successfully detects unauthorized file modifications and provides real-time alerts, contributing to enhanced data security.
4.9 Recommendations
•	Expanding support for additional cryptographic hash functions.
•	Enhancing automation for remediation actions upon detecting file modifications.








CHAPTER FIVE: CONCLUSION AND RECOMMENDATIONS
5.1 Introduction
This chapter summarizes the study, highlighting key findings and proposing future improvements. It also provides recommendations for further enhancements and research directions.
5.2 Summary of Findings
The File Integrity Checker effectively detects file modifications using cryptographic hashing techniques and provides real-time monitoring capabilities. Through rigorous testing, the system has demonstrated accuracy in identifying unauthorized changes, ensuring data integrity, and offering timely alerts to users.
5.3 Conclusion
The tool successfully addresses challenges associated with unauthorized file changes, contributing to improved cybersecurity. By leveraging cryptographic hashing and automated monitoring, the system enhances file security and minimizes risks associated with data tampering. Its modular architecture ensures flexibility, allowing for future expansions and integrations.
5.4 Recommendations
Future work should focus on:
•	Integrating blockchain-based verification for enhanced security, ensuring immutable file integrity records.
•	Extending the tool to cloud-based file storage systems, enabling broader accessibility and seamless integration with cloud environments.
•	Enhancing the user experience by incorporating a more intuitive interface and additional customization options for file monitoring.
•	Implementing real-time collaboration features for organizations needing multi-user monitoring capabilities.
5.5 Future Research Directions
Further studies should explore:
•	AI-driven anomaly detection techniques to minimize false positives and improve detection accuracy, leveraging machine learning models for adaptive security.
•	Advanced encryption methods to complement hash-based integrity verification, adding an extra layer of protection.
•	Cross-platform compatibility to support different operating systems, including mobile devices, for wider usability.
•	Behavioural analysis techniques to detect sophisticated file modification patterns linked to cyber threats.  



References
Books  
1. Stallings, W. (2018). Cryptography and Network Security: Principles and Practice. Pearson.  
2. Bishop, M. (2005). Introduction to Computer Security. Addison-Wesley.  
3. Schneier, B. (1996). Applied Cryptography: Protocols, Algorithms, and Source Code in C. Wiley. 

Online Sources  
7. National Institute of Standards and Technology (NIST). (2021). Guide to Computer Security Log Management (NIST SP 800-92). Retrieved from [https://www.nist.gov](https://www.nist.gov)  
8. OWASP. (2023). File Integrity Monitoring. Retrieved from [https://owasp.org](https://owasp.org)  
9. MITRE ATT&CK Framework. (2024). File Integrity Checking in Cybersecurity. Retrieved from [https://attack.mitre.org](https://attack.mitre.org)




























