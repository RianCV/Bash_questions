# Bash_questions
##1
wget https://gmap.pucrs.br/dalvan/POD-2022/Teams-raw.zip

##2
unzip Teams-raw.zip

##3
shuf -i 0-40000 > numIntAlea.txt
export n_linhas=wc -l Teams-raw.csv
shuf -i 0-40000 -n $n_linhas > numIntAlea.txt

##4
sed -i '' '1s/.*/numIntAlea/' numIntAlea.txt 

##5
ver de novo como eu consegui o numero 48
paste -d ";" <(cut -d ";" -f 48 Teams-raw.csv) numIntAlea.txt > Teams-raw1.5.csv

