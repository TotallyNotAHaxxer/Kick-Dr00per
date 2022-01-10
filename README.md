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

when you are prompted to this then you will need to input the number in which the paramater is on
