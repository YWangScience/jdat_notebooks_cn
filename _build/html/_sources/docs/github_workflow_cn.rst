.. _GitHub Workflow:

#######################
Git 和 GitHub 工作流程
#######################

本节概述了 Git 和 GitHub 的工作流程。
每次更新您的笔记本时，请按照以下说明“保存”您的更改。
下面子节中概述的工作流程可以用以下命令集进行总结：

.. code:: bash

    # 进入目录
    cd notebooks<name_of_your_folder>

    # 检查状态
    git status

    # 添加文件到提交
    # 对于每个文件，运行：
    git add <file_name>

    # 再次检查状态（已添加的文件应为绿色）
    git status

    # 带注释提交
    git commit -m "对更改的简短描述"

    # 准备上传时，推送到您的分叉
    git push <your_github_username> <branch_name>


**步骤 1：本地准备文件**

下一步是创建或更新您的文件到本地仓库，然后再上传到 GitHub。
如上所述 `above <GitHub Submissions>`_，在 `notebooks` 目录中创建一个以项目名称命名的新文件夹。将您的 :ref:`科学笔记本 <Jupyter Notebooks>` 和 :ref:`需求文件 <Requirements File>` 添加到新文件夹中。在继续之前，请确保 :ref:`清除单元输出 <Clearing Notebook Outputs>`。

.. note::

    请记得清除您笔记本中的所有单元输出。
    有关说明，请参见 :ref:`Clearing Notebook Outputs`。

**步骤 2：添加**

使用终端，您必须首先 ``cd`` 进入您创建的文件夹：

.. code:: bash

    cd jdat_notebooks/notebooks/<name_of_your_folder>

检查状态：第一步是检查有哪些更改可以添加并提交到仓库历史中。
要获取更改及其状态的列表，请运行：

.. code:: bash

    git status

这将返回已添加到本地仓库的文件列表。未暂存以提交的文件将以红色突出显示。已暂存以提交的文件将以绿色列出。要选择要暂存以提交的文件，您必须首先“添加”它们。可以将“添加”视为选择您希望包含在提交中的文件。

添加要上传的文件：要将文件添加到提交中，请对每个文件运行以下命令：

.. code:: bash

    git add <file_name>

再次检查状态：添加文件后，您应该再检查一次您打算提交的文件是否已暂存。为此，请运行：

.. code:: bash

    git status

这次，您选择的文件应在 `Changes to be committed` 下以绿色字体显示。

**步骤 3：提交**

现在您可以将文件提交到本地 git 历史中。当您提交更改时，您应该留下简短的注释，描述在提交中引入的更改。要添加注释，您可以在提交命令的末尾附加 ``-m "comments"``。要带注释提交更改，请运行以下命令：

.. code:: bash

    git commit -m "对更改的简短描述"


**步骤 4：推送**

现在您可以将更改推送（上传）到您的 GitHub 分叉。为此，请运行以下命令：

.. code:: bash

    git push <your_github_username> <branch_name>

.. tip::

    如果您不确定自己正在使用哪个分支，请运行 ``git branch``

系统会提示您输入 GitHub 用户名和密码。输入凭据后，您的更改将上传到您的 GitHub 分叉（在线副本）。