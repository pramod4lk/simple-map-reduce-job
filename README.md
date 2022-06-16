# Notes on MRJob installation
In the next activity, we'll walk you through installing the "mrjob" package for MapReduce on the HDP Sandbox.

Installing mrjob on HDP 2.65
The following video will walk you through these steps, but you may find it helpful to have the commands in writing so you can just copy and paste them as you go (be sure to "su root" first, as shown in the video.)

```sh
yum-config-manager --save --setopt=HDP-SOLR-2.6-100.skip_if_unavailable=true
yum install https://repo.ius.io/ius-release-el7.rpm https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
yum install python-pip
pip install pathlib
pip install mrjob==0.7.4
pip install PyYAML==5.4.1
yum install nano
wget http://media.sundog-soft.com/hadoop/RatingsBreakdown.py
wget http://media.sundog-soft.com/hadoop/ml-100k/u.data
```

# Installing mrjob on HDP 2.5
While going through the next activity, many students are running into an error when entering the command:

```sh
pip install google-api-python-client==1.6.4
```

This seems to arise from a mismatch between python-pip and Python 2.6, but I'm not sure why it only happens for some students and not others. If you do run into this, just update your sandbox to Python 2.7 by entering the following commands:

```sh
yum install scl-utils
yum install centos-release-scl
yum install python27
scl enable python27 bash
```

Now, you should be able to

```sh
pip install google-api-python-client==1.6.4
```

successfully.

If you're still having trouble, please use the Q&A feature for this lecture and we'll help you out.