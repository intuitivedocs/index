---
title:  "Code Review"
---

## Purpose
- To identify any defects in the development before the development is released to the QA team.
- To ensure that the development meets the agreed upon specification.
- To ensure that intuitive coding practices are followed.
- To identify any pre-requisites that need to be created.
- Resolution of any merge conflicts to the destination branch.


## Roles
- **Developer**
	- The member of the development team that has carried out the work that is being code reviewed.
- **Code Reviewer**
	- A senior member of the development team verifying the work.  Usually a Tech Lead, but can be a Senior Developer or Team Lead.

## Entry Criteria
- **Developer** has completed the development.
- **Developer** has completed adequate testing.
- A **Code Reviewer** with the required experience is available.
- **Developer** has marked the development as 100% complete in JIRA and moved the development from *In Progress* to *Code Review*.
- **Developer** has the correct code and database branches on their machine.
- **Developer** has created the pull request to the correct destination branch in all modified repositories.


![Code Review Process](/DevelopmentTeamProcess/images/CodeReview/CodeReviewFlow.png)


## Tasks
T1. 	BBD Analysis: **Code Reviewer** goes through the BDD and the **Developer** demonstrates that each BDD scenario has passed.  Any issues are noted down.

T2.		Correct Defects:  **Developer** fixes any defects raised under T1 or T3.  Following the the **Developer** restarts the Code Review Process.

T3.		Code Analysis: **Code Reviewer** goes through the code changes to ensure a good qualit of code is being commited (e.g. no commented out code, good white spacing, follows DTY, follows SOLID, no StyleCop exceptions if the code is in C#).  Any issues are noted down and the **Developer** fixes the issues under T2.

T4.		Creation of Pre-Requisites:  **Code Reviewer** following the knowledge gained in T1 and T2 creates any applicable Release Pre-Requisites in JIRA.

T5.		Merge Conflicts:  **Code Reviewer** fixes any merge conflicts with the destination branch.

T6.		Merge:  **Code Reviewer** merges the work into the destination branch.

T7.		JIRA Admin:  **Code Reviewer** moves the JIRA status of the ticket to *Pending*.

## Verification
N/A

## Exit Criteria
- Code is merged into the destination branch
- All BDD scenarios pass
- JIRA ticket status is in *Pending*

## Deliverables
D1. Release Pre-Requisites

## Quality Records
N/A