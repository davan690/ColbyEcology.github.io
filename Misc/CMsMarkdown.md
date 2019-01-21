---
layout: page
title: "Chris' markdown guide"
---
Links: [HEADERS](#HEADERS), [EMPHASIS](#EMPHASIS), [LISTS](#LISTS), [TABLES](#TABLES), [HORIZONTAL RULE](#HORIZONTAL_RULE), [CODE](#CODE), [LINKS](#LINKS), [COMMENTS](#COMMENTS)

<a name="HEADERS"></a>
# HEADERS
**code:**
```
# header 1
## header 2
### header 3
#### header 4
##### header 5
###### header 6
```
**output:**
# header 1
## header 2
### header 3
#### header 4
##### header 5
###### header 6

<a name="EMPHASIS"></a>
# EMPHASIS

**code:**
```
*italic*
**bold**
~~strikethrough~~
```
**output:**

*italic*
**bold**
~~strikethrough~~

<a name="LISTS"></a>
# LISTS
**code:**
```
* bulleted item
- bulleted item
  - sub-bulleted item
+ bulleted item
```
**output:**
* bulleted item
- bulleted item
  - sub-bulleted item
+ bulleted item

**code:**
```
1. numbered item
2. numbered item
3. numbered item 
```
**output:**
1. numbered item
2. numbered item
3. numbered item

<a name="TABLES"></a>
# TABLES
**code:**
```
| column 1 | column 2      | column 3 |
|----------|:-------------:|---------:|
| col1 is  | left-aligned  | 1        |
| col2 is  | centered      | 2        |
| col3 is  | right-aligned | 3        |
```
**output:**

| column 1 | column 2      | column 3 |
|----------|:-------------:|---------:|
| col1 is  | left-aligned  | 1        |
| col2 is  | centered      | 2        |
| col3 is  | right-aligned | 3        |

<a name="HORIZONTAL_RULE"></a>
# HORIZONTAL RULE
**code:**
```
*** or --- or ___
```
**output:**

***

<a name="CODE"></a>
# CODE
Adding a back quote before and after text is an example of how you add **in-line code**: `plot(x = indvar, y = depvar)`.

To create a **block of code** put three back quotes (`) before and after the code:
 ```
indvar <- 1:10
depvar <- indvar^2
plot(x = indvar, y = depvar)
 ```

To create a **block of code with syntax highlighting** put three back quotes (`) and a little r  before and three back quotes after the code:
 ```r
indvar <- 1:10
depvar <- indvar^2
plot(x = indvar, y = depvar)
 ```

<a name="LINKS"></a>
# LINKS

**code:**
```
[Colby's homepage](http://www.colby.edu/)
```
**output:**
[Colby's homepage](http://www.colby.edu/)

**code:**
```
![Colby logo](http://www.colby.edu/communicationsoffice/wp-content/uploads/sites/136/2015/01/Colby_logo_002878.png)
```
**output:**
![Colby logo](http://www.colby.edu/communicationsoffice/wp-content/uploads/sites/136/2015/01/Colby_logo_002878.png)

<a name="COMMENTS"></a>
# COMMENTS
**code:**

```
I like to comment out <!--- words ---> or blocks of text   
<!---  
look at me   
I'm a line of code   
--->
```

**output**

I like to comment out <!--- words ---> or blocks of text
<!---
look at me
I'm a line of code
--->
