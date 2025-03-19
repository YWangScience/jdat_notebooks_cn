=======================================================
JWST 数据分析工具笔记本
=======================================================

`jdat_notebooks 仓库 <https://github.com/spacetelescope/jdat_notebooks>`_ 包含了展示 JWST 数据后处理分析工作流程的笔记本。一些笔记本还展示了适用于其他天文台数据的通用分析工作流程。该仓库及其笔记本是 STScI 更大 `数据分析工具生态系统 <https://jwst-docs.stsci.edu/jwst-post-pipeline-data-analysis>`_ 的一个组成部分。

摘要列表和描述
================================

本页面左侧的侧边栏提供了笔记本的摘要列表，点击后将带您到 HTML 渲染版本的笔记本。这些版本易于阅读，并且只需您的网页浏览器即可，无需特殊工具。笔记本按 JWST 仪器组织，或标记为跨仪器。在每个笔记本的顶部，您将找到该笔记本展示的特定科学用例的简要描述、所使用数据的描述以及通过该用例展示的数据分析工具列表。

安装说明
=========================

要下载和执行笔记本，我们建议您按照 :ref:`安装说明 <install>` 中的描述将 `jdat_notebooks 仓库 <https://github.com/spacetelescope/jdat_notebooks>`_ 克隆到您的本地计算机。

帮助
====

如果您发现任何问题或错误，可以打开一个 `GitHub 问题 <https://github.com/spacetelescope/jdat_notebooks/issues>`_。然而，为了更快的响应，我们鼓励您提交 `JWST 帮助台工单 <https://stsci.service-now.com/jwst>`_。

贡献
============

欢迎科学家和开发者社区的贡献。如果您希望对现有笔记本进行修复或澄清，请随意直接对该仓库进行贡献。如果您希望贡献新的笔记本或对现有笔记本进行重大重构，请参见 `贡献说明 <https://github.com/spacetelescope/jdat_notebooks/blob/main/CONTRIBUTING.rst/>`__。这些笔记本尝试利用 STScI 支持的多个软件包，包括 `Astropy <https://www.astropy.org>`__、`glue <http://docs.glueviz.org/en/stable/index.html>`__、`ginga <https://ginga.readthedocs.io/en/latest/>`__、`photutils <https://photutils.readthedocs.io>`__、`specutils <https://specutils.readthedocs.io/en/stable/>`__、`astroimtools <http://astroimtools.readthedocs.io>`__、`imexam <http://imexam.readthedocs.io>`__、`jdaviz <https://jdaviz.readthedocs.io/en/latest/>`__、`asdf <http://asdf.readthedocs.io/en/latest/>`__、`gwcs <https://gwcs.readthedocs.io/en/latest/>`__ 和 `synphot <http://synphot.readthedocs.io/en/latest/index.html>`__。请注意，jdaviz 是 STScI 的 JWST 数据分析可视化工具，旨在与光谱、IFU 立方体和多目标光谱 (MOS) 一起使用。

.. |image1| image:: data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ib2N0aWNvbiBvY3RpY29uLWxpbmsiIHZpZXdib3g9IjAgMCAxNiAxNiIgdmVyc2lvbj0iMS4xIiB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIGFyaWEtaGlkZGVuPSJ0cnVlIj48cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik03Ljc3NSAzLjI3NWEuNzUuNzUgMCAwMDEuMDYgMS4wNmwxLjI1LTEuMjVhMiAyIDAgMTEyLjgzIDIuODNsLTIuNSAyLjVhMiAyIDAgMDEtMi44MyAwIC43NS43NSAwIDAwLTEuMDYgMS4wNiAzLjUgMy41IDAgMDA0Ljk1IDBsMi41LTIuNWEzLjUgMy41IDAgMDAtNC45NS00Ljk1bC0xLjI1IDEuMjV6bS00LjY5IDkuNjRhMiAyIDAgMDEwLTIuODNsMi41LTIuNWEyIDIgMCAwMTIuODMgMCAuNzUuNzUgMCAwMDEuMDYtMS4wNiAzLjUgMy41IDAgMDAtNC45NSAwbC0yLjUgMi41YTMuNSAzLjUgMCAwMDQuOTUgNC45NWwxLjI1LTEuMjVhLjc1Ljc1IDAgMDAtMS4wNi0xLjA2bC0xLjI1IDEuMjVhMiAyIDAgMDEtMi44MyAweiI+PC9wYXRoPjwvc3ZnPg==
   :class: octicon octicon-link
   :target: #james-webb-space-telescope-data-analysis-tool-notebooks
.. |image2| image:: data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ib2N0aWNvbiBvY3RpY29uLWxpbmsiIHZpZXdib3g9IjAgMCAxNiAxNiIgdmVyc2lvbj0iMS4xIiB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIGFyaWEtaGlkZGVuPSJ0cnVlIj48cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik03Ljc3NSAzLjI3NWEuNzUuNzUgMCAwMDEuMDYgMS4wNmwxLjI1LTEuMjVhMiAyIDAgMTEyLjgzIDIuODNsLTIuNSAyLjVhMiAyIDAgMDEtMi44MyAwIC43NS43NSAwIDAwLTEuMDYgMS4wNiAzLjUgMy41IDAgMDA0Ljk1IDBsMi41LTIuNWEzLjUgMy41IDAgMDAtNC45NS00Ljk1bC0xLjI1IDEuMjV6bS00LjY5IDkuNjRhMiAyIDAgMDEwLTIuODNsMi41LTIuNWEyIDIgMCAwMTIuODMgMCAuNzUuNzUgMCAwMDEuMDYtMS4wNiAzLjUgMy41IDAgMDAtNC45NSAwbC0yLjUgMi41YTMuNSAzLjUgMCAwMDQuOTUgNC45NWwxLjI1LTEuMjVhLjc1Ljc1IDAgMDAtMS4wNi0xLjA2bC0xLjI1IDEuMjVhMiAyIDAgMDEtMi44MyAweiI+PC9wYXRoPjwvc3ZnPg==
   :class: octicon octicon-link
   :target: #help
.. |image3| image:: data:image/svg+xml;base64,PHN2ZyBjbGFzcz0ib2N0aWNvbiBvY3RpY29uLWxpbmsiIHZpZXdib3g9IjAgMCAxNiAxNiIgdmVyc2lvbj0iMS4xIiB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIGFyaWEtaGlkZGVuPSJ0cnVlIj48cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik03Ljc3NSAzLjI3NWEuNzUuNzUgMCAwMDEuMDYgMS4wNmwxLjI1LTEuMjVhMiAyIDAgMTEyLjgzIDIuODNsLTIuNSAyLjVhMiAyIDAgMDEtMi44MyAwIC43NS43NSAwIDAwLTEuMDYgMS4wNiAzLjUgMy41IDAgMDA0Ljk1IDBsMi41LTIuNWEzLjUgMy41IDAgMDAtNC45NS00Ljk1bC0xLjI1IDEuMjV6bS00LjY5IDkuNjRhMiAyIDAgMDEwLTIuODNsMi41LTIuNWEyIDIgMCAwMTIuODMgMCAuNzUuNzUgMCAwMDEuMDYtMS4wNiAzLjUgMy41IDAgMDAtNC45NSAwbC0yLjUgMi41YTMuNSAzLjUgMCAwMDQuOTUgNC45NWwxLjI1LTEuMjVhLjc1Ljc1IDAgMDAtMS4wNi0xLjA2bC0xLjI1IDEuMjVhMiAyIDAgMDEtMi44MyAweiI+PC9wYXRoPjwvc3ZnPg==
   :class: octicon octicon-link
   :target: #contributing