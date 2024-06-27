+++
title = 'Bài 1: Biến'
date = 2024-06-21T13:48:36+07:00
draft = false
tags = ["Cơ bản"]
categories = ["Python cơ bản cho người mới bắt đầu"]
+++

Cùng tìm hiểu về cách sử dụng biến trong Python

<!--more-->

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

Khi ta viết các chương trình của mình, code editor sẽ làm nổi bật các phần khác nhau của chương trình theo các màu khác nhau. Ví dụ, nó nhận ra rằng `print` là tên của một hàm, phần đóng mở ngoặc đơn và phần văn bản để hiển thị ra màn hình được hiển thị theo 3 màu khác nhau. Chức năng này được gọi là `syntax highlighting` và rất hữu ích trong việc lập trình.

## Biến

Hãy thử sử dụng một biến (`variable`) trong file `hello_world.py`. Thêm một dòng mới vào đầu tệp và chỉnh sửa dòng thứ hai như sau:

```python
message = "Hello Pythonista!"
print(message)
```

Chạy chương trình mới để xem điều gì xảy ra, ta có thể thấy dòng chữ `Hello Pythonista!` vẫn được in ra màn hình như ban đầu.

```bash
Hello Pythonista!
```

Chúng ta đã thêm một biến có tên là `message`. Mỗi biến đều được gán với một giá trị. Trong toán học, khi chúng ta viết `a = b` có nghĩa là giá trị của `a` và `b` bằng nhau. Nhưng trong lập trình nói chung và lập trình Python nói riêng. Việc viết `a = b` có nghĩa là giá trị `b` được gán cho biến `a`. Trong trường hợp này, biến `message` được gán giá trị là đoạn văn bản `Hello Pythonista!`.

Thêm một biến làm cho trình thông dịch Python phải làm thêm một chút công việc. Khi xử lý dòng đầu tiên, nó gán cho biến `message` với giá trị là đoạn văn bản `Hello Pythonista!`. Khi đến dòng thứ 2, nó in giá trị của biến `message` ra màn hình.

Hãy mở rộng chương trình này bằng cách sửa đổi `hello_world.py` để in một thông báo thứ 2. Thêm code mới cho `hello_world.py` ở dòng 3 và 4:

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

## Gán đa giá trị

Trong Python, ta có thể sử dụng kỹ thuật gán đa giá trị (`multiple assignment`). Điều này cho phép ta gán giá trị cho nhiều biến chỉ trong một dòng lệnh duy nhất.

Kỹ thuật này giúp rút ngắn chương trình và làm cho mã nguồn dễ đọc hơn. Ta thường sử dụng phương pháp này khi cần khởi tạo một tập hợp các số.

```python
user_name, user_age, user_salary = "Pythonista", 25, 12000000
print(user_name)  # Pythonista
print(user_age)  # 25
print(user_salary)  # 12000000
```

Dòng 1 ở code trên sẽ tương đương với việc viết 3 dòng riêng biệt

```python
user_name = "Pythonista"
user_age = 25
user_salary = 12000000
```

Nhưng nó ngắn gọn và hiệu quả hơn nhiều. Kỹ thuật gán đa giá trị không chỉ giúp code trở nên sạch sẽ hơn mà còn làm tăng tính rõ ràng của chương trình, đặc biệt khi ta cần khởi tạo nhiều biến cùng một lúc.


## Hằng số

Một hằng số (`constant`) giống như một biến, nhưng giá trị của nó không thay đổi trong suốt thời gian chạy của chương trình. Python không có kiểu hằng số được tích hợp sẵn, nhưng các lập trình viên Python thường sử dụng chữ in hoa để chỉ ra rằng một biến nên được xem như một hằng số và không bao giờ nên thay đổi giá trị của nó.

```python
PI = 3.141592654
```
