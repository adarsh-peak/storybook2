# hub-bamboo-insea-sync

## Introduction
This repository contains a Cron task that fetches employee data for all the tenants mentioned in env as `bamboo_tenants` with geo location `insea` using the BambooHR service and syncs it with specific tables in the database.

## Functionality
The cron task performs the following operations:
  - Backups the current tables.
  - Deletes previous backups.
  - Truncates all tables.
  - Syncs the data from bamboo hr to the current tables.
  - Sends out email notifications to recievers mentioned in the env.

## Tables Synced
  - `employee` 
  - `employee_profile` 
  - `employee_enc`

## Cron Schedule
Cron job is scheduled to run every day at 11:00AM UTC.
