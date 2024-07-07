# fullstack-repo

## Overview

This README outlines the workflow implemented to manage multiple repositories on GitHub, integrating them into a unified project while maintaining distinct repositories (frontend-repo, backend-repo, and fullstack-repo). The setup utilizes submodules, automated workflows, and secure environment management to enhance productivity and collaboration.

## Research

Before implementation, thorough research was conducted to ensure a robust setup. This included reviewing GitHub's official documentation, educational resources, and engaging in community discussions. Direct consultations with stakeholders provided insights into project requirements and alignment.

## Implementation

### Initial Setup

- **Repositories Initialization:**
  - Created frontend-repo and backend-repo, each with a main branch.

- **Fullstack-repo Repository:**
  - Established fullstack-repo as a central repository integrating frontend-repo and backend-repo as submodules for unified control and updates.

### Configuration and Workflow Integration

#### Environment Variable Management

- Utilized environment variables across repositories (frontend-repo and backend-repo) to manage configuration settings centrally.

#### Python Integration

- Developed scripts in frontend-repo and backend-repo to dynamically read environment variables for configuration.

#### Security with PATs

- Implemented Personal Access Tokens (PATs) with restricted permissions, securely stored in GitHub secrets, to manage operations securely across repositories.

### Automated Workflows

#### Individual Repo Workflows

- Configured workflows in frontend-repo and backend-repo triggered by push events, notifying fullstack-repo of updates.

#### Fullstack-repo Workflow

- Implemented a workflow in fullstack-repo responding to notifications, facilitating submodule updates and merge operations.

### Challenges

- **Documentation Navigation:**
  - Initially encountered challenges navigating extensive documentation, resolved through thorough exploration and focused research.

- **Repository Permissions:**
  - Overcame issues with repository write permissions in GitHub Actions by refining workflow permissions and leveraging community-provided solutions.

- **Workflow Implementation:**
  - Attempted to implement a post-push workflow but encountered limitations, particularly with triggering events correctly. After several attempts and troubleshooting, it was decided to rely on post-commit hooks for repository updates instead, ensuring stability and consistency in workflow execution.

## Conclusion

This workflow effectively consolidates multiple repositories into a unified project structure (fullstack-repo), ensuring streamlined development processes and enabling seamless updates across project components.
