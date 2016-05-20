---
title: "Test Deployments"
---

## Purpose
- To update the client's test system to allow QA to test the features before handing over to the customer.

## Roles
- **Dev Resource**
	- Senior member of the development team responsible for the customer.
- **Project Manager**
	- The Project Manager responsible for the customer.
- **Bamboo**
	- The automated build and deployment software used.

## Entry Criteria
- Bamboo builds for all required projects are configured for the required fix version and passing.
- Bamboo deployments all required products are configured.
- Either
	- The customer as requested an ad-hoc test update
	- The overnight deployment deployment has been triggered

![Test Deployment Process](/DevelopmentTeamProcess/images/TestDeployment/TestDeploymentFlow.png)

## Tasks
T1. 	Run Artefact Builds: **Bamboo** To run the artefact builds

T2.		 Atefact Deployments: **Bamboo** To run the artefact deployments

T3.		Notifications sent: **Bamboo** to send emails to **Dev Resource** and **Project Manager** regarding the success of the builds

T4.		Automated JIRA changes:  **Bamboo** moves the tickets that have been updated out of *Pending*

T5.		Enact Pre-Requisites:  **Dev Resource** to ensure all Pre-Requisites tied to items now in the test system have been actioned

T6.		Correct Bamboo Failures:  Any failures from **Bamboo** need to be resolved by the **Dev Resource**
		

## Verification
V1.		Verify JIRA Statuses:  **Project Manager** to ensure that all tickets and pre-requisites have been completed and are in the correct status

## Exit Criteria
- Test environment has been updated
- All *Pending* tickets in the fix version have moved into  *In QA*

## Deliverables
N/A

## Quality Records 
N/A