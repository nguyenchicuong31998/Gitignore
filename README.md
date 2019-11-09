# 1. Gitignore là gì?
- Gitignore là file có tên là **.gitignore** do thằng Git quy định, nhiệm vụ của nó là liệt kê những file mà mình không mong muốn cho vào git hoặc hiểm nôm na là thằng Git sẽ lờ những file đó đi.
# 2. Cách thức hoạt động?
- Khi add 1 file mới vào git, git sẽ kiểm tra danh sách những thằng sẽ lờ đi trong file .gitignore và lờ luôn chúng nó. À đó mới chỉ là điều kiện cần, điều kiện đủ là nó không có trong git cache nữa thì thằng git nó mới lờ đi chứ nó mà nằm trong git cache thì .gitignore sẽ vô tác dụng.
# 3. Một số lệnh cơ bản của .gitignore
 - Một dòng bắt đầu bằng # có tác dụng như 1 comment chú thích.
 - 
 ## Git cached
 - Có thể hình dung ra rằng tập những file được Git parse mỗi khi có sự thay đổi đều được list ra ở trong vùng cache này để tực tiếp làm việc. Và nếu giữa chừng mà chỉ tạo, cập nhật mỗi file .gitignore thì sẽ chẳng có thay đổi nào đâu, những thứ bạn cho thêm vào sẽ vô tác dụng, bạn vẫn sẽ pull push đều đều bọn chúng lên pull request. Như vậy giri pháp ở đây sẽ là xóa file hoặc folder đó ra khỏi git cache và nó sẽ hoạt động đúng, chỉ bằng 1 dòng lệnh :
 - `git rm -r --cached /path/to/file_or_folder`
- Nếu có quá nhiều thứ bạn cần ignore mới thì chỉ cần
 - `git rm -r --cached`
- Rồi sau đó load lại toàn bộ vào như sau
- `git add`



