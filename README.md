# Application Migration Using AWS MGN  

## Overview  
Migrated a **Virtual Machine (VM) from Oracle VB/EC2 to AWS EC2** using **AWS Application Migration Service (MGN)**, ensuring minimal downtime and seamless transition. The migration replicated the entire system, including **web server configurations, application files, and system settings**, to a new EC2 instance while maintaining operational consistency.  

## Migration Process  

- **Set up a source VM** on **Oracle VirtualBox/EC2**, installed **Apache Web Server**, and created sample files to validate migration integrity. Configured a simple webpage displaying "Application Migration Successful" to test post-migration functionality.  

- **Configured AWS MGN for migration**, adding the server in the **Application Migration Console**, selecting **Replicate all Disks**, and providing **AWS Access and Secret Keys** to initiate the replication process.  

- **Installed and configured AWS Replication Agent** on the source VM, ensuring real-time data synchronization to the AWS **Replication Server**. Monitored replication progress in the **AWS MGN Console** while waiting for the data sync to complete.  

- **Launched a test instance** from the replicated data, confirming that the web application and all files were successfully migrated. Verified that the test instance functioned identically to the original VM before proceeding with the cutover.  

- **Finalized the migration by launching the cutover instance**, ensuring a smooth transition from the original VM to AWS EC2. Marked the instance as **Ready for Cutover** and finalized the migration.  

- **Verified the migration by accessing the new EC2 instance via Public IP**, confirming that the web server and application were running correctly. Resolved network issues by enabling **public IP assignment** if necessary.  

## Outcome  
- Successfully migrated the **VM to AWS EC2**, maintaining application integrity and system functionality.  
- Ensured **zero manual reconfiguration**, with all settings and data mirrored seamlessly.  
- Optimized application availability and minimized migration downtime using **AWS MGN**.  

## Future Improvements  
- Automate the migration process using **Terraform** or **AWS CLI scripts**.  
- Implement **CloudWatch monitoring** to track replication and cutover performance.  
- Explore **AWS Systems Manager** for post-migration instance management.  

