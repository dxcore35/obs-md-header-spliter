![](https://github.com/dxcore35/obs-md-header-spliter/blob/master/markdown-spliter-diagram.png)

One line AWK script for spliting markdown file into to multiple files. The spearator for splitting are first level markdown formatted headings.

# INPUT DATA FILE

Your markdown file is formated in the way, that heading have standard #(space) prefix. ```# Heading 1```.
All other heading levels 2,3,4,5,6 are not splitted.

## STEPS (MAC OS)

1. Open terminal
2. The Mac user you need to download GAWK (becouse AWK in Mac is broken)
3. Install GAWK just run command: ```brew install gawk```
4. Paste command: ```gawk -F, '/^# /{h=substr($0,3);} {print > ( h ".md")}' $Book.md$```
5. In script above replace ```$Book.md$``` with the path to markdown file you want to split.
6. Hit enter

## STEPS (WINDOWS, LINUX)

1. Open terminal
2. Paste command: ```awk -F, '/^# /{h=substr($0,3);} {print > ( h ".md")}' $Book.md$```
6. In script above replace ```$Book.md$``` with the path to markdown file you want to split.
7. Hit enter
