
Bài học: https://youtu.be/mAFoROnOfHs?si=7JVr3I2Fea4BEiiW 
Kho chứa mã lệnh Git: https://share.google/Xm9FW5nkBkSg7Y4mS
## Chưa phân loai: 

Xem phiên bản Git mình đang sử dụng: 

```git
git --version
```

Để đóng cửa số git bash sử dụng lệnh: 
```git
exit
```

Để dọn các lệnh trong cửa sổ ta cần sử dụng lệnh:
```git
clear 
```

## Cài đặt :

1.  Chỉ định tên (name) 
```git
git config --global user.name "my_name"
```

2. Email 
```git
git config --global user.mail "my_email"
```

trong đó: 
+ global : . . . 

Ngoài ra còn có thể thay global thành: 
+ system : . . . 
+ local : . . .

Nếu như quên mất user.name và user.mail, ta chỉ cần sử dụng lệnh sau: 
+ Đối với user.name
```git
git config user.name
```
+ Đối với user.mail
```git
git config user.mail
```


3.  Trình soạn thảo mặc định (Default Editor)

Đối với tôi trong bài học này là đưa về VSC
```git
code
```

Thiết lập trình soạn thảo mặc định bằng lệnh: 
```git
git global --config core.editor "code --wait"
```

Mở trình soạn thảo mặc định mà ta đã thiết lập trên: 
```git
git global --config -e 
```

4.  Cách nó xử kí kết thúc dòng (Line Ending)

(vẫn chưa hiểu mục đích lắm)

---
## Creating local a project and file: 

+ Chuyển đến thư mục trong máy tính bằng lệnh terminal
```git
cd <tên thư mục>
```

+ Tạo thư mục con trong thư mục mà mình chuyển đến để lưu trữ thư mục con bằng lệnh terminal 
```git
mkdir <đặt tên thư mục>
```

Sau đó ta có thể tiếp tục trỏ đến thư mục con mà mình mới tạo để lưu trữ các file hoặc folder con nữa. 

Muốn quay lại thư mục ta chỉ cần gõ lệnh `cd` và thêm hai dấu hai chấm là được: 
```git
cd ..
```

Để cho git bắt đầu giám sát mọi thứ bên trong thư mục con mà mình khởi tạo ban đầu, tôi phải cho Git biết đây là thư mục dự án của tôi để theo dõi các thay đổi. Để làm được điều này hãy chắc chắn tôi đang ở thư mục mà tôi muốn git giám sát và cần sử dụng lệnh sau:
```git
git init 
```

# Cloning Repository: 

Tạo một dự án mới (new repository)

Copy link HTTPS ở local 

Sử dụng lệnh sau để kế nối với github: 
```git
git clone <dán link từ HTTPS ở github> 
```

Hiển thị danh sách các file, folder: 
```git
ls
```

Hiển thị danh sách các file ẩn: 
```git
ls -a 
```

Nếu có thay đổi các file git sẽ biết điều đó và nếu ta muốn xem các file đã thay đổi, ta sử dụng lệnh 
```git
git status 
```

nhưng trước đó hãy sử dụng lệnh
```git
git add --all 
```

để cho git biết những file mà mình đã chỉnh sửa hoặc thêm vào sau đó mới sử dụng lệnh `git status`. 

Sử dụng lệnh sau để commit các file, folder đã sửa hoặc thêm vào thư mục con được `git init`: 
```git 
git commit -m "write something bla bla"
```

Để xóa các file ta sử dụng lệnh: 
```git
git rm <tên file> 
```

Để xóa folder ta sử dụng lệnh:
```git
git rm -r folder_name/
```

Sau khi commit và status một lần nữa, để đẩy dự án lên kho Github ta sử dụng lệnh sau: 
```git 
git push origin <branches> 
```

Ví dụ dự án thông thường sẽ đẩy branches có tên là main, thì lúc này lệnh sẽ là: 
```git
git push origin main
```

Nếu ta có branches khác thì để tên khác nhóe. 


Để xem được lịch sử `commit` sử dụng lệnh: 
```git
git log
```

Để xem được lịch sử `commit` một cách ngắn gọn sử dụng lệnh: 
```git
git log --oneline 
```

# Branch: 

Để xem được số branch có trong repository ta sử dụng lệnh: 
```git
git branch
```

Để tạo một branch mới trong repository ta sử dụng lệnh
```git
git checkout -c <name>
```

hoặc 
```git
git checkout -b <name>
```

Để chuyển sang các branch khác để làm việc trong cùng repository ta sử dụng lệnh: 
```git
git checkout <name> 
```

 Lúc này các thao tác như thêm, chỉnh sửa folder cũng như file được thực hiện tương tự khi làm việc ở branch main. 

Để xóa branch ta sử dụng lệnh sau: 
```git
git branch -D <name>
```

