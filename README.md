# Lattice bosh release

A bosh release for a scalable, highly available lattice deployment. This bosh release, combined with the Diego bosh release, can deploy a complete lattice cluster.

The example manifest is for an AWS deploy, standard VPC with private and public network with a working BOSH installed.

This README assumes you're already pretty comfortable with BOSH and have done a bunch
of deployments already!

Getting this up and running on AWS generally involve the following steps;

1. Create a VPC with a private and public subnet

2. [Install microbosh](https://github.com/cloudfoundry/bosh-init)

3. Upload a stemcell

4. Upload this release and the latest diego releases

5. Tailor the manifest and deploy

6. Create two ELBs, one connected to one or more routers for HTTP traffic and
the other for ssh connections to containers, this one should be connected to the
SSH proxy instance.
