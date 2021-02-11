#  Question

Write a bash script for following requirement as a test task
Write a script that will display<br />
1-Disk Space<br />
2-Top 10 Process names consuming high cpu with % consumption after name<br />
3-Top 10 Process names consuming high memory with % consumption after name<br />
The script should be configured in a way that user should be able to provide what is needs either 1,2,3 or all

---
###  Answer:

Used `$1` is the first command-line argument passed to the shell script. Also, know as Positional parameters<br /><br />



`ps -eo comm,%cpu --sort=-%cpu | head -n 11`  script to get output for Top 10 CPU consuming processes names<br /><br />
 `ps -eo comm,%mem --sort=-%mem | head -n 11`  script to get output for Top 10 MEMORY consuming processes names<br /><br />
 `pr -fm  <(ps -eo comm,%cpu --sort=-%cpu | head -n 11) <(ps -eo comm,%mem --sort=-%mem | head -n 11) && df -h` script to print both Top 10 MEMORY and CPU consuming processes names.

<br />

_**Execution**_<br/>

Save this bash file (e.g home\ismaeel\assignment\bashing.sh) on your machine and go to that directory <br/> run it by just just typing that command<br/>
 `./bashing.sh 1  ` to Dispaly Disk Space<br/>
 `./bashing.sh 2  ` to Dispaly Top 10 Process names consuming high cpu with % consumption after name<br/>
 `./bashing.sh 3  ` to Dispaly Top 10 Process names consuming high memory with % consumption after name<br/>
 `./bashing.sh all  ` to Dispaly Top 10 Process names consuming high memory and high cpu with % consumption after name and Disk space<br/>




---