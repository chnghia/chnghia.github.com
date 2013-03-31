---
layout: post
title: "Môi trường develop cho Windows"
date: 2013-03-29 20:30
comments: true
categories: [Windows, Develop]
---

###Mục đích
Đây là những thiết lập của mình cho một môi trường develop hướng đến lập trình Ruby, NodeJS, hoặc Web nói chung.
Ngoài ra, việc cài đặt còn phụ thuộc vào thói quen sử dụng máy tính. Nên tuỳ vào nhu cầu thì các bạn chỉ cần cài đặt phần các bạn sử dụng mà thôi.
<!--more-->
{% img /images/post/2013-03-29-windows-desktop.png 600%}

###Cài đặt
- Cài đặt phần mềm dùng chung: Dropbox, Evernote, Editor - Sublime Text (*), Programmer's Notepad ...
- Cài đặt Git
- Cài đặt Ruby
- Cài đặt NodeJS
- Cài đặt Python
- Các thiết lập môi trường

###Chi tiết

####Phần mềm dùng chung
- [Dropbox](http://db.tt/59oLmVtJ)

Có nhiều cloud storage nhưng vẫn thích cái này nhất, cái này rất hay nếu tận dụng nó để làm repositories cho 1 team nhỏ.
Ngoài ra, cũng có thể sử dụng làm một static-blog bằng [Calepin.co](http://calepin.co/)

- [Evernote](https://www.evernote.com)

Dùng để ghi chú, mình đã không sử dụng OneNote nữa bởi cái này, hỗ trợ đa nền tảng, tuy chức năng không tốt bằng OneNote.

- [Sublime Text 2](http://www.sublimetext.com/) (purchase)

Đây là editor gần như tốt nhất hiện tại, hỗ trợ nhiều thứ bằng plugins - Package Control, ngoài ra mình thích nhất cái folders của nó.

- [Programmer Notepad](http://www.pnotepad.org/)

Đây là editor khá tốt, mình không thích Notepad++ vì nó xấu hơn cái editor này :)

- [Console2](http://sourceforge.net/projects/console/)

Đây là emulator support multi-tab và một số thứ khác

- [ConEmu](https://code.google.com/p/conemu-maximus5/)

Emulator này thay thế rất tốt Console2 ở trên, nhưng mình vẫn xài cả hai :)

- [VirtualBox](https://www.virtualbox.org/)

Mình dùng cái này như một test environment và một *nix terminal

####Git
- [msysGit](http://msysgit.github.com/)
- [github](http://github.com)
- [bitbucket](http://bitbucket.org)

####Ruby
- [RubyInstaller](http://rubyinstaller.org/)
- [RailsInstaller](http://railsinstaller.org/)

####NodeJS
- [NodeJS](http://nodejs.org/)

####Python
- [Python](http://www.python.org/)

####Các thiết lập môi trường 
Sau khi cài đặt xong thì cần phải tinh chỉnh một số thứ như thiết lập PATH, thiết lập Bash Shell cho Console2(ConEmu),
thêm alias, thay đổi bash prompt

**Console2 - ConEmu**

Với Console2, tại `settings > tabs` thiết lập Bash shell của msysgit bằng `C:\Windows\SysWOW64\cmd.exe /c ""C:\Program Files (x86)\Git\bin\sh.exe" --login -i"` tại mục `shell`, `name` thì đặt là `Bash`, và chuyển Tab này lên đầu thì khi mở Console2 nó sẽ vào Bash shell.

Với ConEmu, `settings > startup > tasks` thiết lập Bash shell của msysgit giống trên, để khi khởi động thì vào Bash shell thì chọn `Specified named task` là `Bash` theo tên task đã đặt.

{% blockquote %}
Việc sử dụng Bash shell một *nix terminal trên Windows sẽ giúp mình sử dụng được `ssh-client`, `scp`, `vim` và một cấu trúc thư mục tương thích với Linux
{% endblockquote %}

**Git - Github - Bitbucket**

**Alias**

**Sublime Text**

###Kiểm tra lại

