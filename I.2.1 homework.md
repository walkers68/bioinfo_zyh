1.
统计文件行数:
```
wc -l test_command.gtf
```  
统计文件字数：
```
wc -c test_command.gtf
```  
2.
```
sort -k 1 test_command.gtf | grep 'YDL248W' | sed -n '1,3 p'
```  
3.
```
sed 's/chr_/chromosome_/g' test_command.gtf | cut -f 1,3,4,5
```  
4.
```
awk '{ temp=$2; $2=$3; $3=temp; print}' test_command.gtf | sort -k 4n -k 5n > result.gtf
```  
5.
```
ls -hl
chmod 774 test_command.gtf
ls -hl
```