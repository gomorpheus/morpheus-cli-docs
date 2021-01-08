The Morpheus CLI can be used to setup a freshly installed Morpheus Appliance.

First, add your remote appliance with `remote add`

```bash
morpheus remote add demo https://10.0.2.2 --insecure --use
```

The *--insecure* option tells the cli to ignore SSL errors for this remote appliance.

The *--use* option tells the to cli to make this the current remote, so it will be used by default for subsequent commands.


Setup is also done automatically by `remote add`, which checks if the appliance is a fresh install and asks if you want initialize it.

Or you can run `setup` on a fresh appliance manually:

```bash
morpheus setup
```

This will prompt you for all the settings required to initialize the appliance, and then log you as the new master user with the role of System Admin.

```bash
Morpheus Appliance Setup
==================

It looks like you're the first one here.
Let's initialize your remote appliance at https://10.0.2.2

Create Master account
==================

Master Account Name: root

Create Master User
==================

First Name (optional): 
Last Name (optional): 
Username: admin
Email: admin@demomorpheus.com
Password: 
Confirm Password: 

Initial Setup
==================

Appliance Name: demo
Appliance URL [https://10.0.2.2]: 
Enable Backups (yes/no) [no]: 
Enable Monitoring (yes/no) [yes]: 
Enable Logs (yes/no) [yes]: 
Initializing the appliance...

You have successfully setup the appliance.
You are now logged in as the System Admin admin.

Would you like to apply your License Key now? (yes/no) [yes]:    
License Key: <your key>

Do you want to create the first group now? (yes/no) [yes]: 
Name: dev
Code (optional): 
Location (optional): 
Added group dev

Morpheus Groups
==================

   | ID | NAME | LOCATION | CLOUDS | HOSTS
---|----|------|----------|--------|------
=> | 1  | dev   |          | 0      | 0    

Viewing 1-1 of 1

# => Currently using g1

Do you want to create the first cloud now? (yes/no) [yes]: 
Cloud Type ['?' for options]: Morpheus
Name: c1
Code (optional): 
Location (optional): 
Visibility (optional) [private] ['?' for options]: 


Cloud Details
==================

ID: 1
Name: c1
Type: Morpheus
Code: standard
Location: 
Visibility: Private
Groups: g1
Status: OK

Cloud Servers (0)
==================

 Container Hosts: 0    Hypervisors: 0      Bare Metal: 0    Virtual Machines: 0     Unmanaged: 0    

```

Your appliance setup is now complete and you have created your first Group and Cloud.

The setup command can only be completed once, attempting to run it again will result in an error:

```bash
morpheus remote setup
Appliance has already been setup
```
