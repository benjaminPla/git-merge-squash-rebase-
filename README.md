#GIT [merge, --squash, rebase] basics

##Diagram
```
git init
touch master.txt

echo m1 >> master.txt
git add master.txt
git commit -m 'm1'

echo m2 >> master.txt
git commit -am 'm2'

git checkout -b feature
touch feature.txt

echo f1 >> feature.txt
git add feature.txt
git commit -m 'f1'

echo f2 >> feature.txt
git commit -am 'f2'

git checkout master

echo m3 >> master.txt
git commit -am 'm3'
```

##merge
Standing on 'master' branch
```
git merge feature
```
![merge](https://user-images.githubusercontent.com/85419447/192778815-cd30d299-ea37-4d21-b3a1-4ba7d46b176d.png)

##--squash
Standing on 'master' branch
```
git merge --squash feature
git commit -m "Merge --squash branch 'feature'"
```
![merge--squash](https://user-images.githubusercontent.com/85419447/192778799-d04ca5af-395f-415c-a574-48df21a84d51.png)

##rebase
Standing on 'feature' branch
```
git rebase master
git checkout master
git rebase feature
```
![rebase](https://user-images.githubusercontent.com/85419447/192778757-afc2950d-92fc-47f3-bdee-b7d2c435839e.png)
