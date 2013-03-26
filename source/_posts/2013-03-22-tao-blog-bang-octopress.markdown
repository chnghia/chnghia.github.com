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

### Dùng git clone repo Octopress về máy

``` bash
git clone git://github.com/imathis/octopress.git your-blog
cd your-blog

# 
gem install bundler

#
bundle install

#
bundle exec rake install
```

### Thiết lập các giá trị
### Chạy thử trên máy tính

``` bash
bundle exec rake generate    # Generate post và page tại thư mục public
bundle exec rake watch       # Kiểm tra thay đổi tại thư mục source/ và sass/ và liên tục generate blog
bundle exec rake preview     # Giống trên và tạo webserver tại http://localhost:4000

```

### Deploy blog

### Tạo post/page cho blog
#### Tạo Post
```
bundle exec rake new_post["title"]
```
#### Tạo Page

``` bash
bundle exec rake new_page[page-title]
# creates /source/page-title/index.markdown
bundle exec rake new_page[page-title/sub-page.html]
# creates /source/page-title/sub-page.html
```

### Sử dụng plugin