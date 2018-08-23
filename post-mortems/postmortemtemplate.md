# Name of the postmortem, e.g. “API Outage Postmortem”

## Date

When the incident happened, e.g. “30-05-2018”

## Authors

List of people who wrote the postmortem  in the following format:

* Jane Doe
* John Doe

## Status

Current status of the postmortem, e.g. “Complete, action items in progress”

## Summary

A one-sentence summary of the incident, usually something like “Service X was down for N minutes due to Y”

## Impact

 The incident’s impact on customers and, if known, revenue or reputation, e.g. “Users were unable to do X while service Y was unavailable from 09:29 to 10:00 UTC”

## Root Causes

A list of causes that have contributed to the incident

## Trigger

What triggered the outage? e.g. “Merging pull request X which started the rollout of broken software Y”

## Resolution

The action(s) that mitigated and resolved the outage, e.g. “Disabling feature X helped to mitigate the problem. Rolling back to version Y resolved it.”

## Detection

How the problem was noticed, e.g. “AppDynamics detected that service X was down and sent an alert email to...”

## Action Items

A list of actions taken (with links to Trello cards) to mitigate or resolve the incident, and to prevent it from recurring

| Action Item | Type | Owner | Trello Card |
| ----------- | ---- | ----- | --- |
| Update playbook with instructions for responding to cascading failure | mitigate | emma | [TRELLO](https://trello.com/c/XXXXXX) **DONE** |
| Use flux capacitor to balance load between clusters | prevent | andrew | [TRELLO](https://trello.com/c/XXXXXX) **TODO** |
| Freeze production until 20-11-2018 due to error budget exhaustion, or seek exception due to grotesque, unbelievable, bizarre, and unprecedented circumstances | other | Jane | n/a **TODO** |

## Lessons Learned

What went well? What went wrong? And what was sheer luck?

### What went well

* 
* 

### What went wrong

* 
* 

### Where we got lucky

* 
* 

## Timeline

A detailed timeline of the events related to the incident

20-11-2018 (*all times UTC*)

| Time  | Description |
| ----- | ----------- |
| 14:51 |             |
| 14:53 |             |
| 14:54 | **OUTAGE BEGINS**  |
| 14:55 |  |
| 14:57 | |
| 14:58 | Jane starts investigating, finds xxxx |
| 15:01 | **INCIDENT BEGINS** Jane declares incident #465 due to xxx |
| 15:36 | **OUTAGE MITIGATED**, updated index replicated to all clusters |
| 15:39 | |
| 16:00 | **OUTAGE ENDS**,  |
| 16:30 | **INCIDENT ENDS**, |

## Supporting Information

Additional graphs, screenshots, command output, etc.

* Monitoring dashboard, <http://monitoringdashboard.local>