# Celebal_Devops_Week_7

✅ Task Summary
Task No.	Task Description	Completed
1	Create project with user groups and apply group policies	✅
2	Apply branch policies to restrict direct access to main for contributors	✅
3	Apply branch-level security & locks	✅
4	Configure branch filters & path filters	✅
5	Create and verify pull request workflow	✅
6	Implement triggers in build and release pipelines	✅
7	Add gates to pipelines (pre-deployment conditions)	✅
8	Enforce pull-request-only access and restrict direct merges	✅
9	Integrate work items into pipelines and trace builds	✅
10	Attach GitHub repo to Azure Boards	✅
🔍 Q1: Create a project with different user groups and implement group policies
Objective: Establish role-based access using user groups.



Summary:


Created project in Azure DevOps
Configured custom user groups like QA Team, New_Joiner
Applied permissions for Repos, Pipelines, Boards, and Artifacts
Linked with GitHub repository
Reference:


Microsoft Docs – Add Users to Team Project solution 
🔐 Q2: Apply branch policies so only the project administrator can access the master branch
Objective: Secure production branch access.

Summary:


Applied branch-level permissions
Denied Contribute to Contributors group
Allowed only Project Administrators to push/merge
Reference:

Branch Permissions in Azure DevOps solution 📎 Download Solution File
🔒 Q3: Apply branch security and locks
Objective: Enforce branch immutability during deployment cycles.


Summary:

Denied push and force push for contributors
Locked the main branch to freeze changes
Configured inheritance and granular permission levels
Reference:

Branch Policies and Locks solution 
🔃 Q4: Apply branch filters and path filters
Objective: Optimize CI/CD by targeting only necessary changes.


Summary:

Configured YAML pipeline triggers:
trigger:
  branches:
    include: [ main, develop ]
  paths:
    include: [ src/*, README.md ]
    exclude: [ docs/* ]
GUI-based filter policies set via Branch Policies
Reference:

Pipeline Triggers Docs solution 
🔁 Q5: Apply a pull request
Objective: Enforce code review before merging.


Summary:

Created feature branch PULL_FROM_AD
Made changes and pushed to remote
Created and merged a PR with admin approval
Reference:

Pull Requests in Azure DevOps solution 
🚀 Q6: Apply triggers in build and release
Objective: Automate CI/CD using triggers.


Summary:

YAML-based trigger setup:
trigger:
  branches:
    include: [ main ]
Classic UI triggers also applied via GUI
Release pipeline configured for CD with successful build trigger
Reference:

CI/CD Triggers Guide solution 
🛡 Q7: Apply gates to the pipeline
Objective: Implement pre-deployment validations.

Summary:


Created release pipeline with DeployToTest stage
Enabled 2-minute delay and approval gates
Ensured safe deployment flow
Reference:

Release Pipeline Gates solution 
🚫 Q8: Apply security so contributors can only create pull requests, not merge
Objective: Enforce pull-request-based merging only.

Summary:


Denied direct Contribute access to main
Enabled PR policies requiring minimum reviewers
Contributors allowed to raise PRs, not merge
Reference:

Branch Security Docs solution 
🔗 Q9: Use work items in pipelines
Objective: Enable traceability between work and builds.

Summary:


Used Fixes #<WorkItemID> in commit messages
Linked work items directly from PR UI
Enabled policy: "Check for linked work items"
Reference:

Work Items in Azure Pipelines solution 
🔄 Q10: Attach GitHub repo to Azure Boards
Objective: Enable GitHub-Azure DevOps integration.

Summary:


Connected GitHub repository to Azure DevOps project
Enabled real-time board activity and linking PRs
Reference:

GitHub Integration with Azure Boards solution 
📦 Tools Used
Azure DevOps: Boards, Repos, Pipelines, Releases
GitHub: Repo hosting & integration
YAML: Pipeline automation
Classic UI Pipelines: For visual configuration

📄 License
This project is part of a professional internship assignment and is for educational/demo purposes only.

"Secure, automate, trace – That’s the DevOps way."

Feel free to fork, star, or open issues for discussions!
