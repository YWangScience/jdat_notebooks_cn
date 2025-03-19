.. _数据文件:

##########
数据文件
##########

由于我们将与天文学社区共享笔记本，因此在笔记本中分析和可视化的数据需要易于下载。因此，STScI的JDAT团队已设置了一个Box文件夹用于分发数据产品。出于安全原因，我们仅支持托管在STScI的Box文件夹上的数据文件。请遵循以下指南上传和集成您的数据文件。

.. seealso::

    有关STScI数据存储的最新信息，请访问
    `STScI关于笔记本数据存储的指南。 <https://github.com/spacetelescope/style-guides/blob/master/guides/where-to-put-your-data.md>`_.


上传数据到Box
*********************

.. important::

    要提交您的数据文件，您需要一个Box账户。请参见
    `Box支持页面 <https://support.box.com/hc/en-us/articles/360044196373-The-Basics-of-Box>`_ 获取说明。
    一旦您设置好Box账户，请联系JDAT团队以获取对STScI
    `jwst-data_analysis_tools`文件夹的电子邮件邀请。如果您不是STScI的工作人员，请在您的拉取请求中请求访问权限。

.. tip::

    如果您有多个文件，建议在上传到Box之前将它们放入一个`zip`文件中。

**步骤1：创建新文件夹**：一旦您获得对Box上`jwst-data_analysis_tools`文件夹的访问权限，
您可以创建一个与包含您的笔记本和`requirements.txt`的文件夹同名的新文件夹（有关命名约定，请参见 :ref:`GitHub Submissions` 部分）。
创建文件夹后，您可以将数据文件上传到该文件夹中。

.. image:: images/box_new_folder.png
    :scale: 50%
    :align: center

**步骤2：上传数据文件**：要上传文件，请进入您创建的文件夹，并在``上传``菜单下选择``文件``。

.. image:: images/box_upload.png
    :scale: 50%
    :align: center

**步骤3：共享设置**：您上传的文件应该可以公开共享。对于每个您上传的文件，将鼠标悬停在文件名上。选择``共享``按钮以打开共享选项。

.. image:: images/box_share_button.png
    :scale: 50%
    :align: center

一旦共享对话框打开，请确保``共享链接``单选按钮已打开，并且选择了``拥有链接的人``选项。

.. image:: images/box_share_options.png
    :scale: 75%
    :align: center

一旦文件被共享，文件名旁边将出现一个蓝色链接图标。

.. note::

    确保文件夹也被共享，并且选择了``拥有链接的人``选项。您可以通过点击页面右上角的蓝色共享按钮进行检查。您必须在点击按钮之前查看您创建的文件夹。

    .. image:: images/box_share_folder_button.png
        :scale: 50%
        :align: center

**步骤4：更新数据文件**：您可以通过右键单击文件名并点击``上传新版本``来在Box上上传数据的新版本：

.. image:: images/box_update_file.png
    :scale: 50%
    :align: center

笔记本中的Box网址
*********************

.. important::

    STScI Box上的文件分配了一个人类可读的链接，我们请求笔记本负责人在他们的笔记本中使用此URL。

一旦您的文件上传完成，您可以通过URL链接在笔记本中使用它们。
人类可读的URL格式如下::

    https://data.science.stsci.edu/redirect/JWST/jwst-data_analysis_tools/name_of_your_folder/name_of_file.extension

例如，假设您创建了一个名为`example_folder`的文件夹，并添加了一个名为`example.fits`的文件，则URL为::

    # Box上的路径：
    jwst-data_analysis_tools > example_folder > example.fits

    # URL：
    https://data.science.stsci.edu/redirect/JWST/jwst-data_analysis_tools/example_folder/example.fits

现在，您应该能够像在笔记本中使用任何路径一样使用此URL。在上面的示例中，我们可以使用astropy打开fits文件，如下所示：

.. code-block:: Python

    from astropy.io import fits

    data_url = "https://data.science.stsci.edu/redirect/JWST/jwst-data_analysis_tools/example_folder/example.fits"
    hdu_list = fits.open(data_url)

.. note::

    如果您无法使用URL打开文件，请告知团队或在您的笔记本中留下开发者注释。

如果您需要下载文件或有一个`zip`文件，您可以使用以下代码在笔记本中下载文件（并解压缩`zip`文件）：

.. code-block:: Python

    import os

    # 如果示例数据集已经下载，请注释掉这些行：
    import zipfile
    import urllib.request

    boxlink = "https://data.science.stsci.edu/redirect/JWST/jwst-data_analysis_tools/example_folder/example.zip"
    boxfile = './example.zip'  # 指定下载文件的输出路径和文件名

    # 下载文件
    urllib.request.urlretrieve(boxlink, boxfile)

    # 解压缩.zip文件
    zf = zipfile.ZipFile(boxfile, 'r')
    zf.extractall()

此示例将下载并提取数据文件到运行笔记本的同一目录中。
由于您压缩文件的方式决定了解压缩数据的目录结构，请使用您的代码下载文件，并确保笔记本中的路径与解压缩数据的文件结构匹配。