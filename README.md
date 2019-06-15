1. 如何删除一个git push不需要的文件

首先需要将本地的代码进行回退

git reset

其中有2种命令：
git reset --hard
git reset --soft

其中--hard直接该本本地源码，不仅指向变化而且代码也回到原来的形似。 
当使用--soft的时候，知识改变HEAD的指向，本地代码不会发生变化

git reset --soft xxx版本号

也可以使用

git reset --soft HEAD~1 (~1回退一个版本)

然后直接修改代码，然后commit或者取消git add命令

git rm --cached xxx文件名xxx

例如我们push提交了Test.java文件，如何操作呢？

git reset --soft HEAD~1
git rm cached Test
