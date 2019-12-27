# Creating-Stage-VM
Creating a stage VM where we can deploy our product for testing

1. Run the given Vagrant file
2. You can see that we have done following task inside the VagrantFile
   * Installed Apache2 for hosting our product
   * Installed gitlab runner to create a runner on this VM which points to our product repository, This mean that if there is any change in the product repo, the pipeline will be run in this VM if we have configured proper tag for this runner.
   * Create a softlink for /home/vagrant/stage/ in /var/www/html/, so that anything we copy to our VM home directory will be hosted by our apache2

## Registering the runner in the VM
Follow tutorial in https://github.com/acapozucca/devops/blob/master/pipeline/s3-automate-deploy/README.md to register a runner for stage-vm.

## Adding stage VM to pipeline
Follow tutorial in https://github.com/venkateshwarant/UAT to create test cases and adding those to pipeline and run those test cases in stage-vm
