# bdp2-2024 - Advanced Containers
This repository contains files used in the course Infrastructures for Big Data Processing (BDP2) at the University of Bologna, Academic Year 2023-2024, taught by prof. Alessandro Costantini (credits Prof. Davide Salomoni).

For details, see the course slides.

For more information on the course, see <a href="https://www.unibo.it/it/studiare/dottorati-master-specializzazioni-e-altra-formazione/insegnamenti/insegnamento/2023/435337">here</a>.

## git commands

Add files to git:
```
git add Dockerfile index.html

```

Check the status with
```
git status

```

Commit:
```
git commit -m "First commit of my web server"

```

Edit your Dockerfile to fix a typo there was in the original Dockerfile and then add and commit the changed file:
```
git commit -a -m "Fix for silly typo"

```

You can now succesfully build and run your web server with 
```
docker build -t web_server .
docker run --rm -d -p 80:80 web_server

```

Changes and reverting to previous versions:
```
# this gives you details about the differences introduced in each commit
git log -p 

# revert to a version of a file (e.g. index.html) specified by a commit hash
git checkout <hash> -- index.html

# revert all files to a given commit (careful!)
git reset --hard <hash>
```
