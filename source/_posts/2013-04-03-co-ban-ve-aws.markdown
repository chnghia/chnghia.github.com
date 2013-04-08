---
layout: post
title: "Cơ bản về AWS"
date: 2013-04-03 23:00
comments: true
categories: [IAAS, AWS]
---

Đây là một số kinh nghiệm khi làm cho dự án về AWS. Để tìm hiểu sâu hơn các bạn có thể tham khảo [tại đây](http://aws.amazon.com/documentation/). AWS hiện tại cung cấp nhiều dịch vụ tùy vào yêu cầu dự án thì các bạn có thể sử dụng những dịch vụ cần thiết, đối với dự án của mình thì do dự án là chuyển đổi từ hosting sang AWS nên mình sử dụng các dịch vụ:

- EC2 with EBS
- VPC
- Loadbalancer
- S3 (for backup)
- EC2-tools

<!--more-->
{% img /images/post/2013-04-04-co-ban-ve-aws.png 600%}

### EC2 with EBS
Dịch vụ EC2 dùng để chạy 1 instance (máy ảo). Về cơ bản để chạy 1 instance trên EC2 thì bạn có 2 cách

- Sử dụng các instance mặc định, hoặc trên AWS market place
- Hoặc tự tạo instance

### VPC (Virtual Private Cloud)
Dùng để xây dựng 1 private network trên AWS, theo tài liệu của AWS thì có nhiều mô hình lựa chọn để xây dựng VPC,
ngoài ra, Amazon cũng cung cấp dịch vụ VPN có tính phí đi kèm với VPC. Mình không sử dụng dịch vụ VPN mà thay vào đó
là tự xây dựng một OpenVPN tiết kiệm hơn.

### Loadbalancer
Dùng để cấu hình load balancer cho các service

### S3 (Simple Storage Service)
Dùng để lưu trữ với giá tốt hơn so với sử dụng EBS. Ở đây mình chỉ sử dụng S3 như một Linux file system bằng cách sử dụng [s3ql](https://code.google.com/p/s3ql/)

### EC2-tools
Với AWS ngoài việc sử dụng giao diện WEB thì bạn có thể sử dụng thư viện CLI để thao tác. Bạn có thể download thư viện [tại](http://aws.amazon.com/developertools/351) hoặc tạo 1 instance Amazon Linux AMI có sẳn thư viện EC2-tools để sử dụng. Bạn chỉ cần thiết lập thêm

``` bash
export AWS_ACCESS_KEY=<aws-access-key>
export AWS_SECRET_KEY=<aws-secret-key>
export EC2_URL=https://<region-url>
```

Với `<aws-access-key>/<aws-secret-key>` được lấy tại `Account Settings > Security Credentials > Access Credentials`.
Nếu chưa tạo thì bạn `Create a new Access Key`

Với `<region-url>` được liệt kê trên shell bằng command `ec2-describe-regions`