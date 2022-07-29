# Azure-SQL-Database


# Azure SQL Database is a PaaS
- Azure manages it and you just have to manage the data


# Create Azure SQL Database




# Download SQL Server Management Studio
- This will allow you to access the SQL database server


# Connect to SQL Server via SQL Management Studio





# Azure SQL Database - Firewall Settings
- Sometimes users can't access the DB server
- Go to Firewalls and virtual networks on the SQL server created when the SQL database is created.
- Add client IP address with the start IP and end IP








# Azure AD Authentication - Azure SQL Databases
- SQL authentication is via user id and password when we created it during the SQL database creation.
- What if instead of creating an user ID one by one, we can use Azure AD identities.



#  Allocating access to Azure AD users to access Azure SQL Database #247
- First step is to enable Azure AD authentication
- Go to Azure AD and create a new user that will act as the db admin
- Go to SQL server > Azure AD > Set admin 
- Now log in to SQL management studio using the admin's email
- As an admin, the SQL db admin can now assign access to the Azure SQL database by running a query to create and assign permissions.



# Azure SQL Database - Transparent Data Encryption
- All of the data in a Azure SQL database is stored in an Azure data center
- Azure SQL provides Transparent Data Encryption - meaning that the data is ENCRYPTED first and then stored in a storage device in a Azure Data Center
- By default, Transparent Data Encryption is enabled for Azure SQL Databases



# Azure SQL Databases - Always Encrypted Feature
- Always Encrypted can be used to encrypt data at rest and in motion
- Can encrypt multiple columns in different tables
- Can encrypt multiple columns located in the same table

# Two types of encryption - Deterministc Encryption(Less secure)
- Here the same encrypted value is generated for any given plain text value. 
- BUT it allows for point lookups, equality joins, grouping and indexing on encrypted columns

# Two types of encryption - Randomized Encryption(Most secure encryption method)
- This prevents the searching, grouping, indexing and joining on encryped columns

# How to enable the Always Encrypted Feature?
- Use SQL Server Management Studio
- 2 keys ALWAYS gets created when the Always Encrypted feature is enabled for a database.
- The Column master key and the column encryption key

# Always Encrypted Lab #248
- We need an Azure Key Vault in order to encrypt
- Go to key vault and ensure that the user has crytographic permissions in Access policies
- Object Explorer > Select table > right click and select encrypt columns 
- Select a column you want to encrypt
- Check in the key vault to see that the master key was encrypted AND if they column select is encrypted
