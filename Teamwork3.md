# Teamwork III (DevOps, Best Practices, Tools)
## Team members
Tony Thesslund / e2101348

## 1. What is the main purpose of DevOps?
Improve collaboration between teams. Automate/simplify software development process.

## 2. What are the main stages of a CI/CD pipeline?
1. Code commit 
2. Build 
3. Test
4. Package 
5. Deploy

## 3. Which DevOps tools can be used for source control, CI/CD, containerization, infrastructure, configuration management, and monitoring?

**Source control**: Github, bitbucket

**CI/CD**: Jenkins, Azure devops, github actions

**Containerization**: Docker 

**infrastructure**: Terraform

**Configuration management**: Ansible

**Monitoring**: 
- Prometheus + Grafana
- Telegraf + InfluxDB + Grafana
- Zabbix


## 4. How can Git support effective collaboration in DevOps?
**Version control**

**Branching:** Developers can create feature or bugfix branches without risk of touching the main branch.

**Pull requests, Code review**

**CI / CD:** Automated builds, tests and deployment pipelines. 


## 5. What is Infrastructure as Code (IaC), and what are its benefits?
Infrastructure (software) defined as code. Version controlled, reviewed, tested and automated. 

IaC makes infrastructure management more consistent and repeatable

## 6. What is configuration management, and how can Ansible support it?
A tool for reducing the repetitive manual administration.

Ansible can support it by for example:
- Installing software
- Configuring servers
- Creating users
- Deploying applications
- Applying consistent settings across multiple machines

## 7. What are containers, and why are they useful in DevOps?
Containers are lightweight, isolated environments.

Software can be packaged into containers along with the required libraries and runtime configuration.

Containers help reduce differences between development, testing, and production environments.
## 8. What is container orchestration, and what role does Kubernetes play?
The automated management of containers across one or more machines.

Kubernetes can, for example, help with:
- Scheduling containers
- Scaling applications
- Restarting failed workloads
- Service discovery
- Rolling out new versions

## 9.  What are monitoring and observability, and which tools support them?
Collecting data from devices/virtual machines/applications via for example SNMP. Software like telegraf or prometheus is used for polling the data. Grafana can then be used to visualize the data using dashboards.

Examples of monitoring tools:
- Telegraf + InfluxDB + Grafana
- Prometheus + Grafana
- Zabbix
- PRTG
- Nagios

## 10. What is DevSecOps, and how does it improve software security?
Development approach that integrates automated security practices into the DevOps workflow.

It involves integrating security checks in CI/CD pipelines to detect vulnerabilities early.

## 11. Why is automated testing important in DevOps?
Problems can be detected and fixed faster.


## 12. What is configuration drift, and how can it be reduced?
A gradual change of system settings away from the planned and documented baseline.

Can be reduced by continuous monitoring, IaC and by enforcing clear rules, approvals and documentation for every modification.


## 13. Why are small and frequent deployments considered a DevOps best practice?
Faster troubleshooting and fixes.

## 14. What are the main steps for responding to a failed deployment?
1. Detection
     - Identify the failure 
     - Check logs
2. Decision
     - Assess the impact
     - Choose a strategy for solving the issue
3. Mitigation
    - Fix the issue
    - Verify it's working
4. Communication
    - Notify stakeholders 
    - Announce the fix
5. Postmortem
    - Review of what happened
    - Improve processes.


## 15. How can Git, Jenkins, Docker, Kubernetes, Terraform, Ansible, Prometheus, and Grafana work together?

Example:
1. Code is pushed to **Git**
2. **Jenkins** builds, tests and deploys the code
3. **Ansible** configures the software (and the server, if needed) based on configurations from **Terraform**
4. **Prometheus** collects data
5. **Grafana** visualizes the data