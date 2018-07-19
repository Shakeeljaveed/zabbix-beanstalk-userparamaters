# We can monitor beanstalk in zabbix by userdefined items called userparameters
In the beanstalk server:

Run a cronjob for every 2 minutes to collect beanstalk metric parameters as arguments:

#sudo crontab -e

*/2 * * * * sh beanmetric.sh

The shell script contains the script to collect data 

# And add userparameter_beanmetric.conf in the /etc/zabbix/zabbix_agent.conf.d/

And then add the following parameters in zabbix UI:

Go to Zabbix UI > configuration > host > item > create item > key > enter the key
