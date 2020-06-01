# Ansible

## Philosophy

- Just enough abstraction of text (yaml) to orchestrate tasks.

## What

- Is a task execution framework and lightweight fleet management system
- Mostly, automation through playbooks.
- No agents, state or bootstraps.

## How

- Is designed to work on numerous machines at once.
- Modes of operation
    - Linear
    - Rolling deploys
    - Free strategy (run as fast as it can)
- Written in Python and using YAML configuration files
- Is developed by RedHat and is open source.

## Elements

- Inventories are colelction of hosts.
    - Has variables in key value pairs.
    - Has static and dynamic inventory sources
    - Uses ini format files.
- Groups of hosts is the next step.
- Patterns filter inventories and groups.
- Tasks
    - To execute a desired action.
    - Has task condiionals.
    - Tasks have controls to loop and determine if the task runs.
    - Task is attempted or skipped.
- Modules
    - Tasks are groups of tasks and are available in the community.
    - Just enough abstraction to execute specific tasks.
- Playbooks
    - Contains an orchestration of plays.
    - Is stored in YAML files
    - Use three dashs for a yaml file.
- Orchestration
    - Complicated tasks with important order.
- Templates
    - Uses mustache formatting.
- Handlers
    - React to task chnages via notif.
    - Handlers are tasks with special meaning.
- Forks
    - Split tasks to run in paralell.

## Extensions

- Three types
    - Modules, Plugins, and dynamic inventories (cloud etc)
    - Modules
        - From the location `/usr/share/ansible/sitemod.py`
    - Plugins
        - Extends core
    - Dynami Inventories
        - JSON data
        - Infra as a service

## Example

```bash
ansible -i hosts host1 -m command -a "uname -r"
```
