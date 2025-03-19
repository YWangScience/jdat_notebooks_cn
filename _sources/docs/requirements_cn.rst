.. _Requirements File:

#################
需求文件
#################

一个 pip 需求文件是一个文本文件，命名为 `requirements.txt`，其中包含运行科学笔记本所需的 Python 包列表。当用户下载科学笔记本时，他们需要这个需求文件来安装必要的 Python 包。因此，笔记本负责人需要提供一个需求文件，作为他们笔记本的补充。

**列出包：** 每个 Python 包应在需求文件中单独列出一行。您只应列出在笔记本中导入的包（在笔记本中使用的包）。您可以通过查看笔记本中的导入语句来列出包。原生于 Python 的包，例如 ``os`` 或 ``math``，**不应**列在需求文件中。

.. tip::

    您可以通过在终端中运行 ``conda list`` 或 ``pip list`` 来获取包版本的列表。

要指定包的版本，可以使用 ``==`` 运算符（例如 ``astropy==4.1``）。请列出所有需求版本，以匹配您用于开发笔记本的 conda 或 pip 环境。如果您需要添加一个仅在 GitHub 上可用的 Python 包，可以按如下方式列出模块：

.. code:: bash

    # GitHub 上的包：
    git+https://github.com/name_of_repo

    # 如果需要指定一个分支：
    git+https://github.com/name_of_repo#branch_name


**示例：** 这是一个示例需求文件 (`requirements.txt`)：

.. code-block:: text

    numpy==1.19.1
    jupyter==1.0.0
    aplpy==2.0.3
    astrodendro==0.2.0
    astropy==4.0.1.post1
    matplotlib==3.3.1
    photutils==0.7.2
    scipy==1.5.0
    specutils==1.0
    git+https://github.com/spacetelescope/jwst#0.16.2

.. tip::

    要安装 `requirements.txt` 文件中的包，请使用 ``pip install -r requirements.txt``

.. warning::

    在从需求文件安装一组新包之前，应该考虑创建一个新的 Conda 环境。如果您需要设置 Conda，请参阅 Conda 的
    `入门指南 <https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html>`_ 文档。


有时，开发团队会添加一个额外的需求文件，命名为 `pre-requirements.txt`。此文件用于测试基础设施，应该在 `requirements.txt` 之前安装。笔记本负责人不需要贡献 `pre-requirements.txt` 文件。