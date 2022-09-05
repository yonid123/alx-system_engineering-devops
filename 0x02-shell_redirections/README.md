[Forwarded from A B]
0-hello_world
#!/bin/bash
echo "Hello, World"

1-confused_smiley
#!/bin/bash
echo -e "\x22\x28\\xc3\x94\x6F\x29\x27"

10-no_more_js
#!/bin/bash
find -name "*.js" -type f -delete

100-empty_casks
#!/bin/bash
find . -empty | rev | cut -d '/' -f 1 | rev

101-gifs
#!/bin/bash
find -name '*.gif' -type f -printf '%f\n' |  LC_ALL=C sort -f | rev | cut -c 5- | rev

102-acrostic
#!/bin/bash
echo $(cut -c 1 | tr -d "\n")

103-the_biggest_fan
#!/bin/bash
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev

11-directories
#!/bin/bash
find . -mindepth 1 -type d | wc -l

12-newest_files
#!/bin/bash
ls -1t | head -10

13-unique
#!/bin/bash
sort | uniq -u

14-findthatword
#!/bin/bash 
grep "root" /etc/passwd

15-countthatword
#!/bin/bash
grep -c "bin" /etc/passwd

16-whatsnext
#!/bin/bash
grep -A 3 "root" /etc/passwd

17-hidethisword
#!/bin/bash
grep -v "bin" /etc/passwd

18-letteronly
#!/bin/bash
grep ^[[:alpha:]] /etc/ssh/sshd_config

19-AZ
#!/bin/bash
tr 'A' 'Z' | tr 'c' 'e'

2-hellofile
#!/bin/bash
cat /etc/passwd

20-hiago
#!/bin/bash
tr -d "Cc"

21-reverse
#!/bin/bash
rev

22-users_and_homes
#!/bin/bash
cut -d: -f 1,6 /etc/passwd | sort

3-twofiles
#!/bin/bash
cat /etc/passwd /etc/hosts

4-lastlines
#!/bin/bash
tail /etc/passwd

5-firstlines
#!/bin/bash
head /etc/passwd

6-third_line
#!/bin/bash
head -3 iacta | tail +3

7-file
#!/bin/bash
echo "Best School" > \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)

8-cwd_state
#!/bin/bash
ls -la > ls_cwd_content

9-duplicate_last_line
#!/bin/bash
tail -1 < iacta >> iacta

script
#!/bin/bash


#Storing the file names in an Array
declare -a filenames=(
0-hello_world
1-confused_smiley
10-no_more_js
11-directories
12-newest_files
13-unique
14-findthatword
15-countthatword
16-whatsnext
17-hidethisword
18-letteronly
19-AZ
2-hellofile
20-hiago
21-reverse
22-users_and_homes
3-twofiles
4-lastlines
5-firstlines
6-third_line
7-file
8-cwd_state
9-duplicate_last_line
100-empty_casks
101-gifs
102-acrostic
103-the_biggest_fan)
