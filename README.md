

What is a 3-Tier Architecture?

A 3-tier architecture is a type of software architecture which is composed of three “tiers” or “layers” of logical computing. 
They are often used in applications as a specific type of client-server system. 3-tier architectures provide many benefits for production and development environments by modularizing the user interface, business logic, and data storage layers.
Doing so gives greater flexibility to development teams by allowing them to update a specific part of an application independently of the other parts.


![image](https://user-images.githubusercontent.com/51155706/131279493-08c5ba67-7f6d-4242-9f44-b9a3bc65347d.png)


    Presentation Tier-
    
    The presentation tier is the front end layer in the 3-tier system and consists of the user interface. 
    This user interface is often a graphical one accessible through a web browser or web-based application and which displays content and information useful to an end user. 
    
    Application Tier- 
    
    The application tier contains the functional business logic which drives an application’s core capabilities. 
    It’s often written in Java, .NET, C#, Python, C++, etc.
    
    Data Tier- 
    
    The data tier comprises of the database/data storage system and data access layer. 
    Examples of such systems are MySQL, Oracle, PostgreSQL, Microsoft SQL Server, MongoDB, etc. Data is accessed by the application layer via API calls.
    
 
 
----------------------------------------------------------------------------------------------------------------------------------------------------------

Azure Instance Metadata Service

The Azure Instance Metadata Service (IMDS) provides information about currently running virtual machine instances. 
You can use it to manage and configure your virtual machines. This information includes the SKU, storage, network configurations, and upcoming maintenance events.

Here's sample code to retrieve all metadata for an instance. To access a specific data source, see Endpoint Categories for an overview of all available features.

Invoke-RestMethod -Headers @{"Metadata"="true"} -Method GET -NoProxy -Uri "http://IP/metadata/instance?api-version=2021-02-01" | ConvertTo-Json -Depth 64
