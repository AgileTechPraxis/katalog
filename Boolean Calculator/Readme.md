
---
![](../kata.png)

## Boolean Calculator

Implement a Boolean calculator that gets a string in input and evaluates it to the Boolean result.

These are the specifications:

Supports single values:
```
 "TRUE" -> true
 "FALSE" -> false
```

Supports NOT operator:
```
"NOT TRUE" -> false
```

Supports AND operator:
```
"TRUE AND FALSE" -> false
"TRUE AND TRUE" -> true
```

Supports OR operator:
```
"TRUE OR FALSE" -> true
"FALSE OR FALSE" -> false
```

Supports any number of AND and OR giving precedence to NOT then AND and eventually OR operation:
```
"TRUE OR TRUE OR TRUE AND FALSE" -> true
"TRUE OR FALSE AND NOT FALSE" -> true
```

Supports parenthesis:
```
"(TRUE OR TRUE OR TRUE) AND FALSE" -> false
"NOT (TRUE AND TRUE)" -> false
```

#### BONUS:

Prints the Abstract Syntax Tree representing the calculation:
```
"(TRUE OR TRUE OR TRUE) AND FALSE" 

AND
|_ OR
|  |_ TRUE
|  |_ OR
|      |_ TRUE
|      |_ TRUE
|_ FALSE


"TRUE OR TRUE OR TRUE AND FALSE"

OR
|_ TRUE
|_ OR
   |_ TRUE
   |_ AND
      |_ TRUE
      |_ FALSE

        
"NOT ((TRUE OR TRUE) OR (TRUE AND FALSE))"

NOT
|_ OR
   |_ OR
   |  |_ TRUE
   |  |_ TRUE
   |_ AND
      |_ TRUE
      |_ FALSE
        

"TRUE OR TRUE OR NOT TRUE AND FALSE"
```
Which because of precedence is equivalent to :
```
"(TRUE OR (TRUE OR ((NOT TRUE) AND FALSE)))"

OR
|_ TRUE    
|_ OR
   |_ TRUE   
   |_ AND
      |_ NOT
      |  |_ TRUE            
      |_ FALSE
```
