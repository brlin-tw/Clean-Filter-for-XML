# 用於 XML 的清潔過濾器<br>Clean Filter for XML
A clean filter for XML for Git and other applications.  Currently it only beautifies the file using XMLstarlet

<https://github.com/Lin-Buo-Ren/Clean-Filter-for-XML>

## 依賴的軟體<br>Software Dependencies
Every software's executable directory should be in the shell's executable search `$PATH`

* GNU Bash as the scripting language
* XMLstarlet as the XML beautifer

## 如何使用<br>How to use it
Feel free to customize it according to your project configuration, the following instructions takes assumption that your working directory is at the root of your git worktree.

1. Add this repository as the repository's submodule with the following command:

        git submodule\
            add\
            --depth=1\
            'https://github.com/Lin-Buo-Ren/Clean-Filter-for-XML.git'

1. Update required sub-submodules with the following command:

        git submodule\
            update\
                --init\
                --recursive\
                "Clean Filter for XML"

1. Setup external git config with the following command:

        git config\
            --file .gitconfig\
            filter.xml.clean\
            '"./Clean Filter for XML/Clean Filter for XML.bash"'
  Note that the single and double braces are required(for GNU Bash syntax, other shell may need adjustments)

1. Setup Git to read previously created external config with the following command:

        git config\
            --local\
            include.path\
            ../.gitconfig

1. Add the following content in the `.gitattributes` file:

        ## Setup filters for XML
        ## Refer .gitconfig for more information
        *.xml filter=xml
  Add whatever filename extension that is in XML format.

1. All set!  From now on all XML file check-in will be automatically be cleaned!

## 原作者<br>Original Author
林博仁 &lt;<Buo.Ren.Lin@gmail.com>&gt;

## 智慧財產授權條款<br>Intellectual Property License
GNU GPLv3+

```
這個專案介紹文件是基於專案介紹文件範本
This README is based on Project README Template

http://github.com/Lin-Buo-Ren/Project-README-templates
```
