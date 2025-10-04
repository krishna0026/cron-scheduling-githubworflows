# Schedules Workflow
- useful for running jobs automatically at specific time like
- nightly builds, daily reports, cleanup tasks etc...

## Basic Syntex

```yml
name: Scheduled Workflow

on: 
    scheduled:
        - cron: "*/5 * * *" #Run on every 5 min
jobs:
    builds: 
        runs-on: ubuntu-latest

        steps:
            - name: Testing cron job
              run: echo "Hello from cron job"    

```