## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/sofan110/sofan110.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

[TOC]

# Reinforcement Learning

强化学习体系总结

## MDP总结

### MDP

### semi-MDP

很多option并非是Markov的，因此对于HRL提出了SMDP的概念。

任何拥有固定options集的MDP本质上都是SMDP

## Model Free

### Hierarchical RL

**Abstract**

有两篇关于HRL的综述文章[Pateria, 2021](https://doi.org/10.1145/3453160)&[Barto, 2003](https://doi.org/10.1023/A:1022140919877)和一篇[知乎综述](https://zhuanlan.zhihu.com/p/267524544)

abstract actions部分主要分为*options*和*goal-conditioned policy/value functions* (GCVF)。

[俞扬老师这篇](http://html.rhhz.net/tis/html/201706031.htm)写的还是非常清楚的。

**Methods**

##### [Proto-value Functions: A Laplacian Framework for Learning Representation and Control in Markov Decision Processes](https://dl.acm.org/doi/10.5555/1314498.1314570)



**Advantages**

## Model Base

### Dynamics Model Learning

#### State Abstraction

#### Temporal abstraction (Hierarchical RL)

**Abstract**

HRL的思想在MB中的应用。

问题的核心在于如何对轨迹聚类，即identify the relevant subroutines。

**Methods**

- Graph Structure

- State-space coverage

  ##### [A Laplacian Framework for Option Discovery in Reinforcement Learning](https://proceedings.mlr.press/v70/machado17a.html)

  - Background

    - Option $$\omega$$ 定义为一个三元组 $$\omega = <I,\pi,T>$$

      $$I$$ 是option初始的状态集合，$\pi:S\times A\rightarrow[0,1]$表示option的策略，$T:S\rightarrow[0,1]$表示终止条件，$\beta(s)$表示状态$s$有$\beta(s)$的概率终止并推出此option。 

    - Bottleneck States

      连接MDP图中两个子图的状态

    - Proto-value function（PVF）

      PVFs可以探索MDP上状态之间的图结构，有效探索到状态之间的对称性和瓶颈，具体可见[Proto-valuefunction](#Proto-value Functions: A Laplacian Framework for Learning Representation and Control in Markov Decision Processes)

  - Method

    - Eigenpurpose

      即PVF $e\in \R^{|S|}$ 对应的内在奖励$r_i^e(s,s')=e^T(\Phi(s')-\Phi(s))$。$\Phi(x)$是状态表征函数。(这不就是探索吗？PVF相当于不同的option探索不同？)

    - Eigenbehavior

      即对应Eigenpurpose的最优策略$X^e$

    - 

  - Experiment

    - 

  - 

- Compression(information-theoretic)

  ##### 

- Reward relevancy

- Priors



**Advantages**

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/sofan110/sofan110.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
