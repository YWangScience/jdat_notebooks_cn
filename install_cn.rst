.. _install:

=========================
安装说明
=========================

您可以在此处查看笔记本的渲染版本，
这只需您的网页浏览器，无需其他特殊工具。

要下载并执行笔记本，我们建议您将
`jdat_notebooks <https://github.com/spacetelescope/jdat_notebooks>`_
仓库克隆到您的本地计算机。您也可以点击仓库主页顶部绿色“代码”按钮下的“下载 ZIP”选项来下载整个仓库。您可以单独下载各个笔记本，
但这并不那么直接，也不推荐，因此我们在此不提供详细信息。

此页面是jdat_notebooks的简体中文版本，位于
`jdat_notebooks <https://github.com/YWangScience/jdat_notebooks_cn>`_ 。

大多数笔记本在其文件夹中都有附加的相关文件，
包括列出运行笔记本所需包的需求文档。
这些包可以使用 `pip <https://pip.pypa.io/en/stable/>`_ 安装。版本依赖关系列在每个笔记本文件夹中的 environment.yaml 和 requirements 文件中。您需要 Python 版本 3.9 或更高版本。

创建您的本地环境并克隆仓库
------------------------------------------------

Jdaviz 的某些依赖项需要非 Python 包才能正常工作
（特别是 Jupyter 生态系统的一部分前端栈）。
我们建议使用 `Miniconda <https://docs.conda.io/en/latest/miniconda.html>`_
来轻松管理与 ``jdaviz`` 兼容的 Python 环境；它应该与大多数现代 shell 兼容，除了 CSH/TCSH。

您可能想考虑在新的虚拟环境或 conda 环境中安装您的笔记本，
以避免与您可能已安装的其他包的版本冲突，例如::

    conda create -n jdat-nb python=3.11
    conda activate jdat-nb
    git clone https://github.com/spacetelescope/jdat_notebooks.git

使用 Pip 安装笔记本需求
---------------------------------

接下来，进入您想要安装的笔记本的目录并设置需求::

    cd jdat_notebooks/notebooks/<whatever-notebook>
    pip install -r pre-requirements.txt (如有必要)
    pip install -r requirements.txt
    pip install jupyter
    jupyter notebook
    ## 或者，您可以使用 jupyter lab