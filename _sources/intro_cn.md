<html>
    <head>
        <title> Spacetelescope jdat_notebooks 索引 </title>
<meta http-equiv="content-type" content="text.html"; charset=utf-8">

<!-- 自定义样式 -->
<link rel="stylesheet" href="main.css">
<link href="https://fonts.googleapis.com/css2?family=Overpass:wght@400;900&display=swap" rel="stylesheet">

<!-- 移动设备配置标签 -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- 内容摘要 -->
<meta name="description" content="天文学笔记本空间" />
<meta name="keywords" content="stsci,spacetelescope,jupyter,notebooks,astronomy" />
<meta name="author" content="Spacetelescope" />

<!-- Google SEO -->
<!-- 详情: https://support.google.com/webmasters/answer/79812?hl=en -->
<meta name="googlebot" content="index" />

<!-- Open Graph -->
<!-- https://ogp.me/ -->
<meta property="og:title" content="Spacetelescope jdat_notebooks 索引" />
<meta property="og:url" content="https://spacetelescope.github.io/jdat_notebooks" />
<meta property="og:description" content="天文学笔记本空间" />
<meta property="og:type" content="website" />
<meta property="og:locale" content="zh" />
<meta property="og:author" content="Spacetelescope" />
    </head>
    <body>
    <section class="notebooks">
 <div id="readme" class="Box-body readme blob js-code-block-container p-5 p-xl-6 gist-border-0">
    <article class="markdown-body entry-content container-lg" itemprop="text"><a name="user-content-james-webb-space-telescope-data-analysis-tool-notebooks"></a>
<h2><a id="user-content-james-webb-space-telescope-data-analysis-tool-notebooks" class="anchor" aria-hidden="true" href="#james-webb-space-telescope-data-analysis-tool-notebooks"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>詹姆斯·韦伯空间望远镜数据分析工具笔记本</h2>

<p><code>jdat_notebooks</code> 代码库包含了展示JWST数据管线后分析工作流程的笔记本。部分笔记本还展示了适用于其他天文台数据的通用分析工作流程。该代码库和笔记本是STScI更大的<a href="https://jwst-docs.stsci.edu/jwst-post-pipeline-data-analysis" rel="nofollow">数据分析工具生态系统</a>的组成部分之一。</p> 

<p>此页面是<code>jdat_notebooks</code>的<a href="https://github.com/YWangScience/jdat_notebooks_cn">简体中文版本</a>。</p>

<p>下表总结了当前可用的笔记本。大多数链接会带您进入笔记本的渲染版本，只需要网络浏览器即可查看。要下载和执行这些笔记本，请将此<a href="https://github.com/spacetelescope/jdat_notebooks">代码库</a><a href="https://github.com/git-guides/git-clone">克隆</a>到您的本地计算机。大多数笔记本依赖的包可以使用<a href="https://pip.pypa.io/en/stable/" rel="nofollow">pip</a>安装。版本依赖关系列在environment.yaml文件中，以及每个笔记本文件夹中的requirements文件中。</p>

<table>
<thead valign="bottom">
<tr><th colspan="2">JWST科学分析笔记本</th>
</tr>
<tr><th>笔记本</th>
<th>描述</th>
</tr>
<tr><th colspan="2">跨仪器</th>
</tr>
</thead>
<tbody valign="top">

<table>
<thead valign="bottom">
<tr><th colspan="2">JWST科学分析笔记本</th>
</tr>
<tr><th>笔记本</th>
<th>描述</th>
</tr>
<tr><th colspan="2">跨仪器</th>
</tr>
</thead>
<tbody valign="top">
<tr><td>ASDF</td>
<td><ul>
<li>用例：将FITS文件转换为ASDF（高级科学数据格式）文件。</li>
<li>数据：CANDELS项目的COSMOS场图像。</li>
<li>工具：asdf、gwcs、astrocut。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>背景估计</td>
<td><ul>
<li>用例：在复杂场景中估计天空背景。</li>
<li>数据：在笔记本中创建的具有特殊背景模式的图像。</li>
<li>工具：photutils</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>红移互相关</td>
<td><ul>
<li>用例：重现IRAF任务XCORFIT的工作流程来测量红移。</li>
<li>数据：LEGA-C光谱和星系模板光谱；光学静止波段。</li>
<li>工具：specutils。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>查询MAST</td>
<td><ul>
<li>用例：如何使用Python提交NIRSpec MAST查询。</li>
<li>数据：</li>
<li>工具：mast、astroquery。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>Specviz图形界面</td>
<td><ul>
<li>用例：如何在Specviz图形界面中检查和导出光谱。</li>
<li>数据：使用MIRAGE代码生成的NIRISS模拟数据。</li>
<li>工具：specutils、jdaviz。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>IFU立方体拟合</td>
<td><ul>
<li>用例：星系IFU光谱的连续谱和发射线建模。</li>
<li>数据：Messier 58的Spitzer IRS数据。</li>
<li>工具：specutils、自定义函数。</li>
<li>跨仪器：MIRI、NIRSpec。</li>
</ul>
</td>
</tr>
<tr><td colspan="2">NIRCam（近红外相机）</td>
</tr>
<tr><td>多波段扩展孔径测光</td>
<td><ul>
<li>用例：测量视场中的扩展星系测光。</li>
<li>数据：来自JADES GTO河外空白场的模拟NIRCam图像。</li>
<li>工具：photutils。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>密集场孔径测光</td>
<td><ul>
<li>用例：使用孔径拟合测光进行密集场成像。</li>
<li>数据：LMC天体测量定标场的模拟NIRCam图像。</li>
<li>工具：jwst pipeline、photutils。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>PSF测光</td>
<td><ul>
<li>用例：使用PSF拟合测光进行密集场成像。</li>
<li>数据：LMC天体测量定标场的模拟NIRCam图像。</li>
<li>工具：webbpsf、photutils。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td>PSF匹配测光</td>
<td><ul>
<li>用例：使用PSF拟合测光进行密集场成像。</li>
<li>数据：LMC天体测量定标场的模拟NIRCam图像。</li>
<li>工具：webbpsf、photutils。</li>
<li>跨仪器：适用于所有仪器。</li>
</ul>
</td>
</tr>
<tr><td colspan="2">NIRISS（近红外成像和无缝光谱仪）</td>
</tr>
<tr><td>WFSS光谱
笔记本0
笔记本1
笔记本2
笔记本3</td>
<td><ul>
<li>用例：光栅光谱的最优提取和分析。</li>
<li>数据：星系团的模拟NIRISS光谱</li>
<li>工具：specutils。</li>
<li>跨仪器：NIRSpec。</li>
</ul>
</td>
</tr>
<tr><td>MOS光谱</td>
<td><ul>
<li>用例：一维光谱的发射线测量和模板匹配。</li>
<li>数据：LEGA-C光谱和星系模板光谱；光学静止波段。</li>
<li>工具：specutils。</li>
<li>跨仪器：NIRSpec。</li>
</ul>
</td>
</tr>
<tr><td>SOSS凌星系外行星</td>
<td><ul>
<li>用例：系外行星主凌星。</li>
<li>数据：使用awesomesoss的模拟凌星。</li>
<li>工具：jwst pipeline、juliet。</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td>AMI
双星系统</td>
<td><ul>
<li>用例：寻找AB Dor的双星参数。</li>
<li>数据：双点源的MIRAGE模拟数据。</li>
<li>工具：jwst pipeline、nrm_analysis。</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td colspan="2">NIRSpec（近红外光谱仪）</td>
</tr>
<tr><td>IFU分析</td>
<td><ul>
<li>用例：AGN的连续谱和发射线建模；1.47-1.87μm。</li>
<li>数据：双子座天文台NIFS；NGC 4151。</li>
<li>工具：specutils、cubeviz。</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td>MOS最优提取</td>
<td><ul>
<li>用例：最优光谱提取。</li>
<li>数据：模拟NIRSpec MOS数据；点源。</li>
<li>工具：jwst pipeline</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td>MOS预成像</td>
<td><ul>
<li>用例：NIRSpec的NIRCam预成像模拟。</li>
<li>数据：LMC天体测量定标场的模拟NIRCam图像。</li>
<li>工具：jwst pipeline。</li>
<li>跨仪器：NIRCam。</li>
</ul>
</td>
</tr>
<tr><td>BOTS凌星系外行星</td>
<td><ul>
<li>用例：系外行星主凌星。</li>
<li>数据：来自地基观测的模拟NIRSpec数据。</li>
<li>工具：</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td>IFU最优提取</td>
<td><ul>
<li>用例：最优光谱提取。</li>
<li>数据：暗弱（类星体）点源的模拟数据。</li>
<li>工具：jwst、scipy、specutils、jdaviz、photutils、astropy.io、astropy.wcs</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td colspan="2">MIRI（中红外仪器）</td>
</tr>
<tr><td>LRS最优提取</td>
<td><ul>
<li>用例：最优光谱提取。</li>
<li>数据：MIRISim模拟光谱。</li>
<li>工具：jwst pipeline、gwcs。</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td>IFU立方体1</td>
<td><ul>
<li>用例：从IFU立方体提取空间-光谱特征。</li>
<li>数据：LMC中点源的KMOS数据立方体。</li>
<li>工具：specutils、spectral_cube、photutils。</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
<tr><td>IFU立方体2</td>
<td><ul>
<li>用例：使用photutils自动检测点源并提取测光</li>
<li>数据：ALMA 13CO数据立方体。</li>
<li>工具：specutils、spectral_cube、photutils。</li>
<li>跨仪器：</li>
</ul>
</td>
</tr>
</tbody>
</table>

<a name="user-content-help"></a>
<h2><a id="user-content-help" class="anchor" aria-hidden="true" href="#help"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>帮助</h2>

<p>如果您发现任何问题或错误，可以开启GitHub工单。但为了获得更快的响应，我们建议您提交JWST帮助台工单：jwsthelp.stsci.edu</p>

<a name="user-content-contributing"></a>
<h2><a id="user-content-contributing" class="anchor" aria-hidden="true" href="#contributing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>贡献</h2>

<p>我们欢迎来自科学家和开发者社区的贡献。如果您希望对现有笔记本进行修复或说明，请直接在此代码库中进行。如果您希望贡献新的笔记本或对现有笔记本进行重大改写，我们建议您访问<a href="https://github.com/spacetelescope/jdat_notebooks">jdat_notebooks</a>。有关如何提供此类贡献的详细信息，请参阅<a href="https://github.com/spacetelescope/jdat_notebooks/blob/main/CONTRIBUTING.rst">贡献说明</a>。</p>

<p>这些笔记本尝试使用STScI支持的多个软件包，包括<a href="https://www.astropy.org" rel="nofollow">Astropy</a>、<a href="http://docs.glueviz.org/en/stable/index.html" rel="nofollow">glue</a>、<a href="https://ginga.readthedocs.io/en/latest/" rel="nofollow">ginga</a>、<a href="https://photutils.readthedocs.io" rel="nofollow">photutils</a>、<a href="https://specutils.readthedocs.io/en/stable/" rel="nofollow">specutils</a>、<a href="http://astroimtools.readthedocs.io" rel="nofollow">astroimtools</a>、<a href="http://imexam.readthedocs.io" rel="nofollow">imexam</a>、<a href="https://jdaviz.readthedocs.io/en/latest/" rel="nofollow">jdaviz</a>、<a href="http://asdf.readthedocs.io/en/latest/" rel="nofollow">asdf</a>、<a href="https://gwcs.readthedocs.io/en/latest/" rel="nofollow">gwcs</a>和<a href="http://synphot.readthedocs.io/en/latest/index.html" rel="nofollow">synphot</a>。请注意，jdaviz是STScI的JWST数据分析可视化工具，设计用于处理光谱、IFU立方体和多目标光谱(MOS)。</p>
  </body>
</html>