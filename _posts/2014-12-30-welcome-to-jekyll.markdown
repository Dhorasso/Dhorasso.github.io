---
layout: post
title:  "Numerical method to solves the system of ODE's and PDE's"
date:   2014-12-30 09:00:13
categories: jekyll update
permalink: /archivers/hello
---

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
