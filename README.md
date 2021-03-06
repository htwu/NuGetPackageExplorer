![Logo](https://cloud.githubusercontent.com/assets/5808377/11324261/06c2ccd8-912d-11e5-87e4-9898b2217baa.png)

[![Twitter Follow](https://img.shields.io/twitter/follow/NuGetPE.svg?style=social?maxAge=2592000)](https://twitter.com/NuGetPE)

[Latest clickonce release](https://npe.codeplex.com/downloads/get/clickOnce/NuGetPackageExplorer.application) (uninstall first if previous version is 3.9 or lower)

[![Chocolatey](https://img.shields.io/chocolatey/v/NugetPackageExplorer.svg?maxAge=259200)](https://chocolatey.org/packages/NugetPackageExplorer)

[![Join the chat at https://gitter.im/NuGetPackageExplorer/NuGetPackageExplorer](https://badges.gitter.im/NuGetPackageExplorer/NuGetPackageExplorer.svg)](https://gitter.im/NuGetPackageExplorer/NuGetPackageExplorer?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


[![Build status](https://ci.appveyor.com/api/projects/status/nhowjp0e1w0225v7/branch/master?svg=true)](https://ci.appveyor.com/project/NuGetPackageExplorer/nugetpackageexplorer/branch/master)

NuGet Package Explorer is a ClickOnce application that makes it easy to create and explore NuGet packages. After installing it, you can double click on a .nupkg file to view the package content, or you can load packages directly from nuget.org.

To build packages from the command line, use the NuGet command-line tools, which are documented on the [official NuGet site](https://docs.nuget.org/create-packages/creating-a-package).

![image](https://cloud.githubusercontent.com/assets/5808377/13399085/cefc7a10-df01-11e5-88b9-423a90107dce.png)

# Creating a Package

1. Launch Package Explorer and select **File > New** (Ctrl-N), or select **Create a new package** from the **Common tasks** dialog when Package Explorer starts:

	![Package Explorer's common tasks dialog](https://cloud.githubusercontent.com/assets/1339874/19167418/7bca3b18-8bc0-11e6-8ecf-de5b05ed8923.png)

2. Select **Edit > Edit Package Metadata** (Ctrl-K) to open the editor for the underlying .nuspec file. Details for the metadata can be found in the [nuspec reference](https://docs.nuget.org/ndocs/schema/nuspec).

	![Editing package metadata with the Package Explorer](https://cloud.githubusercontent.com/assets/1339874/19167426/8399b85a-8bc0-11e6-8516-6f0b53ddc595.png)

3. Open the files you want to include in the package in Windows explorer, then drag them into the **Package contents** pane of Package Explorer. Package Explorer will attempt to infer where the content belongs and prompt you to place it in the correct directory within the package. (You can also explicitly add specific folders using the **Content** menu.)

	For example, if you drag an assembly into the Package contents window, it will prompt you to place the assembly in the **lib** folder:

	![Package Explorer infers content location and prompts for confirmations](https://cloud.githubusercontent.com/assets/1339874/19167427/88c80fc0-8bc0-11e6-8d39-cc6e04024013.png)

	![The package's lib folder with added content](https://cloud.githubusercontent.com/assets/1339874/19167432/8e675a3a-8bc0-11e6-9848-0dd8cf73b4f9.png)


4. Save your package with **File > Save** (Ctrl-S).

# Publishing a Package

1.Create a free account on [nuget.org](http://nuget.org/), or log in if you already have one. When creating a new account, you'll receive a confirmation email. You must confirm the account before you can upload a package.

2.Once logged in, click your user name (on the upper right) to navigate to your account settings.

3.Under **API Key**, click **copy to clipboard** to retrieve the access key you'll need in the next step:

    ![Copying the API key from the nuget.org profile](https://cloud.githubusercontent.com/assets/1339874/19167409/6fd8d238-8bc0-11e6-86b4-49af64483d78.png)

4. Assuming your package is loaded in Package Explorer, select **File > Publish** (Ctrl+P) to bring up the **Publish Package** dialog:

	![Publish Package Dialog](https://cloud.githubusercontent.com/assets/1339874/19167436/90ebbbc0-8bc0-11e6-8cb1-68717ec811e7.png)

5. Paste your API key intp **Publish key** and click **Publish** to push the package to nuget.org.

6. In your profile on nuget.org, click **Manage my packages** to see the one that you just published; you'll also receive a confirmation email. Note that it might take a while for your package to be indexed and appear in search results, during which time you'll see a message that the package hasn't yet been indexed.

