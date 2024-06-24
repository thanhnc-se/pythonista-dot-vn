+++
title = 'Bài 1: Biến và kiểu dữ liệu'
date = 2024-06-21T13:48:36+07:00
draft = false
+++

## Điều gì xảy ra khi ta chạy chương trình Python :thinking:

Đầu tiên, chúng ta tạo file `hello_world.py` có nội dung như sau:

```python
print("Hello Pythonista!")
```

Khi chạy chương trình, ta sẽ thấy nội dung sau được in ra màn hình:

```bash
Hello Pythonista!
```

Dựa vào phần đuôi `.py` cho biết rằng file này là một chương trình Python. Trình soạn thảo code của chúng ta (`VSCode, Pycharm,...` sau này mình sẽ gọi là Code Editor) sẽ sử dụng `trình thông dịch Python` để chạy file này. Trình thông dịch sẽ đọc qua chương trình và xác định ý nghĩa của từng từ trong chương trình. Ví dụ, khi trình thông dịch nhìn thấy từ `print` theo sau bởi dấu ngoặc đơn `()`, nó sẽ in ra màn hình bất kỳ thứ gì nằm trong dấu ngoặc đơn.

Khi ta viết các chương trình của mình, code editor sẽ làm nổi bật các phần khác nhau của chương trình theo các màu khác nhau. Ví dụ, nó nhận ra rằng `print` là tên của một hàm, phần đóng / mở ngoặc đơn và phần văn bản để hiển thị ra màn hình được hiển thị theo 3 màu khác nhau. Chức năng này được gọi là `syntax highlighting` và rất hữu ích trong việc lập trình.

## Biến

Hãy thử sử dụng một biến trong file `hello_world.py`. Thêm một dòng mới vào đầu tệp và chỉnh sửa dòng thứ hai như sau:

```python
message = "Hello Pythonista!"
print(message)
```

Chạy chương trình mới để xem điều gì xảy ra. Dòng chữ `Hello Python world!` vẫn được in ra màn hình như ban đầu

```bash
Hello Pythonista!
```

Chúng ta đã thêm một biến có tên là `message`. Mỗi biến đều được gán với một giá trị, đó là thông tin liên quan đến biến đó. Trong toán học, khi chúng ta viết `a = b` có nghĩa là giá trị của `a` và `b` bằng nhau. Nhưng trong lập trình nói chung và lập trình Python nói riêng. Việc viết `a = b` có nghĩa là giá trị `b` được gán cho biến `a`. Trong trường hợp này, biến `message` được gán giá trị là đoạn văn bản `Hello Python world!`.

Thêm một biến làm cho trình thông dịch Python phải làm thêm một chút công việc. Khi xử lý dòng đầu tiên, nó gán cho biến `message` với giá trị là đoạn văn bản `Hello Python world!`. Khi nó đến dòng thứ 2, nó in giá trị của biến `message` ra màn hình.

Hãy mở rộng chương trình này bằng cách sửa đổi hello_world.py để in một thông báo thứ hai. Thêm code mới cho `hello_world.py` ở dòng 3 và 4:

```python
message = "Hello Pythonista!"
print(message)
message = "Hoàng Sa, Trường Sa là của Việt Nam!"
print(message)
```

Bây giờ, khi chạy chương trình, ta sẽ thấy 2 dòng chữ được in ra màn hình:

```bash
Hello Pythonista!
Hoàng Sa, Trường Sa là của Việt Nam!
```

Ta có thể thay đổi giá trị của một biến trong chương trình bất cứ lúc nào, và Python sẽ luôn dõi theo giá trị hiện tại của biến.

Khi sử dụng biến trong python, chúng ta phải tuân thủ một vài quy tắc, nếu vi phạm quy tắc này, chương trình của ta sẽ bị lỗi. Các quy tắc mà chúng ta cần nhớ là:

- Tên biến trong Python có thể chứa chỉ các chữ cái, số và dấu gạch dưới `_`. Có thể bắt đầu bằng một chữ cái hoặc dấu gạch dưới, nhưng không bắt đầu bằng một số. Ví dụ: ta có thể đặt tên biến là `message_2` nhưng không thể đặt tên là `2_message`
- Không được phép có khoảng trắng trong tên biến, nhưng có thể sử dụng dấu gạch dưới để ngăn cách các từ trong tên biến. Ví dụ, `greeting_message` hoạt động được, nhưng `greeting message` sẽ gây ra lỗi.
- Tránh sử dụng các từ khóa và tên hàm của Python làm tên biến. Nghĩa là không sử dụng những từ mà Python đã dành riêng cho một mục đích lập trình cụ thể, chẳng hạn như từ `print`.
- Tên biến nên ngắn gọn nhưng mang tính mô tả. Ví dụ, `name` tốt hơn `n`, `student_name` tốt hơn `s_n`, và `name_length` tốt hơn `length_of_persons_name`.

Việc học cách tạo ra những tên biến một cách phù hợp có thể cần một chút thực hành, đặc biệt là khi các chương trình của bạn trở nên dài và phức tạp hơn. Khi bạn đã làm quen với việc code và bắt đầu đọc qua code của người khác, bạn sẽ trở nên giỏi hơn trong việc đặt những cái tên có ý nghĩa.


## Chú thích

Chú thích (hay còn gọi là `comment`) là những dòng chú thích trong code mà `trình thông dịch sẽ bỏ qua` khi chạy chương trình, chú thích thường được dùng để:
- Giải thích code cho bạn bè, đồng nghiệp hoặc cho chính mình (1 tháng sau đọc lại chưa chắc bạn đã hiểu mình viết gì :joy:).
- Note lại ý tưởng.
- Tạm thời vô hiệu hóa một đoạn code.

Có 2 cách để sử dụng comment trong Python:
- Comment 1 dòng: Sử dụng ký tự `#`, Python sẽ vô hiệu hóa từ dấu `#` cho đến hết dòng đó.
- Comment nhiều dòng: Sử dụng 3 dấu nháy đơn `'''` hoặc 3 dấu nháy kép `"""` ở đầu và cuối đoạn comment.

```python
# Đây là một comment một dòng
print("Hello World")  # Comment có thể đặt sau code

'''
Đây là một comment
trên nhiều dòng
'''

print("Hello World")

"""
Đây cũng là một comment
trên nhiều dòng
"""
```

{{< admonition type=note open=true >}}
Từ giờ mình sẽ sử dụng **comment** để giải thích cũng như thể hiện giá trị in ra màn hình của các hàm **print** trong các đoạn code mẫu :ok_hand:
{{< /admonition >}}

## Kiểu dữ liệu String

Bởi vì hầu hết các chương trình đều định nghĩa và thu thập một số loại dữ liệu, và sau đó thực hiện tính toán và biến đổi dữ liệu để chương trình trở nên có ích. Dữ liệu trong lập trình là rất quan trọng, nên để đảm bảo dữ liệu được xử lý đúng cách, chúng cần được chia thành các loại khác nhau gọi là kiểu dữ liệu. Kiểu dữ liệu đầu tiên chúng ta sẽ xem xét là `chuỗi` hay còn gọi là `string`. Chuỗi khá đơn giản, nhưng bạn có thể sử dụng chúng theo nhiều cách khác nhau.

Một chuỗi là một dãy các ký tự. Bất cứ thứ gì bên trong dấu ngoặc kép `"` hoặc cặp dấu ngoặc đơn `'` đều được coi là một chuỗi trong Python.

```python
"Đây là string"
'Đây cũng là string'
```

### Thay đổi chữ hoa - chữ thường trong chuỗi bằng phương thức

Mình có một message như sau:

```python
message = "LeArN pYtHoN wItH pYtHoNiStA"
```

Giả sử, mình muốn tất cả các ký tự trong `message` đều viết thường, mình chỉ cần dùng phương thức `lower` rồi gán giá trị sau khi đã biến đổi cho một biến mới `lower_case_message`

```python
message = "LeArN pYtHoN wItH pYtHoNiStA"
lower_case_message = message.lower()
print(lower_case_message)  # learn python with pythonista
```

Một phương thức là một hành động mà Python có thể thực hiện trên một loại dữ liệu. Dấu chấm `.` sau `message` trong `message.lower()` cho Python biết ta muốn sử dụng phương thức `lower` lên biến `message`. Sau tên của phương thức là một cặp mở / đóng ngoặc đơn `()` vì thông thường ta phải cung cấp thêm thông tin vào bên trong dấu ngoặc đơn để phương thức có thể thực hiện công việc. Nhưng trong trường hợp này, phương thức `lower` không cần thêm bất cứ thông tin gì, nên bên trong dấu ngoặc đơn được bỏ trống.

Hoặc ta cũng có thể sử dụng lại biến `message`

```python
message = "LeArN pYtHoN wItH pYtHoNiStA"
message = message.lower()
print(message)  # learn python with pythonista
```

Giả sử chúng ta muốn viết một chương trình trong đó người dùng có thể nhập họ và tên của họ, nhưng chúng ta đâu thể đảm bảo được rằng người dùng viết tên đúng định dạng phải không nào? Họ và tên muốn đùng thì phải đảm bảo được rằng ở mỗi từ, chữ cái đầu tiên luôn được viết hoa, các chữ cái còn lại sẽ được viết thường. Rất may là Python đã hỗ trợ sẵn cho chúng ta một phương thức để thực hiện việc đó :muscle:, chính là `title`.

```python
full_name = "nguyễn công thành"
full_name = full_name.title()
print(full_name)  # Nguyễn Công Thành
```

Còn nếu muốn tất cả các từ đều in hoa, chúng ta có thể sử dụng phương thức `upper`

```python
full_name = "nguyễn công thành"
full_name = full_name.upper()
print(full_name)  # NGUYỄN CÔNG THÀNH
```

### Sử dụng biến trong string

Trong một số tình huống, chúng ta sẽ muốn sử dụng giá trị của một biến bên trong một chuỗi. Ví dụ, ta có thể muốn hai biến để đại diện cho tên và họ, và sau đó muốn kết hợp những giá trị đó để hiển thị tên đầy đủ của ai đó

```python
first_name = "Thành"
last_name = "Nguyễn"
full_name = f"{first_name} {last_name}"
print(full_name)  # Thành Nguyễn
```

Để chèn giá trị của một biến vào chuỗi, ta đặt chữ f ngay trước dấu ngoặc kép. Đặt dấu ngoặc nhọn xung quanh tên của bất kỳ biến nào mà ta muốn sử dụng bên trong chuỗi. Python sẽ thay thế mỗi biến bằng giá trị của nó khi chuỗi được hiển thị.

Những chuỗi này được gọi là `f-strings`. Chữ f là viết tắt của format (định dạng), bởi vì Python định dạng chuỗi bằng cách thay thế tên của bất kỳ biến nào trong dấu ngoặc nhọn bằng giá trị của nó.
