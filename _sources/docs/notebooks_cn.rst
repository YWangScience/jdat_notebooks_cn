.. _Jupyter Notebooks:

#################
Jupyter Notebooks
#################

请参见 :ref:`Development Procedure` 部分以获取笔记本开发指南。

.. seealso::

    有关格式化笔记本的详细说明，请访问
    `STScI 笔记本风格指南 <https://github.com/spacetelescope/style-guides/blob/master/guides/jupyter-notebooks.md>`_


安装
************

有关如何安装 Jupyter 笔记本的说明，请访问
`Jupyter 安装页面 <https://jupyter.org/install>`_。


我们还强烈建议使用环境管理工具来跟踪依赖关系并防止冲突。可选工具包括 Python 标准库中的 `venv` 包和 `pip` 工具，或结合 `conda-forge` 包索引的 `Conda <https://docs.conda.io/projects/conda/en/latest/index.html>`_ 工具。如果您需要有关如何设置 Conda 的说明，请参见 Conda 的
`入门指南 <https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html>`_ 文档。

.. important::

    请注意，所有与 JDAT 相关的代码均使用 `Python 3` 编写；不支持 `Python 2`。


启动笔记本
*******************

在您的终端中，``cd`` 到您希望工作的目录并运行 ``jupyter notebook``。
如果没有弹出网页浏览器，请使用终端输出中的 URL 打开 Jupyter 主页。


创建新笔记本
***********************

要创建新笔记本，请导航到您希望工作的目录，并在 `new` 菜单项下选择 `Python 3` 选项：

.. image:: images/notebook_new_notebook.png
    :scale: 60%
    :align: center


Markdown
********

“Markdown” 用于向笔记本添加支持性文献。要将单元格转换为 markdown，使用光标选择它并在单元格类型下拉菜单中选择 markdown。

.. image:: images/notebook_markdown.png
    :scale: 50%
    :align: center

一旦单元格转换为 markdown 单元格，您可以输入文本和方程。如果您有图像链接，可以嵌入它们，并在运行单元格时呈现。
**完成编辑后，请确保运行单元格 (Shift + Enter) 以呈现 markdown**

.. seealso::

    请参见 Adam Pritchard 的 `markdown 备忘单 <https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet>`_
    以获取提示和说明。


开发者笔记
***************

开发者笔记用于为 JDAT 开发者留下笔记或反馈。
开发者笔记应作为笔记本的一部分，并应为单个 `markdown`_ 单元格。该单元格应以文本 ``*Developer Note:*`` 开头。
例如：

.. code-block::

    *Developer Note:*
    创建上面的光谱有点复杂，如果有一个简单的函数可以直接执行 `spec = simulate_jwst_spectrum(a, b)`，将会改善工作流程。

清除笔记本输出
*************************

在打开或更新拉取请求之前，应清除笔记本的所有单元格输出。这是因为完全渲染的笔记本包含图形可能占用大量存储空间。请确保您的结果是可重复的（您不需要输出），因为清除笔记本是不可逆的。要清除笔记本单元格输出，请在 Jupyter 菜单中单击 ``Kernel`` 并选择 ``Restart & Clear Output``。
在笔记本重新启动后，请确保在关闭和提交之前保存笔记本。

.. image:: images/notebook_restart_and_clear_outputs.png
    :scale: 50%
    :align: center

多个笔记本
******************

如果您有多个笔记本需要按特定顺序运行，请根据顺序在每个笔记本标题前添加数字（最多允许 99 个笔记本）。例如::

    jdat_notebooks
    └── notebooks
        └── example_folder
            ├── 01_generate_simulated_data.ipynb
            ├── 02_run_calibration_pipeline.ipynb
            ├── 03_data_analysis.ipynb
            └── requirements.txt

Pep-8 指南
***************

有关更多信息，请参见 STScI 的 `Python 指南 <https://github.com/spacetelescope/style-guides/blob/master/guides/python.md>`_ 和官方 `Pep-8 指南 <https://www.python.org/dev/peps/pep-0008/>`_。


.. seealso::

    - `STScI 笔记本风格指南 <https://github.com/spacetelescope/style-guides/blob/master/guides/jupyter-notebooks.md>`_

    - `STScI Python 风格指南 <https://github.com/spacetelescope/style-guides/blob/master/guides/python.md>`_