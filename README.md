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
- 

