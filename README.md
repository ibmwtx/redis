
# Redis Adapter overview

The Redis Adapter allows you to read / write and listen to Redis in-memory data structure store. 


## Minimum Requirements : 

ITX v9.0.0.x

## Command Alias : 

Adapter commands can be specified by using a command string on the command line or creating a command file that contains adapter commands. The execution command syntax is:

-IM[alias] card_num <br>
-OM[alias] card_num


where -IM is the Input Source Override execution command and -OM is the Output Target Override execution command, alias is the adapter alias, and card_num is the number of the input or output card. The following table shows the adapter alias and its execution command.


Adapter 	:  RDS <br>
Alias 	        :  RDSL <br>
As Input        :  -**IMRDS**card_num <br>
As Output       :  -**OMRDS**card_num <br>    	  


## Redis Adapter commands

The following table lists valid commands for the EXCEL Adapter, the command syntax, and whether the command is supported (✓) for use with data sources, targets, or both.

Hostname (-H)     : Host name of the service

Port (-P)	  : Port number of the service

Channel (-C )  : Channel name

Key (-K) : Key name

Password (-PASS) : password of the service

## Redis Adapter Command Line Examples
###Inbound Adapter : 

Command Line : -H localhost -P 6379 -C mychannel -PASS password or -H localhost -P 6379 -K mykey -PASS password

###Outbound Adapter : 

Command Line : -H localhost -P 6379 -C mychannel -PASS password or -H localhost -P 6379 -K mykey -PASS password


Listener : Supported 

## REDIS Adapter Installation Instructions 

a) Create a directory com.ibm.itx.dtx.m4redis under ITX Install / jars 

b) Drop m4redis.jar in to directory

c) Edit adapters.xml and add the following line 

M4Adapter name="Redis" alias="RDS" id="177" type="app" class="com/ibm/itx/dtx/m4redis"


d) Download Redis artifacts from [Redis](http://redis.io/download). Copy jedis.jar, commons-pool2-xx.jar to "WTX INSTALL DIR/jars/com.ibm.itx.dtx.m4redis" directory


####Note : For any defects or usage concerns, please open an issue ticket and shall be addressed. 
