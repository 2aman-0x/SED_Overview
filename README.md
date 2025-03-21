## Sed Overview
suppose I have a file like 'Data' so below all to the questions all are based on 'Data' file  
```cat data```  
```
ID Name salary country
1  kakashi  25000  Japan
2  Hinata 45000  Canada
3  Naruto 55000  Poland
4  Itachi 35000  Japan
```

__1) How to show only a given line or range of lines?__
- ```sed -n '1p' file_name```
- ```sed -n '1,5p' file_name```
- ```sed -n '$p' file_name```

__2) How to see all the users from Japan Country?__
- ```sed -n '/Japan/p' file_name```

__3) How to use multiple expression in sed command?__  
Example: If you wanna only see 2 and 5th line  
- ```sed -n -e '2p' -e '4p' file_name```

__4) How to see all the users from Japan and Canada?__
- ```sed -n -e '/Japan/p' -e '/Canada/p' file_name```

__5) How to see next 4 lines from 2nd line?__
- ```sed -n ‘2,+4p’ file_name```

__6) How to see every 2nd line from first line/Only Even Numbers?__
- ```sed -n ‘1~2p’ file_name```

__7) How to read expression from external file?__
- ```sed -f ex_file file_name```

__8) How to replace a word in a file and show?______
- ```sed 's/<string_to_change>/<new_string>/g' file_name```

__9) How to replace a word in a file and show except a given line or only in given line?__
- ```sed '2 s/<string_to_change>/<new_string>/g' file_name```
- ```sed '2! s/<string_to_change>/<new_string>/g' file_name```

__10) How to replace a word and and edit in your file?__
- ```sed -i '2! s/<string_to_change>/<new_string>/g' file_name```






