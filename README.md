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

##--squash
Standing on 'master' branch
```
git merge --squash feature
git commit -m "Merge --squash branch 'feature'"
```

##rebase
Standing on 'feature' branch
```
git rebase master
git checkout master
git rebase feature
```
