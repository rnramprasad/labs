## Splunk Enterprise Server installation 

#### Cent OS
```
cd /tmp ; wget -O splunk-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz "https://download.splunk.com/products/splunk/releases/9.0.3/linux/splunk-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz"
```
```
tar -xzf splunk-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz -C /opt
/opt/splunk/bin/splunk start --accept-license  ( enter username & password )
```
#### Ubuntu
```
cd /tmp ; wget -O splunk-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz "https://download.splunk.com/products/splunk/releases/9.0.3/linux/splunk-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz"
```
```
tar -xzf splunk-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz -C /opt
/opt/splunk/bin/splunk start --accept-license  ( enter username & password )
```

## Splunk Forwarder Installation    

#### Cent OS
```
cd /tmp ; wget -O splunkforwarder-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz "https://download.splunk.com/products/universalforwarder/releases/9.0.3/linux/splunkforwarder-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz"
```
```
tar -xzf splunkforwarder-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz -C /opt
/opt/splunkforwarder/bin/splunk start --accept-license ( enter username & password )
```

#### Ubuntu
````
cd /tmp ; wget -O splunkforwarder-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz "https://download.splunk.com/products/universalforwarder/releases/9.0.3/linux/splunkforwarder-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz"
```
```
tar -xzf splunkforwarder-9.0.3-dd0128b1f8cd-Linux-x86_64.tgz -C /opt
/opt/splunkforwarder/bin/splunk start --accept-license ( enter username & password )
```

```
cofigure mail server

	settings ==> Server settings ==> Email Setting 
	Mail host: smtp.gmail.com
	Email security: Enable SSL
	Username: your gmail 
	Password: your gmail passwd

	Save

============================================================================================================
Create Alert

serach for data 
	index="apachelogs" sourcetype="nginx" 404 ==> Save As ==> Alert ( under setting )
	Title: 404-Alert
	Permission: Shared in App
	Alert type: Scheduled/Real Time
	Trigger Conditions: choose accordinlgy
	Throttle: choose if required ( after an alert is triggered, subsequent alerts will not be triggered until after the throttle period )
	Trigger Actions: send Email
```
