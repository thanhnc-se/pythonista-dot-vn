+++
title = 'Bài 2: Kiểu dữ liệu chuỗi'
date = 2024-06-21T15:48:36+07:00
draft = false
tags = ["Cơ bản"]
categories = ["Python cơ bản cho người mới bắt đầu"]
+++

Cùng tìm hiểu về cách sử dụng kiểu dữ liệu chuỗi trong Python

<!--more-->

Bởi vì hầu hết các chương trình đều định nghĩa và thu thập một số loại dữ liệu, và sau đó thực hiện tính toán và biến đổi dữ liệu để chương trình trở nên có ích. Dữ liệu trong lập trình là rất quan trọng, nên để đảm bảo dữ liệu được xử lý đúng cách, chúng cần được chia thành các loại khác nhau gọi là kiểu dữ liệu. Kiểu dữ liệu đầu tiên chúng ta sẽ xem xét là `chuỗi` hay còn gọi là `string`. Chuỗi khá đơn giản, nhưng bạn có thể sử dụng chúng theo nhiều cách khác nhau.

Một chuỗi là một dãy các ký tự. Bất cứ thứ gì bên trong dấu ngoặc kép `"` hoặc cặp dấu ngoặc đơn `'` đều được coi là một chuỗi trong Python.

```python
"Đây là string"
'Đây cũng là string'
```

## Thay đổi chữ hoa - chữ thường trong chuỗi bằng phương thức

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

## Sử dụng biến trong string

Trong một số tình huống, chúng ta sẽ muốn sử dụng giá trị của một biến bên trong một chuỗi. Ví dụ, ta có thể muốn hai biến để đại diện cho tên và họ, và sau đó muốn kết hợp những giá trị đó để hiển thị tên đầy đủ của ai đó

```python
first_name = "thành"
last_name = "nguyễn"
full_name = f"{first_name} {last_name}"
print(full_name)  # thành nguyễn
```

Để chèn giá trị của một biến vào chuỗi, ta đặt chữ f ngay trước dấu ngoặc kép (dòng 3). Đặt dấu ngoặc nhọn xung quanh tên của bất kỳ biến nào mà ta muốn sử dụng bên trong chuỗi. Python sẽ thay thế mỗi biến bằng giá trị của nó khi chuỗi được hiển thị.

Những chuỗi này được gọi là `f-strings`. Chữ f là viết tắt của format (định dạng), bởi vì Python định dạng chuỗi bằng cách thay thế tên của bất kỳ biến nào trong dấu ngoặc nhọn bằng giá trị của nó.

Chúng ta có thể làm được nhiều điều thú vị với `f-string` trong Python. Ví dụ, ta có thể sử dụng `f-string` để tạo ra những thông điệp hoàn chỉnh bằng cách kết hợp thông tin từ các biến. Cùng xem ví dụ sau đây để hiểu rõ hơn về cách áp dùng `f-string` một cách hiệu quả:

```python
first_name = "thành"
last_name = "nguyễn"
full_name = f"{first_name} {last_name}"
print(f"Hello {full_name.title()}")  # Hello Thành Nguyễn
```
Trong đoạn này, ta sử dụng `full_name` để tạo ra một thông điệp chào người dùng, và phương thức `title()` được áp dụng để chuyển đổi tên thành dạng viết hoa chữ cái đầu của mỗi từ. Kết quả là ta có được một lời chào được định dạng một cách đẹp mắt.

## Thêm khoảng trắng trong string bằng tab và xuống dòng

Trong lập trình, khoảng trắng bao gồm `các ký tự không in ra được` như `dấu cách`, `tab` hay ký hiệu `xuống dòng`. Chúng ta có thể sử dụng các loại khoảng trắng để định dạng được in ra màn hình trở nên dễ đọc hơn.

Để thêm `tab` vào đoạn văn bản, ta chỉ cần thêm 2 ký tự `\t` như sau:

```python
print("Hello\tPythonista")  # Hello    Pythonista
```

Để thêm ký tự xuống dòng vào đoạn văn bản, ta thêm `\n`:

```python
print("Languages:\nPython\nC\nJavaScript")
# Languages:
# Python
# C
# JavaScript
```

Ta cũng có thể kết hợp cả `tab` và `xuống dòng` trong một chuỗi bằng cách kết hợp chúng lại với nhau:

```
print("Languages:\n\tPython\n\tC\n\tJavaScript")
# Languages:
#     Python
#     C
#     JavaScript
```

## Loại bỏ khoảng trắng

Trong nhiều trường hợp, các chuỗi có thể chứa các khoảng trắng thừa ở đâu, cuối hoặc cả 2 đầu. Những khoảng trắng này có thể gây ra các vấn đề không mong muốn trong quá trình xử lý dữ liệu.

Ta có thể sử dụng các phương thức như `strip()`, `lstrip()`, `rstrip()` để loại bỏ khoảng trắng không cần thiết. Phương thức `strip()` sẽ xóa cả khoảng trắng ở đầu và cuối chuỗi, `lstrip()` chỉ xóa ở đầu, còn `rstrip()` chỉ xóa ở cuối.

Việc loại bỏ khoảng trắng này giúp ta chuẩn hóa dữ liệu, tránh các lỗi so sánh chuỗi và làm cho việc xử lý dữ liệu trở nên đáng tin cậy hơn.

```python
text = "  Python programming  "
print(f".{text.strip()}.")  # .Python programming.
print(f".{text.ltrip()}.")  # .Python programming  .
print(f".{text.rtrip()}.")  # .  Python programming.
```

## Các phương thức được tích hợp sẵn

Python có một tập hợp các phương thức tích hợp sẵn mà ta có thể sử dụng trên các chuỗi.

{{< admonition title="Lưu ý" type=note open=true >}}
Tất cả các phương thức chuỗi đều trả về giá trị mới. Chúng không thay đổi chuỗi gốc.
{{< /admonition >}}

| Phương thức | Mô tả |
|---|---|
| capitalize | Chuyển ký tự đầu tiên thành chữ hoa |
| casefold | Chuyển chuỗi thành chữ thường (mạnh hơn lower()) |
| center | Căn giữa chuỗi trong một khoảng trống |
| count | Đếm số lần xuất hiện của một chuỗi con |
| encode | Mã hóa chuỗi |
| endswith | Kiểm tra xem chuỗi có kết thúc bằng chuỗi con không |
| expandtabs | Thay thế tab bằng khoảng trắng |
| find | Tìm vị trí đầu tiên của chuỗi con |
| format | Định dạng chuỗi |
| format_map | Định dạng chuỗi sử dụng dictionary |
| index | Tìm vị trí đầu tiên của chuỗi con (giống find nhưng ném ra ngoại lệ nếu không tìm thấy) |
| isalpha | Kiểm tra xem tất cả các ký tự có phải là chữ cái không |
| isascii | Kiểm tra xem tất cả các ký tự có phải là ASCII không |
| isdecimal | Kiểm tra xem tất cả các ký tự có phải là số thập phân không |
| isdigit | Kiểm tra xem tất cả các ký tự có phải là chữ số không |
| isidentifier | Kiểm tra xem chuỗi có phải là một định danh hợp lệ không |
| islower | Kiểm tra xem tất cả các ký tự có phải là chữ thường không |
| isnumeric | Kiểm tra xem tất cả các ký tự có phải là số không |
| isprintable | Kiểm tra xem tất cả các ký tự có thể in được không |
| isspace | Kiểm tra xem tất cả các ký tự có phải là khoảng trắng không |
| istitle | Kiểm tra xem chuỗi có phải là dạng title không |
| isupper | Kiểm tra xem tất cả các ký tự có phải là chữ hoa không |
| join | Nối các phần tử của một iterable thành một chuỗi |
| ljust | Căn trái chuỗi trong một khoảng trống |
| lower | Chuyển chuỗi thành chữ thường |
| lstrip | Xóa khoảng trắng bên trái của chuỗi |
| maketrans | Tạo bảng dịch để sử dụng trong phương thức translate() |
| partition | Tách chuỗi thành 3 phần |
| replace | Thay thế một chuỗi con bằng một chuỗi khác |
| rfind | Tìm vị trí cuối cùng của chuỗi con |
| rindex | Tìm vị trí cuối cùng của chuỗi con (giống rfind nhưng ném ra ngoại lệ nếu không tìm thấy) |
| rjust | Căn phải chuỗi trong một khoảng trống |
| rpartition | Tách chuỗi thành 3 phần, bắt đầu từ bên phải |
| rsplit | Tách chuỗi thành một danh sách, bắt đầu từ bên phải |
| rstrip | Xóa khoảng trắng bên phải của chuỗi |
| split | Tách chuỗi thành một danh sách |
| splitlines | Tách chuỗi tại các dòng mới và trả về danh sách |
| startswith | Kiểm tra xem chuỗi có bắt đầu bằng chuỗi con không |
| strip | Xóa khoảng trắng ở đầu và cuối chuỗi |
| swapcase | Đổi chữ hoa thành chữ thường và ngược lại |
| title | Chuyển ký tự đầu tiên của mỗi từ thành chữ hoa |
| translate | Dịch chuỗi theo bảng dịch |
| upper | Chuyển chuỗi thành chữ hoa |
| zfill | Thêm số 0 vào đầu chuỗi cho đến khi đạt độ dài chỉ định |