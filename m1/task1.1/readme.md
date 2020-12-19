#  Module 1 DevOps introduction #
## Task 1.1 ##

**Steps:**
1. Seting global config (adding [name and mail](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-34-30.jpg) and seting [text editor](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-34-09.jpg))
```
git config --global user.email "email@gmail.com"
git config --global user.name "Name"
git config --global core.editor "Path"
```
2. Creating repo and cloning to workstation
```
git clone *link*
```
3. Creating readme.txt and making [commit](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-34-23.jpg)
```
> readme.txt 
add .
commit -m "message"
```
4. Creating develop branch and creating index.html [file](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-34-17.jpg)
```
git checkout -b develop
> index.html
```
5. Creating images branch and creating images folder with [images](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-34-14.jpg). also add images into index.html
```
git checkout -b images
mkdir images
```
6. Creating styles [branch](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-34-02.jpg) create styles folder and style.css file. also add styles to index.html)
```
git checkout -b styles
mkdir styles
> style.css
```
7. Merging images branch into develop [branch](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-33-55.jpg)
```
git checkout develop
git merge images
```
8. Merging styles branch into develop branch
```
git merge styles
```
9. Fixing some problem with [merge](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-33-51.jpg) 
10. Merge develop into master [branch](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-33-47.jpg) 
 ```
 git checkout master
 git merge develop
 ```
11. Inspection of [repository](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-33-43.jpg) 
 ```
 git log
 ```
12. Push all changes to [origin](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-33-38.jpg) 
 ```
 git add .
 git commit -m "message"
 git push origin --all
 ```
13. Writing output `git reflog` [command](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m1/task1.1/screenshots/photo_2020-12-10_15-33-32.jpg)
 
## What is DevOps ##

    DevOps is a specialist which combine soft, hard and ops skills. 
