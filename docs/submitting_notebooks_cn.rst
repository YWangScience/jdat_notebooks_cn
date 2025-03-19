####################
提交笔记本
####################

.. _jdat_notebooks: https://github.com/spacetelescope/jdat_notebooks

本节概述了如何提交笔记本。新的笔记本开发在 `jdat_notebooks`_ 仓库中进行。因此，新的笔记本应通过在 ``STSCI jdat_notebooks`` 仓库中发起拉取请求（PR）进行提交（这是 :ref:`预基线阶段 <draft stage>`）。在 :ref:`审核过程 <review process>` 之后，笔记本将被合并（这是 :ref:`基线阶段 <baseline stage>`）。

**提交内容**：

1. :ref:`数据文件`（上传到 :ref:`Box <Box Submissions>`）。
2. :ref:`Jupyter 笔记本`（上传到 :ref:`GitHub <GitHub Submissions>`）。
3. :ref:`需求文件`（上传到 :ref:`GitHub <GitHub Submissions>`）。

|
检查清单
**********

在提交您的笔记本、需求文件和数据之前和之后，请确保以下项目已准备就绪：

.. code:: text

    - [ ] Box:

        - [ ] 数据已上传到 Box。
        - [ ] 数据通过链接共享。确保设置允许任何拥有链接的人下载。

    - [ ] GitHub:

        - [ ] 笔记本的所有单元输出已清除。
        - [ ] 笔记本使用 `Python 3` 编写。
        - [ ] 所有导入在笔记本的开头进行。
        - [ ] 所有数据通过 Box 的 URL 加载到笔记本中。（不使用本地文件）。
        - [ ] 验证 Python 代码符合 PEP 8。
        - [ ] 删除注释和未使用的代码行。
        - [ ] 包含 `requirements.txt` 文件。

.. tip::

    如果您将此检查清单复制并粘贴到您的 PR 中作为评论或描述，它将呈现为带有可切换单选按钮的检查清单，您可以随时切换。

.. _Box Submissions:

Box 提交
***************

所有数据文件应上传到 STScI 的 Box 文件夹，并通过 URL 共享。所有笔记本在加载/读取数据时应使用人类可读的 URL。有关提交数据文件的说明，请访问 :ref:`上传数据到 Box <Data Files>` 部分。

.. _Github Submissions:

GitHub 提交
******************

:ref:`科学笔记本 <Jupyter Notebooks>` 和 :ref:`需求文件 <Requirements File>` 应通过对 STScI `jdat_notebooks`_ 仓库的 `main` 分支发起拉取请求进行提交。有关如何创建 GitHub 拉取请求的说明，请参见 :ref:`GitHub 指南 <GitHub PR>`。

重要提示::

    新的笔记本应添加到 `jdat_notebooks/notebooks` 目录中。

您必须首先在 `jdat_notebooks/notebooks` 目录中创建一个新文件夹，并将新文件夹命名为与提交的笔记本主题相关的名称（可以将其视为一个简短标题）。例如，`jdat_notebooks/notebooks/spectral_fitting`。这个“标题”也将用于命名 Box 中包含的 :ref:`数据文件 <Data Files>` 的文件夹。在创建新文件夹并命名后，请将所有笔记本和需求文件放入其中。

文件夹名称（“简短标题”）应为：

- 与笔记本主题相关。
- 唯一，以避免与现有笔记本混淆/冲突。
- 长度合理（便于在终端中导航）。
- 全部小写字母。
- 使用下划线代替空格。例如 "spectral fitting" -> "spectral_fitting"

|
审核过程
**************

在创建拉取请求（PR）后，您的 PR 将接受科学和技术审核。自动测试基础设施也将尝试渲染您的笔记本。审核人员将在您的 PR 中留下评论，提出建议的更改或给予批准。如果建议或请求更改，您可以通过 :ref:`更新您的 PR <Updating Your PR>` 中描述的步骤进行更新 :ref:`Git 和 GitHub 工作流程 <GitHub Workflow>` 部分。一旦所有审核人员批准并且自动测试通过，PR 将被合并到官方 STScI 仓库中。