Apigee OPDK Setup Bootstrap
===========================

This role manages downloading and invoking the bootstrap script from the Apigee servers that will install Apigee 
OPDK service manager.  

Requirements
------------

This role requires that you have an account with Apigee. 
 
The installation of Apigee OPDK requires root access. Credentials must also be supplied to override the empty placeholders
provided here. It is recommended that credentials be consolidated into a single credentials.yml file that can be stored 
separately. It is assumed that files containing credentials are stored in the ~/.apigee folder. 

Role Variables
--------------
Default values for these variables are provided by the role apigee-opdk-setup-default-settings.

URL from which to download the bootstrap scripts

    apigee_repo_url: 'https://{{ apigee_repo_uri }}'

Path to the bootstrap script

    bootstrap_script: 'bootstrap.sh'

Apigee repository user

    apigee_repo_user: ''
    
Apigee repository user password

    apigee_repo_password: ''
    
Apigee repository host that can be used for special releases.
    
    apigee_repo_host: ''
    
Apigee artifact stage
    
    apigee_stage: ''
        

Dependencies
------------

role: apigee-opdk-setup-default-settings

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: apigee-opdk-setup-bootstrap }

License
-------

Apache License Version 2.0, January 2004

Author Information
------------------

Carlos Frias
<!-- BEGIN Google Required Disclaimer -->

# Not Google Product Clause

This is not an officially supported Google product.
<!-- END Google Required Disclaimer -->
<!-- BEGIN Google How To Contribute -->
# How to Contribute

We'd love to accept your patches and contributions to this project. Please review our [guidelines](CONTRIBUTION.md).
<!-- END Google How To Contribute -->