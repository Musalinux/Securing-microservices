# Securing Microservices in Cloud Containers

This repository contains the implementation of the dissertation project titled **"Securing Microservices in Cloud Containers"**, completed as part of the requirements for the Master of Science in Cyber Security at Nottingham Trent University. The project focuses on securing microservices deployed in cloud containers by integrating robust security measures into the CI/CD pipeline using AWS services.

## Microservice Application Screenshot
![image](https://github.com/user-attachments/assets/e7fd736b-a199-4def-9962-7518d371d315)

## Abstract

The rapid adoption of microservices and containerized architectures in cloud computing has introduced unique security challenges. This project proposes a scalable and automated security framework leveraging advanced AWS tools, including:

- **AWS Macie** for sensitive data protection
- **Amazon GuardDuty** for threat detection
- **AWS Inspector** for vulnerability management
- **AWS Security Hub** for centralized security insights
- **AWS Config** for compliance enforcement

By integrating these services into a CI/CD pipeline, the solution ensures robust, adaptive, and scalable security for cloud-native applications.

## Features

- **Microservices Design:** Modular architecture with user, product, and frontend services.
- **AWS-based Deployment:** Services deployed on Amazon ECS with Fargate.
- **CI/CD Integration:** Automated security checks embedded within the pipeline.
- **Security Tools:** Continuous monitoring, vulnerability scanning, and compliance automation.
- **Threat Scenarios:** Testing for geo-blocking, IP whitelisting, and DDoS simulations.

## Architecture Diagram
![image](https://github.com/user-attachments/assets/c8864d85-cb0e-461e-9cbd-0e3f07c39ade)


The project utilizes a containerized microservices architecture deployed on AWS, with:

1. **Frontend Service**: Flask-based UI for user interactions.
2. **Product Service**: Handles product-related operations.
3. **User Service**: Manages user authentication and profiles.
4. **Amazon ECS**: Orchestrates microservices.
5. **AWS Security Tools**: Implements layered security.

## Project Lifecycle Diagram 
![image](https://github.com/user-attachments/assets/7f930177-6dc4-43ad-92af-87d1e7ed386e)

## Project Repository Structure

```
.
├── Frontend
│   ├── Dockerfile
│   ├── app.py
│   └── requirements.txt
├── ProductService
│   ├── Dockerfile
│   ├── app.py
│   └── requirements.txt
├── UserService
│   ├── Dockerfile
│   ├── app.py
│   └── requirements.txt
├── docker-compose.yml
├── README.md
└── CI/CD_pipeline_scripts
```

## Getting Started

### Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [AWS CLI](https://aws.amazon.com/cli/)
- [AWS Account](https://aws.amazon.com/free/)
- Python 3.8+

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/dissertation-microservices.git
   cd dissertation-microservices
   ```

2. Build and run the containers locally:

   ```bash
   docker-compose up --build
   ```

3. Deploy to AWS ECS:

   - Configure AWS CLI with credentials:
     ```bash
     aws configure
     ```
   - Use the provided deployment scripts in the `CI/CD_pipeline_scripts` directory.

4. Access the application at `http://<public-ecs-endpoint>:3000`.

## AWS CodePipeline 
![image](https://github.com/user-attachments/assets/00862e2c-5ece-4288-9f9a-3c716fe7dbd3)

## Security Features

- **Data Protection**: Automated scanning for sensitive data with AWS Macie.
- **Threat Detection**: Continuous monitoring using Amazon GuardDuty.
- **Vulnerability Management**: Automated scans via Amazon Inspector.
- **Compliance**: Enforcement of AWS Config conformance packs.
- **Geo-blocking and IP Filtering**: Implemented via AWS WAF.

## Testing and Evaluation

Comprehensive testing was performed to validate the security measures, including:

- **Threat Scenario Testing:** Simulated geo-blocking and IP filtering.
- **Vulnerability Assessments:** Using tools like AWS Inspector and manual penetration tests.
- **Compliance Checks:** Automated through AWS Config.

Test cases and results are documented in the `test_results` directory.

## Future Scope

- Extend the framework to support multi-cloud environments.
- Integrate machine learning for anomaly detection.
- Implement runtime security policies for Kubernetes-based deployments.

## Author

**Musaddik Vasaikar**

- Master of Science in Cyber Security
- Nottingham Trent University, 2024

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- **Supervisor**: Alexandros Konios for guidance and support.
- **Family**: For encouragement and motivation.
- **AWS Educate**: For providing resources to execute the project.

---
For more details, refer to the [dissertation report](link-to-report) or the [presentation slides](link-to-slides).
