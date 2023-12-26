\documentclass[15.5pt]{article}
\usepackage{geometry}
\geometry{a4paper,left=2.54cm,right=2.54cm,top=3.17cm,bottom=3.17cm}
\usepackage{ctex}
\usepackage{xeCJK}
\usepackage{fontspec} 
% \setCJKmainfont{SimSun} %或\setCJKmainfont{KaiTi}
% \setCJKmonofont{SimSun} % 中文 SimSun
% \setmainfont{Times New Roman} % 英文 Times New Roman
\usepackage{graphicx}
\usepackage{subfigure}
\usepackage{multirow}
\usepackage{multicol}
\usepackage{amsmath,amsthm,amsfonts,amssymb}
\usepackage{color}
\usepackage{natbib}
\usepackage{makecell}
\usepackage{hyperref}
\usepackage{cleveref}
\usepackage{subfig}
\usepackage{listings}
\usepackage{color}
\definecolor{dkgreen}{rgb}{0,0.6,0}
\definecolor{gray}{rgb}{0.5,0.5,0.5}
\definecolor{mauve}{rgb}{0.58,0,0.82}
\lstset{frame=tb,
  language=Python,
  aboveskip=3mm,
  belowskip=3mm,
  showstringspaces=false,
  columns=flexible,
  basicstyle={\small\ttfamily},
  numbers=left,%设置行号位置none不显示行号
  %numberstyle=\tiny\courier, %设置行号大小
  numberstyle=\tiny\color{gray},
  keywordstyle=\color{blue},
  commentstyle=\color{dkgreen},
  stringstyle=\color{mauve},
  breaklines=true,
  breakatwhitespace=true,
  escapeinside=``,%逃逸字符(1左面的键)，用于显示中文例如在代码中`中文...`
  tabsize=4,
  extendedchars=false %解决代码跨页时，章节标题，页眉等汉字不显示的问题
}

\crefname{figure}{图}{}
\crefname{table}{表}{表}
\crefname{algorithm}{算法}{算法}



\linespread{2.0} % 2倍行距
% \renewcommand{\CJKglue}{\hskip 20pt}
\ziju{0.11}

%===============================%
% format of footnote
\usepackage{scrextend}
\deffootnote{0em}{0em}{\thefootnotemark\quad}
\makeatletter
\def\blfootnote{\gdef\@thefnmark{}\@footnotetext}
\makeatother


\makeatletter
\newcommand{\rmnum}[1]{\romannumeral #1}
\newcommand{\Rmnum}[1]{\expandafter\@slowromancap\romannumeral #1@}
\makeatother

% format of different section level
\usepackage{titlesec}
\titleformat{\section}{\normalfont\normalsize\bfseries}{\thesection\,}{1em}{}
\titleformat{\subsection}{\normalfont\normalsize\bfseries}{\thesubsection\,}{1em}{}
\titleformat{\subsubsection}[runin]{}{\thesubsubsection}{1em}{}[]

% format of figure and table
\usepackage[font=small]{caption} % footnotesize
\usepackage{bicaption}
% \captionsetup[figure][bi-second]{name=Fig.}
\captionsetup{labelformat=default,labelsep=space} % or period

% table \hline new define
\makeatletter
\def\hlinewd#1{%
\noalign{\ifnum0=`}\fi\hrule \@height #1 %
\futurelet\reserved@a\@xhline}
\makeatother

\newcommand{\tr}[1]{\textcolor{red}{#1}}

\begin{document}

{\centering
{\fontsize{22pt}{22pt}\selectfont 
{\bf 2023年十部热门电影分析}
}

\vskip 5mm
武汉大学国家网络安全学院


\vskip 2mm
汪宇恒\quad 2022302131143
\vskip 5mm

\par % end centering
}


{\bf 实验结果简述：}本次实验挑选了2023年十部热门电影进行分析，涉及以下的三个方面：\\\hspace*{1cm}（1）每部电影的评分，即1星$ \sim $ 5星分布比例；\\\hspace*{1cm}（2）每部电影的粉丝地区分布属性；\\\hspace*{1cm}（3）每部电影的票房属性及十部电影的横向比较;

\vskip 5mm
{\bf 信息来源：}百度、豆瓣
\vskip 15mm

\noindent

\section{十部电影的评论分析}

样本概述：本次实验采集了十部2023年的热门电影，九部电影为国产电影，一部为热门欧美电影，且类型涵盖面较广。\par
选择的电影：《三大队》、《孤注一掷》、《消失的她》、《长安三万里》、《流浪地球2》、《满江红》、《封神》、《奥本海默》、《八角笼中》、《河边的错误》

\subsection{各电影不同评级的分布比例}
每部电影分别选取了来自豆瓣官网的200+条评论，存入excel表格中，并利用SPSS进行了数据分析，制作饼状图将数据可视化。\par
十部电影的评级饼状图如下：

\begin{figure}[htbp]
  \centering
  \subfloat[《三大队》]
  {\includegraphics[width=0.3\textwidth]{1.jpg}\label{fig:subfig7}}
  [b]     % 重点就在这，优先横向排列，自动换行
  \subfloat[《孤注一掷》]
  {\includegraphics[width=0.3\textwidth]{2.jpg}\label{fig:subfig8}}
  [b]
  \subfloat[《河边的错误》]
  {\includegraphics[width=0.3\textwidth]{3.jpg}\label{fig:subfig9}}
  [b]
  \subfloat[《消失的她》]
  {\includegraphics[width=0.3\textwidth]{4.jpg}\label{fig:subfig10}}
  [b]
  \subfloat[《流浪地球2》]
  {\includegraphics[width=0.3\textwidth]{5.jpg}\label{fig:subfig10}}
  [b]
  \subfloat[《长安三万里》]
  {\includegraphics[width=0.3\textwidth]{6.jpg}\label{fig:subfig10}}
  [b]
  \subfloat[《奥本海默》]
  {\includegraphics[width=0.3\textwidth]{7.jpg}\label{fig:subfig10}}
  [b]
  \subfloat[《封神》]
  {\includegraphics[width=0.3\textwidth]{8.jpg}\label{fig:subfig10}}
  [b]
  \subfloat[《满江红》]
  {\includegraphics[width=0.3\textwidth]{9.jpg}\label{fig:subfig10}}
  [b]
  \subfloat[《八角笼中》]
  {\includegraphics[width=0.3\textwidth]{10.jpg}\label{fig:subfig10}}
  [b]
  \caption{十部电影评级频率分布}
\end{figure}

\newpage

\subsection{各个电影的好评率纵向比较}
{\bf 好评：}设置4星$ \sim $ 5星为好评\par
那么，下面开始研究十部电影的好评率纵向比较：\par

\begin{figure}[h]
    \centering
    \includegraphics[width=0.75\linewidth]{13.png}
    \caption{十部电影好评率比较}
    \label{fig:enter-label}
\end{figure}
结合上图，发现：《三大队》、《流浪地球2》、《奥本海默》、《八角笼中》四部影片的好评率超过一半，其余六部影片均小于一半。\par

不难发现，《三大队》是这十部电影中好评率最高的一部电影，而《消失的她》是其中好评率最低的电影。一方面，这个数据可以在一定程度上反映当代影迷对题材新颖程度、生活贴切程度电影的需求；另一方面，也激励着新时代电影产业的不断发展：仅仅依靠改编和俗套的“翻转”，观众是不买账的。

\section{十部电影的票房分析}
除《三大队》以外，其他电影皆已下映。换言之，只有《三大队》票房会继续增长，剩下的九部电影的票房不会大幅度改变，故可信程度和参考价值较高。\par

十部电影的票房柱状图如下：\par
\newpage

\begin{figure}[h]
    \centering
    \includegraphics[width=0.75\linewidth]{14.png}
    \caption{十部电影票房情况}
    \label{fig:enter-label}
\end{figure}

不难发现，不同电影之间的票房差距是显著的。例如：《奥本海默》的票房足有50亿多，而《河边的错误》票房仅仅只有2.92亿元。而造成这方面差距的有众多因素，如：受众、影片类型、拍摄投入、上映时间等等。就针对上面的例子而言，《奥本海默》投入成本大，受众较广，且全世界上映，自然能够获得较高的票房。

\section{电影的粉丝分布属性}
本实验采集了豆瓣网上评论显示的IP地址作为相应电影的粉丝所在地址（{\bf 注：}每部电影选取的评论数为230条），下面就以《消失的她》为例，对其粉丝分布情况进行分析。\par


\begin{figure}[h]
    \centering
    \includegraphics[width=0.9\linewidth]{23.png}
    \caption{《消失的她》影迷分布情况}
    \label{fig:enter-label}
\end{figure}
\newpage

对上述数据进行处理，分析出《消失的她》各地区粉丝分布数目的一些基础的统计特征：\par

\begin{figure}[h]
    \centering
    \includegraphics[width=0.9\linewidth]{32.png}
    \caption{《消失的她》粉丝分布统计特征}
    \label{fig:enter-label}
\end{figure}

将数据可视化处理，使《消失的她》影迷分布情况更清晰。\par


\begin{figure}[h]
    \centering
    \includegraphics[width=0.75\linewidth]{30.png}
    \caption{《消失的她》粉丝分布三维条形图}
    \label{fig:enter-label}
\end{figure}


结合上面图表及数据特征，笔者列出三点最基本信息（可提炼的信息远不止三条）：（1）北京影迷最多；（2）影迷分布范围广泛；（3）各地影迷数量差异较大。


\section{数据分析过程}
众所周知，评价一步影片的维度是多重的，本次实验从影迷评论、票房收入方面对十部电影进行了分析，下面将展现数据获取以及分析的过程（仅供参考）。
\subsection{评论及评级的爬取}
为从豆瓣网上获取较为大量的评论及评级数据，本人利用Python进行爬虫，将爬的的数据存入excel表格中，以供后续的使用以及数据分析。\par

代码展示如下：\par

\begin{lstlisting}
import requests
from bs4 import BeautifulSoup
import urllib.parse

import xlwt
import xlrd


def login(username, password):
    url = 'https://accounts.douban.com/j/mobile/login/basic'
    header = {
        'user-agent': 'Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.86 Safari/537.36',
        'Referer': 'https://accounts.douban.com/passport/login_popup?login_source=anony',
        'Origin': 'https://accounts.douban.com',
        'content-Type': 'application/x-www-form-urlencoded',
        'x-requested-with': 'XMLHttpRequest',
        'accept': 'application/json',
        'accept-encoding': 'gzip, deflate, br',
        'accept-language': 'zh-CN,zh;q=0.9',
        'connection': 'keep-alive'
        , 'Host': 'accounts.douban.com'
    }

    data = {
        'ck' : '',
        'name': '',
        'password': '',
        'remember': 'false',
        'ticket': ''
    }
    data['name'] = username
    data['password'] = password
    data = urllib.parse.urlencode(data)
    print(data)
    req = requests.post(url, headers=header, data=data, verify=False)
    cookies = requests.utils.dict_from_cookiejar(req.cookies)
    print(cookies)
    return cookies

def getcomment(cookies, mvid):  
    start = 0
    w = xlwt.Workbook(encoding='ascii') 
    ws = w.add_sheet('sheet1')  
    index = 1  
    while True:

        header = {
            'user-agent': 'Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/73.0.3683.86 Safari/537.36',
        }
   
        try:
  
            url = 'https://movie.douban.com/subject/' + str(mvid) + '/comments?start=' + str(
                start) + '&limit=20&sort=new_score&status=P&comments_only=1'
            start += 20
     
            req = requests.get(url, cookies=cookies, headers=header)
      
            res = req.json()
            res = res['html']  
            soup = BeautifulSoup(res, 'lxml') 
            node = soup.select('.comment-item') 
            for va in node:  
                name = va.a.get('title')  
                star = va.select_one('.comment-info').select('span')[1].get('class')[0][-2]  
                votes = va.select_one('.votes').text  
                comment = va.select_one('.short').text  
                print(name, star, votes, comment)
                ws.write(index, 0, index) 
                ws.write(index, 1, name)  
                ws.write(index, 2, star)  
                ws.write(index, 3, votes)  
                ws.write(index, 4, comment)  
                index += 1
        except Exception as e: 
            print(e)
            break
    w.save('test9.xls')  


if __name__ == '__main__':
    username = input('输入账号：')
    password = input('输入密码：')
    cookies = login(username, password)
    mvid = input('电影的id为：')
    getcomment(cookies, mvid)
\end{lstlisting}


依靠本程序，实现了将豆瓣网上有关这十部电影的评论均存入了excel表格中。（具体代码将在另一文件中展示）
\subsection{数据分析以及可视化处理}
此处对于数据处理仅进行简要叙述和展示，详细细节不再赘述。\par
{\bf 利用的工具：}SPSS、Excel\par

首先先将Excel导入IBM SPSS中，利用其中的指表工具进行可视化处理。处理结果和过程如下（仅拿《三大队》举例）：\par
\newpage

\begin{figure}[h]
    \centering
    \includegraphics[width=0.75\linewidth]{17.png}
    \caption{SPSS制评级分布饼图}
    \label{fig:enter-label}
\end{figure}

针对票房统计以及各电影的票房和好评率的纵向比较，利用到了Excel及其中的制图工具，展示如下：\par

\begin{figure}[h]
    \centering
    \includegraphics[width=0.7\linewidth]{18.png}
    \caption{好评率柱状图制作}
    \label{fig:enter-label}
\end{figure}

\newpage

\begin{figure}[h]
    \centering
    \includegraphics[width=0.7\linewidth]{19.png}
    \caption{票房柱状图制作}
    \label{fig:enter-label}
\end{figure}

将好评率和票房制作成柱状图，将数据可视化，可以更清晰地观察出各个电影之间在这两方面的差异。


\section{判断票房和好评率是否存在线性关系}
除去上面对于电影的分析，笔者还对票房与好评率之间的关系产生兴趣，于是进行了以下实验：\par

根据朴素的想法，自然总结出：好评率和票房存在一定的正相关：因为好电影必定是口碑好的，而口碑好的属性自然会给其带来高票房的结果。因此，将样本中的十个电影的好评率和票房收入制作成散点图，观察票房和好评率的关系。\par

\begin{figure}[h]
    \centering
    \includegraphics[width=0.75\linewidth]{20.png}
    \caption{好评率-票房收入散点图}
    \label{fig:enter-label}
\end{figure}

\newpage

观察上述散点图，不难发现，票房收入和好评率之间并没有直接的关系，这个结论也可以通过计算皮尔斯相关系数来得到进一步验证。分析产生这个与我们认知相违背的结果的原因，笔者认为有以下三个：（1）样本个数太少，10部电影不具有代表性，可能当样本个数够大时，二者会呈现出一定的相关性；（2）实际上，大多数影迷并不会上豆瓣评论，故豆瓣上呈现的好评率并不能代表全体影迷的好评率；（3）不排除有部分电影制作商存在着刷票房的行为。

\section{总结和Future work}
本次实验，本人学习了运用Python爬虫及SPSS和Excel等工具。学习了处理较大数据量情况下的数据分析。同时，充分利用可视化工具，让数据变得更加清晰、便于分析。切身体会到了“在运用中学习”的真谛。\par

除去上述研究外，本人对{\bf 地区影迷数量与地区GDP水平、更大数据量水平下票房和好评率的关系等}研究方向有一定的兴趣，将在未来的工作中体现。\par

\vskip 110mm


{\centering
{\bf 纸上得来终觉浅，绝知此事要躬行。 ——陆游《冬夜读书示子聿》}
\par}
\end{document}
