# Nagios Service Expiry Check for OVH, SoYouStart and Kimsufi 

## Content:
1. [Description](#description)
  1. [What it's designed for](#what-its-designed-for)
  2. [The result in Nagios](#the-results-in-nagios)
2. [Installation](#installation)
  1. [Generate API keys](#generate-api-keys)
  2. [Configure Nagios](#configure-nagios)
    * For Domains
    * For dedicated servers

## Description
### What it's designed for
This script is designed to check the expiry date of dedicated servers and domains directly via API. It is especially designed to return the result in a typical nagios format.

You can use it for servers and domains from:
* OVH
* SoYouStart
* Kimsufi

### The results in Nagios
I suggest you to configure the domain check as a host which will look like this:
```
Ok: decstasy.de will expire in 210 days on 2017-03-15.
```
Or as a service check for servers:
```
Ok: ns304258.ip-94-23-210.eu will expire in 19 days on 2016-09-05.
```

## Installation
### Generate API keys
In order to use this script you have to generate 3 keys for the API which are the:
* Application key
* Application secret
* Consumer key (token)

Since we implemented a guide to generate theese keys it's pretty simple. Just follow this steps...
* Place the script in your /usr/local/nagios/libexec/ or /usr/lib64/nagios/plugins/
* Add execution bit to file (chmod +x check_ovh_service_expiry.sh)
* Execute the script with -g parameter and follow instructions

### Configure Nagios
**This will follow shortly...**
