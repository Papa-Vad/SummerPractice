#       Summer Practice   
## Purpose
The purpose of this practice was to learn basic features of [LaTeX](https://www.latex-project.org/).
## Achieved Goals
While creating practice.pdf(main.tex) and practice_pres.pdf(pres.tex), I learned how to :
- Create title page with any required data 
- Create contents list
- Create and work with Complex Tables 
- Insert images and work with them, insert images into text
- Create ordered and unordered and nested lists 
- Make footnotes, citations and references 
- Write complex math formulas 
- Separate text into sections, subsections and etc.
- Make presentations using beamer package 
- --
## How to begin using LaTeX
In the beggining one should choose how to use LaTeX online or offline. I chose to use [Overleaf](https://www.overleaf.com/project) since most of LaTeX documentation is also there. 
## Begining in LaTex
Creating your first project in LaTeX is pretty close to creating you first project using new programming language or IDE. You create a project with main.tex file and begin writting your text. My first step was to define the title page parametres,which was done by these commands
```
\title{DSBA SUMMER PRACTICE TASK}
\author{Vadim Khanin}
\date{July 2022}
```
And then to create this page
```
\maketitle
```
To make LaTeX more functional and gain more opportunities in it, one will need to include numerous packages, which work like libraries in programming langauges. For example, for comfortable work in LaTeX with formulas,maths,tables,footnotes,captions and figures I had to include the following packages.
```
\usepackage[utf8]{inputenc}
\usepackage[T2A]{fontenc}
\usepackage{tablefootnote}
\usepackage{footnote}
\usepackage{indentfirst}
\usepackage{amsmath}
\usepackage{graphicx}
\usepackage{wrapfig}
\usepackage{color}
\usepackage{subcaption}
\usepackage[export]{adjustbox}
\usepackage{float}
\usepackage{cite}
\usepackage{caption}
\usepackage{textcomp}
\usepackage{color,colortbl}
```
This packages allow new commands to be used. However, you may also manualy define some instructions or objects,it may be useful in some cases. For example, I did it when I needed to define the colors, which were not in the package.
```
\definecolor{col0}{RGB}{147, 30, 206}
\definecolor{col1}{RGB}{136, 117, 98}
\definecolor{col2}{RGB}{152, 127, 113}
\definecolor{col3}{RGB}{152, 127, 110}
\definecolor{col4}{RGB}{145, 122, 103}
\definecolor{col5}{RGB}{140, 119, 102}
\definecolor{col6}{RGB}{143, 121, 103}
\definecolor{col7}{RGB}{164,109,89}
\definecolor{col8}{RGB}{141, 120, 103}
\definecolor{col9}{RGB}{144, 121, 103}
\definecolor{col10}{RGB}{145,123, 105}
```

## Working with text, math formulas, tables and lists.
So, working with text in LaTex is very native and understandable. By using ```\section{section_name}``` or ```\subsection{subsection_name}``` you may split you text into logical parts, which will then appear in the table of content, which is also done automatically by ```\tableofcontents```. To insert math formula one should write it in dollar signs and use the [appropriate syntax](https://en.wikibooks.org/wiki/LaTeX/Mathematics#Symbols) for it. To create any structure or begin some action one writes ```\begin{structure_name}```.   

| Structure | How to create |
| ------ | ------ |
| Table | ```\begin{tabular}``` |
| Unordered list | ```\begin{itemize}``` |
| Ordered list | ```\begin{enumerate}``` |


After beginning the tabular, one have to define its structure, for example the following comand descibes the table with 5 columns ```    \begin{tabular}{| c | c | c | c | c |}```. Then each line is written using "&" to show where the column ends.
After beginnig Itemize or enumerate the items are written in the following manner ```\item itemname```. To end table or list the following command must be used ```\end{name_of_the_structure}```

To create a nested list one should simply do a list inside other list. To create multicolumn one may write ```\multicolumn{number of columns from the main table it will cover}{the structure, for example |c| }{text of the multicolumn}``` inside the description of the main table.

## Working with Images and creating presentation in LaTeX
Working with images in LaTeX is a bit painful as placing the image into correct place on the page may be tricky. To insert the image on the page the following command is required ```\includegraphics[parametres]{file_name}```. However, to insert the image into the text(to the right or to the left) package wrapfig is required. The main problem is that you cannot place the image using cursor, but have to measure how wide you want you picture to be. For example, the following commands 
```
    \begin{wrapfigure}{l}{0.4\textwidth}
        \centering
        \includegraphics[width=0.4\textwidth]{image.png}
        \caption{Caption}
    \end{wrapfigure}
```
Will place the image to the left from the text and its width will be 0.4 of the possible textwidth.

As for presentations, one way to make them using LaTeX is by using beamer package. What is convinient, is that title pagecan be done automatically, by writting the following commands
```\title{Latex Practice}
\author{Author_Name}
\institute{Institute_name}
\date{date}
\frame{\titlepage}
```
And table of content is done by 
```
\begin{frame}
    \frametitle{Content}
    \tableofcontents
\end{frame}
```
And this also represents the structute of any slide. Inside the frame you may write texts, formulas, lists, insert images and etc.

Nevertheless, the user is forced to choose from slide themes from the [list](https://latex-beamer.com/tutorials/beamer-themes/) as creating you own theme is very nontrivial and requires filling tones of parametres.
## Overall Impression 
Overall, LaTeX turned out to be simplier, than I thought. Whereas working with text, while writting an article for example, is quite fast(may be as fast as writting by hand, depending on you typing skills), the time required for writting down math formulas is a way longer, which makes LaTeX not the best option for solving homeworks, however LaTeX is a good option for teachers, when they need to make homework page readable for everyone. As for presentations in LaTeX, personally, I believe, that making a power point presentation is easier and faster, espessially, when it has a lot of images to hadle, since moving them with cursor is a way faster. 

## Contacts 
[telegram](tg:https://t.me/PapaVad)
