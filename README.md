# **Fail2Ban Custom Filters**

## **Description**

This repository contains a series of custom filters for Fail2Ban written by me.

These filters are intended to improve the bastioning of our applications using fail2ban.

All these filters are in the filters.d directory.

## **List of actual filters**

Filter  |  Description
--|--
[apache-domain.conf](./filter.d/apache-domain.conf)  |  Detects web requests to undefined hostnames in apache servers.
[apache-web-fuzz.conf](./filter.d/apache-web-fuzz.conf)  |  Detects web requests of inexistent resources in apache servers.
[owncloud-login.conf](./filter.d/owncloud-login.conf)  |  Detects login failures in Owncloud servers.

## **Usage**

First, you need copy the filter file in /etc/fail2ban/filter.d directory.

To apply a filter you need define a jail that use this. You can create a file /etc/fail2ban/jail.d/custom_jails.conf and define your own jails.

You can see a example of custom jails in [custom-jails.conf](./custom-jails.conf) file.


## **Notes**

I will create new filters as I need them in my own services.

If you want me to investigate the creation of a specific filter you can request it through an issue.
