---
layout: post
title:  "开发环境搭建流程"
date:   2016-10-11 14:08:20 +0800
categories: github-pages bundle jekyll
---
【笔者注】 感谢涛哥的悉心教授与耐心讲解

>[风雪夜归人( lutaoact )](https://github.com/lutaoact)

主要流程参考[Github Pages][github-pages]

搭建jekyll的流程参考[Blogging with Jekyll][setup-jekyll-locally]

其它安装注意事项：
{% highlight sh %}
# ruby源总是连不上，使用国内的镜像源
gem sources -l #查看源列表
gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/ #修改源地址

# 安装bundle命令
sudo gem install bundler

# 编辑好Gemfile后，安装其它依赖，最好修改bundle的源
bundle config mirror.https://rubygems.org https://ruby.taobao.org

bundle install
bundle exec jekyll serve
{% endhighlight %}

修改ruby的镜像源，可以参考[链接][ruby-mirror]

[github-pages]: https://pages.github.com/
[setup-jekyll-locally]: https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/
[ruby-mirror]: https://ruby.taobao.org/
