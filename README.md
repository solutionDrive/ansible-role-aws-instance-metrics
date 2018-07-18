ansible-role-aws-instance-metrics
=================================

This role installs AWS's scripts to report metrics data to CloudWatch.

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/mon-scripts.html


Requirements
------------

None so far.


Role Variables
--------------

    # Set to true to install the prerequisites (perl stuff)
    aws_instance_metrics_install_prerequisites: true
    
    # Set to true to install the scripts
    aws_instance_metrics_install_scripts: true
    
    # Set to true to install the system cronjobs
    aws_instance_metrics_install_cronjobs: true
    
    # Configure the path to install scripts to
    aws_instance_metrics_script_path: "/opt"
    
    # The version of the scripts to install
    aws_instance_metrics_script_version: "1.2.2"
    
    # The source URL the scripts will be loaded from
    aws_instance_metrics_download_url: "https://aws-cloudwatch.s3.amazonaws.com/downloads/CloudWatchMonitoringScripts-{{ aws_instance_metrics_script_version }}.zip"


Dependencies
------------

None so far.


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: solutionDrive.aws-instance-metrics }


License
-------

MIT


Author Information
------------------

Created by solutionDrive GmbH.
https://solutionDrive.de/
