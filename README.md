archiva-puppet-configuration
===========================

#### Requirement

* Ubuntu 14.04 LTS minimal install
* extra packages
```
git puppet
```

#### Puppet install

Prepare Puppet modules:
```
cd /root/puppet/modules
git clone https://github.com/hoccer/puppet-backuppc-client.git backuppc-client
git clone https://github.com/hoccer/puppet-deployment-user.git deployment-user
git clone https://github.com/hoccer/puppet-nrpe.git nrpe
git clone https://github.com/puppetlabs/puppetlabs-stdlib.git stdlib
git clone https://github.com/puppetlabs/puppetlabs-java.git java
git clone https://github.com/maestrodev/puppet-wget.git wget
git clone https://github.com/maestrodev/puppet-archiva.git archiva
```

Apply Puppet configuration:

```
puppet apply init.pp --no-report --modulepath modules --verbose
```
