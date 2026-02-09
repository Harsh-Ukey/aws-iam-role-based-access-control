# AWS IAM Role-Based Access Control Project

## Project Level
Beginner / Foundational Cloud Security Project

## Objective
Demonstrate how AWS Identity and Access Management (IAM) is used to control access to AWS services using users, groups, and policies based on job roles.

## Business Scenario
A company uses Amazon EC2 and Amazon S3 extensively and needs to grant access to employees based on their job function:

| User   | Group        | Permissions |
|-------|--------------|-------------|
| user-1 | S3-Support   | Read-only access to Amazon S3 |
| user-2 | EC2-Support  | Read-only access to Amazon EC2 |
| user-3 | EC2-Admin    | View, Start, and Stop EC2 instances |

## AWS Services Used
- AWS Identity and Access Management (IAM)
- Amazon EC2
- Amazon S3

## IAM Design
- Users are assigned to **groups**
- Permissions are granted using **managed and inline policies**
- Users inherit permissions from their group membership
- Access is validated through AWS Console login

## Implementation Steps
1. Explored pre-created IAM users and groups
2. Inspected managed policies:
   - AmazonEC2ReadOnlyAccess
   - AmazonS3ReadOnlyAccess
3. Inspected inline EC2 Admin policy
4. Assigned users to appropriate IAM groups
5. Retrieved IAM sign-in URL
6. Logged in as each user and tested permissions
7. Verified allowed and denied actions based on policies

## Permission Testing Results
- user-1: Can view S3 buckets, denied EC2 access
- user-2: Can view EC2 instances, denied EC2 stop and S3 access
- user-3: Can view and stop EC2 instances successfully

## Key Learnings
- Importance of least privilege access
- Difference between managed and inline IAM policies
- How group-based access simplifies permission management
- Practical validation of IAM policies

## Screenshots
Screenshots demonstrating successful and denied access are available in the `screenshots/` folder.

## Notes
This project was performed in an AWS Academy lab environment with restricted permissions.

## Author
Harsh Ukey
