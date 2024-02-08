host name or address, in context of database *is the address to which you want to point to access database*, 
so for example if you want to call database when hosting on your own machine, you need to set up a [[localhost]] (172.0.0.1), 
or if you for example running db in a docker container, then you need to specify an address of a base image, where it running on.

### side note from chat-gpt
**Production:**
- In a production environment, it's common to use a dedicated database server.
- The database server may have a different hostname or IP address that you should specify in your connection string.
- Avoid using "localhost" in production connection strings unless the database server is actually on the same machine as your application, which is uncommon in production setups.
