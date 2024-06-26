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


### Khởi tạo Git repo
  Để khởi tạo một repo mới dùng lệnh:
```bash
git init
```
  Git sẽ tự tạo một thư mục ```.git``` ở thư mục hiện tại

  Để Clone một git repo có sẵn, sử dụng lệnh:
```bash
git clone <repo url>
```

  Trong đó ```repo url``` có định dạng: ```git@HOSTNAME:USERNAME/REPONAME.git ```

  Khi sử dụng lệnh ```git clone```, Git sẽ tự động cấu hình remoete URL là URL của repo bạn đã clone từ đó.


  #### Git init

  Lệnh ```git init``` dùng để khởi tạo một repo mới. Khi chạy sẽ tạo ra một folder ```.git``` ở thư mục hiện tại. Thư mục này chứa toàn bộ metadata của repository.

#### Git clone
  Lệnh ```git clone``` sẽ sao chép một repo khác.
  Theo mặc định, lênh này sẽ tạo một remote connnection tên là 'origin' trỏ về chính repo được clone.

#### Git config
  Lệnh này dùng để cấu hình cho git.

  ```git config --local```: Để cấu hình cho git ở local của repo thôi. Mặc định gõ ```git config ``` mà không thêm gì thì sẽ là cấu hình local.

  ```git config --global```: Để cấu hình cho người dùng cụ thể. Tức là cấu hình ở mức người dùng.

  ```git config --system```: Để cấu hình cho toàn bộ hệ thống, áp dụng cho toàn bộ người dùng và toàn bộ repo.

Ví dụ cấu hình trình editor bằng ```git config```:
```bash
~ git config --global core.editor "'c:/program files/sublime text 3/sublimetext.exe' -w"~
```
Ví dụ cấu hình Merge tool: Xem sự khác nhau của file
```bash
git config --global merge.tool kdiff3
```
Ví dụ về cấu hình color:
```bash
git config --global color.ui false
git config --global color.branch
git config --global color.diff
git config --global color.decorate.
git config --global color.grep
git config --global color.pager
git config --global color.status
```
Ví dụ về cấu hình config alias:
```bash
git config --global alias.ci commit
```

#### Git add
```git add``` để báo cho Git biết rằng bạn muốn thêm file vào stage area của Git. Git cần theo dõi file này. Và các lần ```commit``` tiếp theo thì hãy thêm file này vô. ```git add``` không ảnh hưởng đến repo. Repo chỉ thực sự được cập nhật khi gõ ```git commit```.

Hai lệnh ```git add``` và ```git commit``` là các lệnh cơ bản để ghi lại lịch sử thay đổi của code.

Thay vì mỗi lần sửa file gì thì cần commit vào dự án. ```git add``` thêm nhiều sự thay đổi vào một logic, sau đó commit một lần thôi.

#### Git commit
```git commit``` dùng để lưu lại những gì đã ở stage vào repo. Lệnh này sẽ chạy sau lệnh ```git add```.

Commit ghi lại trạng thái của repo tại một thời điểm nào đó. 
Git ghi lại nội dung của từng file trong mỗi lần commit.

Câu lệnh:
```bash
git commit -m "noi dung commit"

#Lệnh này commit toàn bộ các file đã được tracked và các file đó có sự thay đổi.
git commit -a
```

Một số quy tắt viết message cho commit:
- Tách tiêu đề với phần thân của nội dung commit bằng một dòng trắng
- Tiêu đề giới hạn 50 ký tự
- Viết hoa chữ cái đầu ở dòng tiêu đề
- Không kết thúc tiêu đề bằng dấu chấm
- Sử dụng câu mệnh lệnh trong tiêu đề
- Giới hạn 72 ký tự mỗi dòng ở phần thân của nội dung commit
- Trả lời câu hỏi điều gì, tại sao và như thế nào ở phần thân của nội dung commit

Cách sửa nội dung 1 commit:
```bash
git commit --amend
```

#### Git diff
Lệnh ```git diff``` để so sánh những thay đổi với file đã được tracked trước đó.


