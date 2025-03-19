.. _GitHub PR:

##########################
创建拉取请求 (PR)
##########################

.. _jdat_notebooks: https://github.com/spacetelescope/jdat_notebooks

**步骤 1: 在 GitHub 上打开 PR 标签**

要创建拉取请求，请导航到 STScI `jdat_notebooks`_ 仓库，并点击 `Pull Request`：

.. image:: images/github_pr_tab.png
    :alt: 显示 GitHub PR 标签的图片
    :scale: 40%
    :align: center

**步骤 2: 点击新建 PR 按钮**

.. figure:: images/github_pr_button.png
    :alt: 显示 GitHub PR 按钮的图片
    :scale: 40%
    :align: center

**步骤 3: 跨分支比较**

.. image:: images/github_compare_across_forks.png
    :alt: 显示 GitHub 上跨分支比较链接的图片
    :scale: 35%
    :align: center

**步骤 4: 选择你的分支和派生库**

使用下拉菜单选择你的派生库和分支。如果找不到你的分支，请先尝试刷新页面。如果仍然找不到你的分支，可能在 :ref:`Git 和 GitHub 工作流程 <git-workflow>` 部分出现了问题。

.. image:: images/github_select_pr_fork_branch.png
    :alt: 显示如何选择和比较分支以创建 PR 的图片
    :scale: 50%
    :align: center

.. note::

    确保 `base repository`（左侧）设置为 `spacetelescope/jdat_notebooks` 和 `main` 分支。

**步骤 5: 编写描述并创建 PR**

一旦 PR 表单弹出，请在标题中填写你的笔记本或项目的名称。在描述框中，留下你的笔记本及其使用的数据的描述。

.. tip::

    如果你复制并粘贴 :ref:`检查列表` 部分中的检查清单，它将呈现为一个带有可切换单选按钮的检查列表，你可以随时切换。

.. image:: images/github_edit_pr.png
    :alt: 显示应包含在 PR 中的项目检查列表的图片
    :scale: 30%
    :align: center

.. _更新你的 PR:

**步骤 6: 更新你的 PR**

一旦 PR 创建完成，你可以通过向 **你的派生库** 推送新更改来更新它。这意味着你可以简单地按照 :ref:`Git 和 GitHub 工作流程` 部分中描述的步骤操作，GitHub 将自动更新你的 PR 以反映这些更改。

.. seealso::

    有关创建拉取请求的更多信息，请访问
    `GitHub PR 文档 <https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request>`_