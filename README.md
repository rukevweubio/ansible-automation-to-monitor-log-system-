# Ansible Automation to Monitor Log System

This project leverages Ansible to automate the process of scraping logs from databases such as MySQL and PostgreSQL. It also integrates with cron for scheduling and automation, ensuring that log scraping tasks are executed at regular intervals without manual intervention.

## Project Description

The goal of this project is to provide an automated solution for monitoring and collecting logs from database systems. By using Ansible, the project simplifies the process of managing log scraping tasks across multiple servers. The integration with cron ensures that these tasks are performed on a predefined schedule, making the system efficient and reliable.

## Prerequisites

Before using this project, ensure that you have the following:

1. **Ansible**: Installed on your control machine. Follow the [Ansible installation guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html) if needed.
2. **Databases**: MySQL and/or PostgreSQL installed and configured on the target servers.
3. **Python**: Installed on both the control machine and target servers.
4. **Cron**: Available on the target servers for scheduling tasks.
5. **SSH Access**: Ensure passwordless SSH access is configured between the control machine and the target servers.


![data flow ](https://github.com/rukevweubio/ansible-automation-to-monitor-log-system-/blob/main/Concept%20map.png)

## Installation

1. Clone this repository to your local machine:
  ```bash
  git clone https://github.com/your-repo/ansible-automation-to-monitor-log-system.git
  cd ansible-automation-to-monitor-log-system
  ```

2. Install the required Ansible collections and dependencies:
  ```bash
  ansible-galaxy install -r requirements.yml
  ```

3. Configure your inventory file (`inventory.ini`) with the details of your target servers.

## Usage

1. Update the variables in the `vars/` directory to match your database configurations (e.g., database credentials, log file paths, etc.).

2. Run the Ansible playbook to scrape logs:
  ```bash
  ansible-playbook ansible-playbook.yaml -i inventory.ini
  ```

3. To automate the log scraping process, use the provided cron task configuration. The playbook includes tasks to set up cron jobs on the target servers.

## Playbook Structure
![ansible automation ](https://github.com/rukevweubio/ansible-automation-to-monitor-log-system-/blob/main/piturefile/Screenshot%20(610).png)

![ansible automation ](https://github.com/rukevweubio/ansible-automation-to-monitor-log-system-/blob/main/piturefile/Screenshot%20(607).png)

![ansible automation ](https://github.com/rukevweubio/ansible-automation-to-monitor-log-system-/blob/main/piturefile/Screenshot%20(608).png)

![ansible automation ](https://github.com/rukevweubio/ansible-automation-to-monitor-log-system-/blob/main/piturefile/Screenshot%20(612).png)

