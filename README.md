EC2 AWS Rundeck Steps.
[Originially by ahonor, forked to akh13/aws-ec2-instances.](https://github.com/rundeck-plugins/aws-ec2-steps)

Simple wrapper around [AWS EC2, ELB, and EBS.](http://docs.aws.amazon.com/cli/latest/reference/ec2/) to expose subcommands as node steps.
Expanded from [ahonor's aws-ec2-scripts](https://github.com/rundeck-plugins/aws-ec2-steps) to include steps for load balancers, EBS, and
other things.

The following steps are available:

* describe-instance-status (http://docs.aws.amazon.com/cli/latest/reference/ec2/describe-instance-status.html)
* start-instances (http://docs.aws.amazon.com/cli/latest/reference/ec2/start-instances.html)
* stop-instances (http://docs.aws.amazon.com/cli/latest/reference/ec2/stop-instances.html)
* copy-ami (http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html)
* create-image/ami (http://docs.aws.amazon.com/cli/latest/reference/ec2/create-image.html)
* wait-on-instances running (http://docs.aws.amazon.com/cli/latest/reference/ec2/wait/index.html)
* wait-on-instances stop (http://docs.aws.amazon.com/cli/latest/reference/ec2/wait/index.html)
* deregister-from-load-balancer (http://docs.aws.amazon.com/cli/latest/reference/elb/deregister-instances-from-load-balancer.html)
* register-with-load-balancer (http://docs.aws.amazon.com/cli/latest/reference/elb/register-instances-with-load-balancer.html)
* reboot-instances (http://docs.aws.amazon.com/cli/latest/reference/ec2/reboot-instances.html)


To build the plugin from source (not needed if you just want to use the plugin):

    zip -r aws-ec2-steps.zip aws-ec2-steps

To install the plugin, copy the zip file into your $RDECK_BASE/libext folder:

    cp aws-ec2-steps.zip $RDECK_BASE/libext
    
There is no need to do anything other than put the zip folder into your libext location. Once this is done,
you should see these steps under your job edit menus.
