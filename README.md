# ansible-splunk-sc4s
Deploy Splunk SC4S (syslog-ng) onto Rocky 8 VMs

Automate this process with a Rocky 8 target platform
https://splunk.github.io/splunk-connect-for-syslog/main/gettingstarted/byoe-rhel8/

Note we are hardcoded to Rocky 8 since https://copr.fedorainfracloud.org/coprs/czanik/syslog-ng336/ is not updated for EPEL 9 yet

Important note for Rocky 8: Python 3.6.8 is the base/system version and cannot be changed
see https://developers.redhat.com/blog/2018/11/14/python-in-rhel-8-3?source=sso#

But Python 3.9 (or higher) is available as "python3.9" or "pip3.9" which we need for SC4S, and we install from EPEL

Usage:
Make sure to use python3.9+ and pip3.9+ in entrypoint.sh as needed
Set your HEC token and URL in env_file