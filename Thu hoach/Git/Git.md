# NHỮNG ĐIỀU CẦN NHỚ VỀ GIT
- Git là một Version control, nhằm quản lý sự thay đổi về code theo thời gian: Có thể xem lại ai đã chỉnh sửa code gì, thời gian chỉnh sửa, có thể quay lại code cũ nếu cần.
- Một trong những điểm mạnh của Git là khả năng phân nhánh - hay còn gọi là tạo branch mới. Mỗi brand sẽ là một nhánh phát triển riêng như fix bug, version tiếp theo,...

![image](https://github.com/nhathoa/DevOps-Roadmap/assets/9213605/fc9c0f47-ddff-4e69-bf40-4895197179d8)

- Mỗi người tham gia vào một repo sẽ lưu code ở máy local của mình và toàn bộ thông tin về commit của source code

![image](https://github.com/nhathoa/DevOps-Roadmap/assets/9213605/95e78b27-6de8-4946-ac6c-50256f0173b0)

- Pull request yêu cầu nhập mã của một nhà phát triển trên một nhánh vào nhánh chính hoặc nhánh của một nhà phát triển khác.

![image](https://github.com/nhathoa/DevOps-Roadmap/assets/9213605/767a41fd-8ca0-41aa-beef-266ff8730244)


## Sử dụng GIT
### Cài đặt Git
- Cài đặt trên Windows bình thường. Sau khi cài chạy lệnh này để cấu hình user của mình.

```bash
$ git config --global user.name "nhathoa"
$ git config --global user.email "hoangnhathoa@gmail.com"
```

Sau khi cài xong Git, sử dụng GCM để lưu sẵn thông tin đăng nhập Git, khoi cần nhập vào mỗi lần commit

https://github.com/git-ecosystem/git-credential-manager

Chỉ cần cài vào thôi. Lần sau khi clone hay gì đó, Git sẽ yêu cầu đăng nhập, và thông tin tự động được lưu ở GCM.




