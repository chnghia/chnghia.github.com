---
layout: post
title: "Tạo blog bằng Octopress"
date: 2013-03-22 00:10
comments: true
categories: [blog, octopress]
---

Để tạo một static-blog sử dụng Octopress các bạn có thể làm theo các bước đơn giản sau:

- Các yêu cầu cài đặt
- Dùng git clone repo Octopress về máy
- Thiết lập các giá trị
- Chạy thử trên máy tính
- Deploy blog
- Tạo post/page cho blog
- Sử dụng plugin

<!--more-->

### Các yêu cầu cài đặt

Dùng `cmd.exe` (Windows) hoặc `terminal` (Linux) để kiểm tra

1. Git `git --version`
2. Ruby 1.9.3 `ruby -v`

{% img /images/post/2013-03-22-tao-blog-octopress-img1.png %}

### Dùng git clone repo Octopress về máy

``` bash
git clone git://github.com/imathis/octopress.git your-blog
cd your-blog

# 
gem install bundler

#
bundle install

#
rake install

```

### Thiết lập các giá trị
### Chạy thử trên máy tính
### Deploy blog
### Tạo post/page cho blog
### Sử dụng plugin