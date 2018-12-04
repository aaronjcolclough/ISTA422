1. What is Azure Blob Service?

The Azure Blob service gives you the ability to store files and access them from anywhere in the world by using URLs, the REST interface, or one of the Azure SDK storage client libraries.

2. What do you have to do to create Azure Blob Service?

To use the Blob service, you have to create a storage account. Once you have a storage account, you can create containers, which are similar to folders, and then put blobs in the containers.

3. What are some common scenarios where file share can be used?

Many on-premises applications use file shares; this makes it easier to migrate those applications that share data to Azure. If you mount the file share to the same drive letter that the on-premises application uses, the part of your application that accesses the file share should work without any changes. Configuration files can be stored on a file share and accessed by multiple VMs. Diagnostic logs, metrics, crash dumps, etc. can be saved to a file share to be processed and analyzed later. Tools and utilities used by multiple developers in a group can be stored on a file share to ensure that everyone uses the same version and that they are available to everyone in the group.

4. What is Locally Redundant Storage?

Azure Storage provides high availability by ensuring that three copies of all data are made synchronously before a write is deemed successful. These copies are stored in a single facility in a single region. The replicas reside in separate fault domains and upgrade domains. This means the data is available even if a storage node holding your data fails or is taken offline to be updated.

5. Describe Azure Key Vault.

Azure Key Vault helps safeguard cryptographic keys and secrets used by Azure applications and services. You could store your storage account keys in an Azure Key Vault. What does this do for you? While you can’t control access to the data objects directly using Active Directory, you can control access to an Azure Key Vault using Active Directory. This means you can put your storage account keys in Azure Key Vault and then grant access to them for a specific user, group, or application.

6. What is Azure Disk Encryption?

This is another new feature that is currently in preview. This feature allows you to specify that the OS and data disks used by an IaaS VM should be encrypted.

7. What is Client Side Encryption?

We looked at client-side encryption when discussing encryption in transit. The data is encrypted by the application and sent across the wire to be stored in the storage account. When retrieved, the data is decrypted by the application.

8. What are some of the things you can do with AzCopy?

Upload blobs from the local folder on a machine to Azure Blob storage. Upload files from the local folder on a machine to Azure File storage. Copy blobs from one container to another in the same storage account. Copy blobs from one storage account to another, either in the same region or in a different region. Copy files from one file share to another in the same storage account. Copy files from one storage account to another, either in the same region or in a different region. Copy blobs from one storage account to an Azure File share in the same storage account or in a different storage account. Copy files from an Azure File share to a blob container in the same storage account or in a different storage account. Export a table to an output file in JSON or CSV format. You can export this to blob storage.
Import the previously exported table data from a JSON file into a new table. (Note: It won’t import from a CSV file.)

9. Name three options in the settings blade?

Troubleshoot, Audit logs, and new support request.

10. What did you learn from reading this chapter?

I learned about different Azure storage services what they are used for and how they work. 
