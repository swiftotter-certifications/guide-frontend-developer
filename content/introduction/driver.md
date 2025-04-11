<div class="page-break"></div>

### Driver - The database automation tool
How do you get the database from production to staging? Or back to local? And ensure that customer data is properly sanitized from the database? Or prevent those external API keys from trickling back to local and then trashing production data?

[Meet Driver](https://github.com/swiftotter/driver). This is a tool that allows you to automatically sanitize tables-with a snap-in for Magento.

**Environments:**

You can output to different environments (as in a different output for staging versus local). 

**Anonymization:**

Ensure that customer data is properly cleared out. We have supplied a standard package for Magento 2 tables. You can easily create your own custom anonymizations.

**How it works:**

We _never_ want to modify the local Magento database. Thus, we dump the database, push up to an RDS instance, run the transformations, export to a gzipped file and push to S3.

To load the data back from S3 into your staging or local environments, just run a command for this.

### This tool has been transformational for SwiftOtter's processes.
