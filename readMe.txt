项目简介：
这个项目主要是在实现Linux下find命令的模拟。由于里面遍历文件的算法是在基于Linux文件系统的，所以此project只能在Linux下完美运行。

项目实现：
此项目的核心其实就是Linux系统下文件的遍历，因为Linux的文件系统是一个tree，所以正如遍历一个tree一样，我们使用深度遍历和广度遍历都可以，这里我使用的是用递归写的深度遍历。然后看了下效率，也还可以，所以也没有优化。就像Linux下find命令一样可以添加各种参数例如-d -u等等，实现起来也非常简单，其实就是遍历的时候添加一些搜索条件即可。

项目结果：
项目完成了几乎Linux find命令所有的功能。例如 find -print -user -exec -perm -name -prune -group 等等.

项目分析：
Linux 中find命令可以用正则表达式来搜索相关文件例如：
find . -regex ".*\(\.txt\|\.pdf\)$"。   这个功能我当时没有时间完成了，但是我觉得可以构建一个有限自动机来实现这个功能。应该实现起来不是很复杂.
