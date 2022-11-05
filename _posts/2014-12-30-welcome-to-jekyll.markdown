---
layout: post
title:  "Numerical method to solves the system of ODE's "
date:   2014-12-30 09:00:13
categories: jekyll update
permalink: /archivers/hello
---
Let $$\{ t_k\}$$ be a partition of $$[a,b]$$ such that $$a=t_0<t_1<\cdots<t_{N}=b$$ and $H$ be the constant length of the $$k$$-th subinterval ($$H = t_k - t_{k-1}$$). Let us consider initial value problem

$$\begin{equation}\label{eul2}
  \begin{cases}
    \dfrac{dz}{dt} = f(z,t),      & \quad \text{on } [a, b]\\\\
    z(a) = c,
  \end{cases}
\end{equation}$$
where $$z,f,c\in R^M$$ i.e. $$z = [x_1, x_2,\cdots, x_{M}]$$, $$c = [x_1(a), x_2(a),\cdots, x_{M}(a)]$$ and $$f = [f_1, f_2,\cdots, f_{M}]$$. Note that \eqref{eul2} is a the general form of system of ODEs. 

Let $$t, z_k,Z$$ defined as follows $$t=[t_0,t_2,\cdots,t_{N-1},t_{N}],\quad z_k = [x_1(t_k), x_2(t_k),\cdots, x_{M}(t_k)], \quad
Z =\begin{pmatrix}
x_1(t_0)& x_2(t_0)&\cdots& x_{M}(t_0)\\
x_1(t_1)& x_2(t_1)&\cdots& x_{M}(t_1)\\
x_1(t_2)& x_2(t_2)&\cdots& x_{M}(t_2)\\
\vdots& \vdots&\ddots& \vdots\\
x_1(t_{N})& x_2(t_{N})&\cdots& x_{M}(t_{N})
\end{pmatrix}
$$

1. Write a python function <b> EulerOdeSys </b> that takes $$f,c,t$$ and return the solution $$Z$$ of the initial value problem \eqref{eul2} using Euler method i.e.
$$ z_{k+1} = z_k + Hf(z_k,t_k) $$

Euler Method
```ruby
def EulerOdeSys(f,c,t):
    H=t[1]-t[0]
    N=len(t)-1
    M=len(c)
    z = np.ones((N+1, M))
    z[0] = c
    for i in range(N):
        z[i+1]=z[i]+H*f(z[i],t[i])
    return z
```

And $$\mathcal{ Mathematics }$$ is supported!

Use `$$` to wrap your formulas. For example, `$$ e^{i\pi} + 1 = 0 $$` displays $$  e^{i\pi} + 1 = 0  $$

Multi-line forumlas are supported too.

$$
\begin{aligned}
& J(w, b) = \frac{1}{m} \sum_{i=1}^{m}L(\hat{y}^{(i)}, y^{(i)})
+ \frac{\lambda}{2m} \sum_{l=1}^{L}{||w||}^2_F\\\\
& {||w||}^2_F = \sum_{i = 1}^{n[l]}\sum_{j = 1}^{n[l-1]}(w_{ij})^2
\end{aligned}
$$


## EasyBook Advanced Functions ##

You are using [EasyBook][github-easybook] the template from [laobubu.net](http://laobubu.net). Therefore some features are supported now:

* **Pagination** is enabled.
* **Disqus** or **多说** is ready.
* **TOC** for posts is enabled.
* **Profile** including your links and avatar on the sidebar.
* *And more...*

> **Tips:** You can disable Disqus or 多说 on posts/pages by adding `nocomments: true` into [YAML Front Matter][frontmatter].

EasyBook uses upaiyun CDN to make everyone lncluding Chinese visitors feel speedy. You can find it in `_includes/footer.html` and change it to your favorite CDN like Google CDN.

## Support me by... ##

### Add a link ###

EasyBook does not make the footer heavy; the link to theme could be on `about.md`:

> This website is using [laobubu](http://laobubu.net)'s theme: [EasyBook](https://github.com/laobubu/jekyll-theme-EasyBook)

### Donate (PayPal or 支付宝) ###

That's the best :smile: 

Please visit [http://laobubu.net/donate.html](http://laobubu.net/donate.html)

### Star and Fork on GitHub (free) ###

Not going to donate? That's okay. You can also send out your precious star [on GitHub][github-easybook].

## And Here We Go ##

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[frontmatter]: http://jekyllrb.com/docs/frontmatter/
[github-easybook]: https://github.com/laobubu/jekyll-theme-EasyBook
