I.2.3  
bash脚本
```
#!/bin/bash

#切换到目标目录下
cd $1
#将ls的结果保存到CUR_DIR中
CUR_DIR=`ls`

for val in $CUR_DIR
do
        if [ -f $val ]; then
        #若val是文件则输出文件名并存在filenames.txt
        echo "FILE: $val"
echo $val >> filenames.txt
elif [ -d $val ]; then
        #若val是文件夹则输出文件夹名并存在dirnames.txt
        echo "DIRECTOIN: $val"
        echo $val >> dirnames.txt
fi
done

exit 0
```
filenames.txt
```
a1.txt
a.txt
b1.txt
bam_wig.sh
b.filter_random.pl
c1.txt
chrom.size
c.txt
d1.txt
dir.txt
e1.txt
f1.txt
human_geneExp.txt
if.sh
image
insitiue.txt
mouse_geneExp.txt
name.txt
number.sh
out.bw
random.sh
read.sh
test3.sh
test4.sh
test.sh
test.txt
wigToBigWig
```
dirnames.txt
```
a-docker
app
backup
bin
biosoft
c1-RBPanno
datatable
db
download
e-annotation
exRNA
genome
git
highcharts
home
hub29
ibme
l-lwl
map2
mljs
module
mogproject
node_modules
perl5
postar2
postar_app
postar.docker
RBP_map
rout
script
script_backup
software
tcga
test
tmp
tmp_script
var
x-rbp
```