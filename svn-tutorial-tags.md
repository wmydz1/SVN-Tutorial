版本管理系统支持*tag*选项，通过使用*tag*的概念，我们可以给某一个具体版本的代码一个更加有意义的名字。标签允许给某一个具体版本的代码一个描述性强，难忘的名字。举个例子：BASIC_ARRAY_OPERATIONS 就比修改版本 7更有意义。

让我们来看一个 *tag* 标签的例子。Tom为了能更好的审查代码，决定创建一个tag。

<pre>
[tom@CentOS project_repo]$ svn copy --revision=4 trunk/ tags/basic_array_operations
</pre>

上面的命令将会产生出下面的结果。

<pre>
A    tags/basic_array_operations/array.c
Updated to revision 4.
A         tags/basic_array_operations
</pre>


上面的代码成功完成，新的目录将会被创建在 *tags* 目录下。

<pre>
[tom@CentOS project_repo]$ ls -l tags/
total 4
drwxrwxr-x. 3 tom tom 4096 Aug 24 18:18 basic_array_operations
</pre>

Tom想要在提交前双击。状态选项显示 tag 选项成功，所以他可以安全的提交他的更改。

<pre>
[tom@CentOS project_repo]$ svn status
A  +    tags/basic_array_operations

[tom@CentOS project_repo]$ svn commit -m "Created tag for basic array operations"
Adding         tags/basic_array_operations

Committed revision 5.
</pre>
