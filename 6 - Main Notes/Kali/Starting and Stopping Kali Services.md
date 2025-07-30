2025-07-09 15:00

Status: **Complete**

Tags: 
[[Kali Linux]]
[[Basics]]
[[Commands]]
[[Service cmd]]
## Starting and Stopping Kali Services

`services`
	 Allows to start and stop services
		 `sudo service apache2 start`
		 `sudo service apache2 status`
		 This will start your apache2, to verify copy your ip address or use localhost on the browser
		 `http://localhost OR http://10.0.2.15:80`
		 You can also check the status of the service you want by
		 `service service_name status`
		 

`systemctl`
	Allows enable or disable services to start on boot
	`systemctl enable/disable service`
	this will start on boot
	one good thing to start on boot is postgresql
	`systemctl enable postgresql` this will create a server for metasploit to work which is very important when pen testing

*Commands to note*
	`python -m module_name` Is like running a .py file but instead we use a built in tools inside the terminal. 
	Sample here in [[Second Application]]
### Reference
