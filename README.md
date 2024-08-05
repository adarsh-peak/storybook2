# hub-bamboo-insea-sync

## Introduction
This repository contains a Cron task that fetches employee data for all the tenants mentioned in env as `bamboo_tenants` with geo location `insea` using the BambooHR service and syncs it with specific tables in the database.

## Functionality
The cron task performs the following operations:
  - Backups the current tables. - `_backup_existing_tables`
  - Deletes previous backups. - `_delete_previous_backups`
  - Truncates all tables. - `_truncate_existing_tables`
  - Syncs the data from bamboo hr to the current tables. - `_create_employee_model` & `_remove_outdated_users`
  - Sends out email notifications to recievers mentioned in the env. - `notify_job_status`

## Tables Synced
  - `employee` 
  - `employee_profile` 
  - `employee_enc`

## Cron Schedule
Cron job is scheduled to run every day at 11:00AM UTC.
