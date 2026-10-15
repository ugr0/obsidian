---
URL: https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/encrypt-an-existing-amazon-rds-for-postgresql-db-instance.html
Glasp URL: https://glasp.co/f5XC0CoKGYhSNqcjs12752ID2q02/p/9fKkJGCRje45lNt9KM94
Tags: []
Last updated: 2023-11-26
---
#### Highlights & Notes

> by creating a snapshot of your DB instance, and then creating an encrypted copy of that snapshot. You can then restore a DB instance from the encrypted snapshot to get an encrypted copy of your original DB instance.

> if your project doesn’t allow for significant downtime for this activity, you need an alternate approach that helps minimize the downtime. This pattern uses the AWS Database Migration Service (AWS DMS)


