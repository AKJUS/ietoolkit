**ietoolkit - Stata toolkit for analysis**
=====

### **Content**
**ietoolkit** provides a set of commands that address different aspects of data management and data analysis. Many of the commands are initially conceived in the context of primary data and impact evaluations, but implemented to be general and applicable to many other fields. Some of the commands are related to standardized best practices developed at DIME (The World Bank’s department for Impact Evaluations). For these commands, the corresponding help files provide justifications for the standardized best practices applied.


| Command | Description |
| --- | --- |
| [iebaltab](https://worldbank.github.io/ietoolkit/reference/iebaltab.html) | Produces balance tables with multiple groups or treatment arms |
| [ieboilstart](https://worldbank.github.io/ietoolkit/reference/ieboilstart.html) | Applies best practices for collaboration and reproducibility within a project |
| [ieddtab](https://worldbank.github.io/ietoolkit/reference/ieddtab.html) | This command runs a Diff-in-Diff regression and displays the baseline values, the two 1st differences and the 2nd difference |
| [iedropone](https://worldbank.github.io/ietoolkit/reference/iedropone.html) | An extension of the command `drop` with features preventing additional observations are unintentionally dropped |
| [iefolder](https://worldbank.github.io/ietoolkit/reference/iefolder.html) | Sets up project folders and master do-files according to World Bank DIME's standards |
| [iegitaddmd](https://worldbank.github.io/ietoolkit/reference/iegitaddmd.html) | Creates a placeholder file in subfolders of a GitHub repository folder, which allows committing folder structures with empty folders |
| [iegraph](https://worldbank.github.io/ietoolkit/reference/iegraph.html) | Generates graphs based on regressions with treatment dummies common in impact evaluations |
| [iekdensity](https://worldbank.github.io/ietoolkit/reference/iekdensity.html) |  This command plots univariate kernel density estimates by treatment assignment |
| [iematch](https://worldbank.github.io/ietoolkit/reference/iematch.html) | Matching base observations towards target observations using on a single continuous variable |
| [iesave](https://worldbank.github.io/ietoolkit/reference/iesave.html) | Applies best practices before saving data, with option to save meta data report about the data saved |
| [ietoolkit](https://worldbank.github.io/ietoolkit/reference/ietoolkit.html) | Returns information on the version of `ietoolkit` installed |

### **Install and Update**

#### Installing published versions of `ietoolkit`
To install **ietoolkit**, type **`ssc install ietoolkit`** in Stata. This will install the latest published version of **ietoolkit**. The main version of the code in the repo (the `master` branch) is what is published on SSC as well.

 If you think something is different in version in this repo, and the version installed on your computer, make sure that you both look at the `master` branch in this repo, and that you have the most recent version of **ietoolkit** installed. To update all files associated with **ietoolkit** type **`adoupdate ietoolkit, update`** in Stata. (It is wise to be in the habit of regularly checking if any of your .ado files installed in Stata need updates by typing **`adoupdate`**.)

 When we are publishing new versions of **ietoolkit** then there could be a discrepancy between the master branch and the version on SSC as the master branch is updates a couple of days before. You can confirm if that could be the case by checking if we recently published a new [release](https://github.com/worldbank/ietoolkit/releases).

#### Installing unpublished branches of this repository
Follow the instructions above if you want the most recent published version of **ietoolkit**. If you want a yet to be published version of **ietoolkit** then you can use the code below. The code below installs the version currently in the `master` branch, but replace _master_ in the URL below with the name of the branch you want to install from. You can also install older version of **ietoolkit** like this but it will only go back to January 2019 when we set up this method of installing the package.

```
    net install ietoolkit , from("https://raw.githubusercontent.com/worldbank/ietoolkit/master/src") replace
```

#### Install older versions

You can install older versions of `ietoolkit` directly from the GitHub repository.
To do so, start by finding the tag corresponding to
the version you want to install here:
https://github.com/worldbank/ietoolkit/tags.
Update the local "tag" in the code below with the value of the tag you picked,
and then run the code.

```
local tag "v6.2"
net install ietoolkit, ///
  from("https://raw.githubusercontent.com/worldbank/ietoolkit/`tag'/src")
```

`v6.2` is the oldest version that can be installed with exactly this code. 
Older versions back to version `v2.0` may still be installed but not exactly like this.
View the source code in this repository to see how to update the code.
Please get in touch if you are not able to solve it.

#### Requirements
Different versions of this package requires a different minimum version of Stata. See the pkg-file or the ado-file for the version you want to use.

### **Background**
These commands are developed by people that work at or with the Development Impact Evaluations (DIME) unit at the World Bank. While the commands are developed with best practices for impact evaluations in mind, these commands can be useful outside that field as well.

### **Bug Reports and Feature Requests**
If you are familiar with GitHub go to the **Contributions** section below for advanced instructions.

An easy but still very efficient way to provide any feedback on these commands is to create an *issue* in GitHub. You can read *issues* submitted by other users or create a new *issue* in the top menu below [**worldbank**/**ietoolkit**](https://github.com/worldbank/ietoolkit) at [https://github.com/worldbank/ietoolkit](https://github.com/worldbank/ietoolkit). While the word *issue* has a negative connotation outside GitHub, it can be used for any kind of feedback. If you have an idea for a new command, or a new feature on an existing command, creating an *issue* is a great tool for suggesting that. Please read already existing *issues* to check whether someone else has made the same suggestion or reported the same error before creating a new *issue*.

While we have a slight preference for receiving feedback here on GitHub, you are still very welcome to send a regular email with your feedback to [dimeanalytics@worldbank.org](mailto:dimeanalytics@worldbank.org).

### **Contributions**
If you are not familiar with GitHub see the **Bug reports and feature requests** section above for a less technical but still very helpful way to contribute to **ietoolkit**.

GitHub is a wonderful tool for collaboration on code. We appreciate contributions directly to the code and will of course give credit to anyone providing contributions that we merge to the master branch. If you have any questions on anything in this section, please do not hesitate to email [dimeanalytics@worldbank.org](mailto:dimeanalytics@worldbank.org). See [CONTRIBUTING.md](https://github.com/worldbank/ietoolkit/blob/master/CONTRIBUTING.md) for some more details on for example naming conventions.

The Stata files on the `master` branch are the files most recently released on the SSC server. README, LICENSE and similar files are updated directly to `master` in between releases. Check out any of the `develop` branches (if there are any) if you want to see what future updates we are currently working on.

Please make pull requests to the `master` branch **only** if you wish to contribute to README, LICENSE or similar meta data files. If you wish to make a contribution to any Stata file, then please **do not** use the `master` branch. If you wish to make a contribution to any Stata files that we have published at least once, then please fork from and make your pull request to the `develop` branch. The `develop` branch includes all minor edits we have made to already published commands since the last release that we will include in the next version released on the SSC server. If your addition is related to a specific issue in this repository, then see the naming convention in the [CONTRIBUTING.md](https://github.com/worldbank/ietoolkit/blob/master/CONTRIBUTING.md) file.

All Stata commands we are working on that we have yet to release a first version of, are found in the branches called `develop-NAME` where *NAME* corresponds to the working name of the command that is yet to be published. If you wish to contribute to any of those commands, then please fork from the branch of the command you want to contribute to, and only make edits to the .ado/.do and .sthlp that correspond to that command. If you want to make contributions to multiple commands that have yet to be released, then you will have to fork from and make pull request to multiple branches.

If you wish to make a contribution by making *forks and pull requests* but are not exactly sure how to do so, feel free to send an email to [dimeanalytics@worldbank.org](mailto:dimeanalytics@worldbank.org).

### **License**
**ietoolkit** is developed under MIT license. See http://adampritchard.mit-license.org/ or see [the `LICENSE` file](https://github.com/worldbank/ietoolkit/blob/master/LICENSE) for details.

### **Contact**
DIME Analytics ([dimeanalytics@worldbank.org](mailto:dimeanalytics@worldbank.org))

### **About us**
[DIME](https://www.worldbank.org/en/research/dime) is the World Bank's impact evaluation department. Part of DIME’s mission is to intensify the production of and access to public goods that improve the quantity and quality of global development research, while lowering the costs of doing IE for the entire research community. This Library is developed and maintained by [DIME Analytics](https://www.worldbank.org/en/research/dime/data-and-analytics). DIME Analytics supports quality research processes across the DIME portfolio, offers public trainings, and develops tools for the global community of development researchers.

Other DIME Analytics public goods are:
- [Development Research in Practice:](https://worldbank.github.io/dime-data-handbook/) the DIME Analytics Data Handbook
- [DIME Wiki:](https://dimewiki.worldbank.org/wiki/Main_Page) a one-stop-shop for impact evaluation resources
- [iefieldkit:](https://github.com/worldbank/iefieldkit) Stata package for primary data collection
- [Stata Visual Library](https://github.com/worldbank/stata-visual-library)
- [R Econ Visual Library](https://github.com/worldbank/r-econ-visual-library)
- [DIME Research Standards:](https://github.com/worldbank/dime-standards/blob/master/dime-research-standards/) DIME's commitments to best practices
