+++
title = 'Bài 1: Biến và kiểu dữ liệu'
date = 2024-06-21T13:48:36+07:00
draft = false
+++

## Điều gì xảy ra khi ta chạy chương trình Python ?

Khi ta chạy file `hello_world.py` có nội dung như sau:

{{< highlight python >}}
print("Hello Python world!")
{{< /highlight >}}

Ta sẽ thấy nội dung sau được in ra màn hình:

{{< highlight bash >}}
Hello Python world!
{{< /highlight >}}

Dựa vào phần đuôi `.py` cho biết rằng tệp này là một chương trình Python. Trình soạn thảo code của chúng ta sau đó sẽ chạy tệp qua `trình thông dịch Python`, trình thông dịch này sẽ đọc qua chương trình và xác định ý nghĩa của từng từ trong chương trình. Ví dụ, khi trình thông dịch nhìn thấy từ `print` theo sau bởi dấu ngoặc đơn `()`, nó sẽ in ra màn hình bất kỳ thứ gì nằm trong dấu ngoặc đơn.

Khi ta viết các chương trình của mình, trình soạn thảo văn bản sẽ làm nổi bật các phần khác nhau của chương trình theo các cách khác nhau. Ví dụ, nó nhận ra rằng `print()` là tên của một hàm và hiển thị từ đó bằng màu sắc khác. Nó nhận ra rằng `"Hello Python world!"` không phải là mã Python và hiển thị cụm từ đó bằng một màu sắc khác so với print. Tính năng này được gọi là `syntax highlighting` và rất hữu ích khi ta bắt đầu viết các chương trình của riêng mình.

## Biến

Hãy thử sử dụng một biến trong file `hello_world.py`. Thêm một dòng mới vào đầu tệp và chỉnh sửa dòng thứ hai như sau:

{{< highlight python >}}
message = "Hello Python world!"
print(message)
{{< /highlight >}}

Chạy chương trình mới để xem điều gì xảy ra. Dòng chữ `Hello Python world!` vẫn được in ra màn hình như ban đầu

{{< highlight bash >}}
Hello Python world!
{{< /highlight >}}

Chúng ta đã thêm một biến có tên là `message`. Mỗi biến đều được gán với một giá trị, đó là thông tin liên quan đến biến đó. Trong trường hợp này, giá trị là đoạn văn bản `Hello Python world!`.

Thêm một biến làm cho trình thông dịch Python phải làm thêm một chút công việc. Khi xử lý dòng đầu tiên, nó gán cho biến `message` với giá trị là đoạn văn bản `Hello Python world!`. Khi nó đến dòng thứ hai, nó in giá trị của biến `message` ra màn hình.

Hãy mở rộng chương trình này bằng cách sửa đổi hello_world.py để in một thông báo thứ hai. Thêm code mới cho `hello_world.py` ở dòng 3 và 4:

{{< highlight python >}}
message = "Hello Python world!"
print(message)
message = "Hello Pythonista!"
print(message)
{{< /highlight >}}

Bây giờ, khi chạy chương trình, ta sẽ thấy 2 dòng chữ được in ra màn hình:

{{< highlight bash >}}
Hello Python world!
Hello Pythonista!
{{< /highlight >}}

Ta có thể thay đổi giá trị của một biến trong chương trình bất cứ lúc nào, và Python sẽ luôn dõi theo giá trị hiện tại của biến.

### Đặt tên và sử dụng biến

Khi sử dụng biến trong python, chúng ta phải tuân thủ một vài quy tắc, nếu vi phạm quy tắc này, chương trình của ta sẽ bị lỗi. Các quy tắc mà chúng ta cần nhớ là:

- Tên biến trong Python có thể chứa chỉ các chữ cái, số và dấu gạch dưới `_`. Có thể bắt đầu bằng một chữ cái hoặc dấu gạch dưới, nhưng không bắt đầu bằng một số. Ví dụ: ta có thể đặt tên biến là `message_2` nhưng không thể đặt tên là `2_message`
- Không được phép có khoảng trắng trong tên biến, nhưng có thể sử dụng dấu gạch dưới để ngăn cách các từ trong tên biến. Ví dụ, `greeting_message` hoạt động được, nhưng `greeting message` sẽ gây ra lỗi.
- Tránh sử dụng các từ khóa và tên hàm của Python làm tên biến. Nghĩa là không sử dụng những từ mà Python đã dành riêng cho một mục đích lập trình cụ thể, chẳng hạn như từ `print`.
- Tên biến nên ngắn gọn nhưng mang tính mô tả. Ví dụ, `name` tốt hơn `n`, `student_name` tốt hơn `s_n`, và `name_length` tốt hơn `length_of_persons_name`.

Việc học cách tạo ra những tên biến tốt có thể cần một chút thực hành, đặc biệt là khi các chương trình của bạn trở nên thú vị và phức tạp hơn. Khi bạn viết nhiều chương trình hơn và bắt đầu đọc qua code của người khác, bạn sẽ trở nên giỏi hơn trong việc đặt những cái tên có ý nghĩa.

### Tránh viết nhầm tên khi sử dụng biến

Khi lập trình, ai cũng có thể mắc lỗi. Người lập trình viên giỏi là người biết cách phát hiện ra lỗi và khắc phục lỗi một cách hiệu quả. Bây giờ, chúng ta sẽ tạo ra lỗi một cách có chủ đích:

{{< highlight python >}}
message = "Hello Python world!"
print(mesage)
{{< /highlight >}}
