# AWS Backup Plan for EC2 and RDS

## Objective

The goal of this project is to learn how to configure automated backup and recovery for AWS resources using AWS Backup. The project covers launching an EC2 instance and an RDS database, storing some sample data, creating a centralized AWS Backup plan, and validating backups using on-demand runs.

---

# 1. Infrastructure Setup

## 1.1 Launch EC2 Instance

* Launched an EC2 instance using Amazon Linux 2 / Ubuntu
* Connected to the instance
* Installed a sample web server (Apache / Nginx)
* Created a sample HTML or text file as test data

### Screenshot: EC2 Instance Running

Add screenshot of EC2 instance running in AWS console

```
screenshots/01-ec2-instance-running.png
```

---

## 1.2 EC2 Test Data / Web Server Confirmation

* Verified that the web server or file is accessible
* Ensured data exists to validate backup usefulness

### Screenshot: EC2 Test Page / File

```
screenshots/02-ec2-test-data.png
```

---

## 1.3 Launch RDS Instance

* Created an RDS instance using MySQL or PostgreSQL
* Configured security group and credentials
* Created a test database and sample table
* Inserted sample data

### Screenshot: RDS Instance Running

```
screenshots/03-rds-instance-running.png
```

---

## 1.4 RDS Test Data Verification

* Connected to the database
* Verified sample data is inserted successfully

### Screenshot: RDS Sample Table / Data

```
screenshots/04-rds-test-data.png
```

---

# 2. AWS Backup Configuration

## 2.1 Open AWS Backup Service

* Navigated to AWS Backup from the AWS Console

### Screenshot: AWS Backup Service Home

```
screenshots/05-backup-service-dashboard.png
```

---

## 2.2 Create Backup Vault

* Created a Backup Vault (or used default vault)
* Selected encryption settings
* Saved the vault

### Screenshot: Backup Vault Created

```
screenshots/06-backup-vault-created.png
```

---

## 2.3 Create Backup Plan

* Created a Backup Plan
* Defined backup rule

  * Frequency (daily/weekly)
  * Retention period
  * Lifecycle rules if required
* Selected Backup Vault for storage

### Screenshot: Backup Plan Configuration

```
screenshots/07-backup-plan-details.png
```

---

## 2.4 Assign Resources

* Added EC2 instance to the backup plan
* Added RDS instance to the backup plan
* Used either resource ID or tags

### Screenshot: Resource Assignment Page

```
screenshots/08-resource-assignment.png
```

---

# 3. Validation and Reporting

## 3.1 Trigger On-Demand Backup

* Triggered an on-demand backup for EC2
* Triggered an on-demand backup for RDS

### Screenshot: On-Demand Backup Trigger

```
screenshots/09-on-demand-backup.png
```

---

## 3.2 Verify Backup Jobs

* Opened Backup Jobs in AWS Backup
* Confirmed EC2 and RDS backup jobs appeared
* Waited until status changed to Completed

### Screenshot: Backup Jobs Completed

```
screenshots/10-backup-jobs-completed.png
```

---

## 3.3 Verify Recovery Points

* Navigated to Protected Resources
* Selected EC2
* Viewed Recovery Points
* Repeated same for RDS

### Screenshot: EC2 Recovery Point

```
screenshots/11-ec2-recovery-point.png
```

### Screenshot: RDS Recovery Point

```
screenshots/12-rds-recovery-point.png
```

---

# Deliverables

## Screenshots Submitted

* EC2 instance running
* RDS instance running
* Backup Plan configuration
* Backup Vault with recovery points
* Backup Jobs showing completion
* EC2 Recovery Points
* RDS Recovery Points

---

# Short Report

## Steps Followed

* Created EC2 and RDS resources
* Added sample data
* Configured AWS Backup Vault and Plan
* Assigned EC2 and RDS resources
* Triggered on-demand backup
* Verified results

## Key Configuration Details

* Backup Frequency: as configured in backup rule
* Retention Period: as defined in backup plan
* Backup Vault: default or custom vault used

## AWS Sections Used

* EC2 Console
* RDS Console
* AWS Backup:

  * Backup Plans
  * Protected Resources
  * Backup Jobs
  * Recovery Points

## Issues Faced and Resolved

* Backup schedule delay warning resolved by using on-demand backup
* Ensured correct AWS region
* Verified IAM permissions