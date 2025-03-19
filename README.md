[![ci_validation](https://img.shields.io/github/workflow/status/spacetelescope/jdat_notebooks/ci_validation?label=笔记本验证)](https://github.com/spacetelescope/jdat_notebooks/actions?query=workflow%3Aci_validation)
[![ci_deployment](https://img.shields.io/github/workflow/status/spacetelescope/jdat_notebooks/Build%20and%20deploy%20notebooks?label=HTML%20部署&style=flat)](https://github.com/spacetelescope/jdat_notebooks/actions?query=workflow%3ABuild%20and%20deploy%20notebooks)

# James Webb Space Telescope Data Analysis Tool Notebooks 中文版

`jdat_notebooks` 代码库包含用于 JWST（詹姆斯·韦布空间望远镜）数据后管道（post-pipeline）分析的 Jupyter 笔记本。一些笔记本还展示了适用于其他天文台数据的通用分析流程。此代码库及其笔记本是 STScI（太空望远镜科学研究所）[数据分析工具生态系统](https://jwst-docs.stsci.edu/jwst-post-pipeline-data-analysis) 的一部分。

## 概要与描述

请访问[此页面](https://spacetelescope.github.io/jdat_notebooks/)以查看当前可用的内容。

## 安装

如需下载并运行这些笔记本，请阅读[详细安装说明](https://spacetelescope.github.io/jdat_notebooks/install.html)。

## 帮助

如果您发现任何问题或错误，可以[在 GitHub 提交问题报告](https://github.com/spacetelescope/jdat_notebooks/issues/new)。然而，为了更快获得回复，我们建议您提交 JWST 帮助台工单：jwsthelp.stsci.edu。

## 贡献

科学家和开发者社区的贡献均受欢迎。如果您希望修正或澄清现有笔记本的内容，可以直接在此代码库中提交更改。如果您希望贡献新的笔记本或对现有笔记本进行重大修改，请参阅[贡献指南](https://github.com/spacetelescope/jdat_notebooks/blob/main/CONTRIBUTING.rst)，或查看[开发文档](https://spacetelescope.github.io/jdat_notebooks/docs/submitting_notebooks.html)。

这些笔记本利用了 STScI 支持的多个软件包，包括 [Astropy](https://www.astropy.org)、[glue](http://docs.glueviz.org/en/stable/index.html)、[ginga](https://ginga.readthedocs.io/en/latest/)、[photutils](https://photutils.readthedocs.io)、[specutils](https://specutils.readthedocs.io/en/stable/)、[astroimtools](http://astroimtools.readthedocs.io)、[imexam](http://imexam.readthedocs.io)、[jdaviz](https://jdaviz.readthedocs.io/en/latest/)、[asdf](http://asdf.readthedocs.io/en/latest/)、[gwcs](https://gwcs.readthedocs.io/en/latest/)、以及 [synphot](http://synphot.readthedocs.io/en/latest/index.html)。其中，`jdaviz` 是 STScI 开发的 JWST 数据分析可视化工具，专为光谱、IFU 立方体及多目标光谱（MOS）数据设计。