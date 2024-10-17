# Regex-Generator : Readme updated
This project was created as an experiment to see how accurately I can generate valid regex when simply given a string(s) to match. 

# How to use
# Basic Example:
Sample output after tesing the readme changes :

```
# Python 3.11.4 (tags/v3.11.4:d2340ef, Jun  7 2023, 05:45:37) [MSC v.1934 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> from RegexGenerator import RegexGenerator
>>> 
>>> regx = RegexGenerator("Description                         : Abcdefgh AbcDefghi-X Abdc-efgh 000Ab Abcdefgh ABCe Abcdefg")
>>> print(regx).get_regex()   # Issue was here. Fixed the readme after facing this error.
<RegexGenerator.regex_generator.RegexGenerator object at 0x000002024DD1F250>
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'NoneType' object has no attribute 'get_regex'
>>>
>>>
>>> regx
<RegexGenerator.regex_generator.RegexGenerator object at 0x000002024DD1F250>
>>> print(regx.get_regex())   # Correct usage.
\w{11}\s{25}[:]\s{1}\w{8}\s{1}\w{9}[-]\w{1}\s{1}\w{4}[-]\w{4}\s{1}\d{3}\w{2}\s{1}\w{8}\s{1}\w{4}\s{1}\w{7}
```
