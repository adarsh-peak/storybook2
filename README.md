# hub-bamboo-insea-sync

## Introduction
This Cron task fetches user data for the tenant `sequoiacap` with geo location `insea` using the BambooHR service and syncs it with the following tables:
  - `employee`
  - `employee_profile`
  - `employee_enc`

## Cron Schedule
Cron job is scheduled to run every day at 11:00AM
