# Nagios configuration scripts for version 4.4.3
# with sample NRPE scripts

This project is to establish a set of example configuration for default Nagios installation on Centos Linux. It is not meant for a final production, but more leaarning and understanding how to set up monitoring of remote host and grouping the host machines. 

Scripts were configure for Centos Linux 7 in a LAN environment. The sample server are listed here
<ol>
<li>10.1.1.100 the nagios server where this script goes.
<li>10.1.1.101 the development server called tboxmy
<li>10.1.1.102 the server called cmg.com.my
<li>10.1.1.103 the server called eclaim
</ol>

The servers are group into Production and Linux Servers (non production). Information from monitored servers are via the NRPE installed at each server.



### Prerequisites

On the monitored servers, the Selinux should only be permissive or disabled. Check the status with

```
$ getenforce
```

The Nagios should be installed only on the Nagios server. Monitored servers should be installed with npre only. Installation example

```
sudo yum install nagios nagios-plugins nagios-plugins-all
```

## Running the monitor

Once the scripts are edited on Nagios server based on the environment, the proper setup needs to be done at the monitored servers.

Start nagios monitoring

```
sudo systemctl start nagios
```

Stop nagios monitoring

```
sudo systemctl stop nagios
```

Any errors in the script will prevent nagios from starting.


## Packages 

* [nagios](https://www.nagios.org/projects/nagios-core/) - Nagios server


## Authors

* **Nicholas A S(tboxmy)** - *Initial work* - [tboxmy](https://github.com/tboxmy/nagiosconfig.git)



## License

This project is licensed under the GNU General Public License v3.0


