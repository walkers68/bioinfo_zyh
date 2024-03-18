I.2.2  
第一题：
```
cat 1.gtf | awk '$1=="XI" && $3="CDS"{print}' | sort -k 5 -n | tail
```
第二题：
```
grep -v '^#' 1.gtf | awk '$1=="IV" {print $2, $3}' | sort | uniq -c | sort -nk 1
```
第三题：
```
grep -v '^#' 1.gtf | awk '$1!="IV" && $7=="-" && $3=="CDS"{ print $5-$4 + 1;}' | sort -n | tail -n 2
```
第四题：
```
grep -v '^#' 1.gtf | awk '$1=="XV" && $3=="gene"{split($10,x,";");name=x[1];gsub("\"", "", name);print name, $5-$4+1}'| sort -k 2 -n | tail -n 5
```
第五题：
```
awk '{print NF}' 1.gtf | sort -n | uniq -c
```
