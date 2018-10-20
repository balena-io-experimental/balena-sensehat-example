# Balena Sense
Example of using the Pi, Sense-HAT, InfluxDB and Grafana.

This is an example of a multicontainer application running InfluxDB, Grafana and a third container with Python3 and the Sense-HAT library. 

Push the application to balena and use the public device URL to access Grafana. The default login is admin/admin.

Readings are taken from the humidity, temperature and barometric pressure sensors once every 10 seconds.

![](https://raw.githubusercontent.com/resin-io-playground/balena-sense/master/balena-sense-dashboard.png)
