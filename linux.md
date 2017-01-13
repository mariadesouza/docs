#LINUX - RHEL/CENTOS

## Cheat Sheet

* Getting Linux version
> cat /proc/version
> cat /etc/*-release
> cat /etc/redhat-release 

* find out if 32-bit or 64-bit
> uname -a
>>Linux maria.incentivenetworks.internal 2.6.18-194.32.1.el5 #1 SMP Wed Jan 5 17:52:25 EST 2011 x86_64 x86_64 x86_64 GNU/Linux
>>x86_64 => 64-bit
>>i686 => 32-bit.

* Change date
> date +%Y-%m-%d%H:%M:%S -s “2014-02-1018:35:26”

* sync up time with ntp on amazon ec2
> sudo ntpdate -b 0.amazon.pool.ntp.org

* Find perl modules installed
> perl -MExtUtils::Installed -MData::Dumper -e  'my ($inst) = ExtUtils::Installed->new(); print Dumper($inst->modules());' |cut -d\  -f3- |tr ';' '\\' > deps.txt

* Check for listening Ports
> netstat -anp | egrep -i 'httpd|apache'

* Change user group
> usermod -a -G wheel lvuser

* allow the group wheel to use sudo commands.
The sudo configuration file is /etc/sudoers. We should never edit this file manually. Instead, use the visudo command:  # visudo

* Replace a String With Another String In All Files Using sed
> sed -i 's/10.11.50.212/*/g’ *.conf
