---
layout: post
title: "Tại sao sử dụng Octopress?"
date: 2013-03-21 00:21
comments: true
categories: 
---

Khi tạo blog mọi người thường sử dụng [Wordpress](http://chnghia.wordpress.com) hoặc blogspot tuy nhiên các blog này thường phải sử dụng database để lưu các post, việc này tuy tiện lợi nhưng về mặt kỹ thuật nó sẽ tốn nhiều thời gian hơn để render một page, độ bảo mật không tốt vì có thể đánh cắp password ...

Đối với Octopress việc này được khắc phục vì nó dạng static blog, các post/page của blog được generate từ trước, không phải tốn thời gian đọc database, cũng như blog chỉ ở dạng static page, nên việc hack blog trở nên khó khăn hơn, khi việc upload thông qua Git hoặc rsync (sử dụng public/private key, không có tham gia của việc nhập password)
