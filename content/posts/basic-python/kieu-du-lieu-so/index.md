+++
title = 'Bài 3: Kiểu dữ liệu số'
date = 2024-06-21T17:48:36+07:00
draft = false
tags = ["Cơ bản"]
categories = ["Python cơ bản cho người mới bắt đầu"]
+++

Cùng tìm hiểu về cách sử dụng kiểu dữ liệu số trong Python

<!--more-->

Trong lập trình số được sử dụng rất phổ biến, có thể kể đến như lưu điểm trong trò chơi, biểu diễn dữ liệu trên biểu đồ, lưu trữ thông tin trong ứng dụng web và nhiều mục đích khác.

Python xử lý số theo nhiều cách khác nhau, tùy thuộc vào các chúng được sử dụng. Trước hết, ta hãy xem xét cách Python quản lý `số nguyên`, bởi vì chúng là loại số đơn giản nhất để làm việc.

## Số nguyên

Số nguyên trong tiếng Anh là `integer` hay thường được viết tắt là `int`. Ta có thể thực hiện thể cộng `+`, trừ `-`, nhân `*`, chia `/` hay lũy thừa `**` các số nguyên trong Python.

```python
print(3 + 4)  # 7
print(3 - 4)  # -1
print(3 * 4)  # 12
print(3 / 4)  # 0.75
print(3 ** 4)  # 81
```

Python cũng hỗ trợ thứ tự thực hiện các phép toán, vì vậy ta có thể sử dụng nhiều phép tính trong một biểu thức. Ta cũng có thể dùng dấu ngoặc đơn để điều chỉnh thứ tự thực hiện theo đúng trình tự mà ta mong muốn.

```python
print(3 + 4 * 5)  # 23
print((3 + 4) * 5)  # 35
```

## Số thực

Python gọi bất kỳ số nào có phần thập phân là số thực (`float`). Thuật ngữ này được sử dụng trong hầu hết các ngôn ngữ lập trình.

Nhìn chung, ta có thể sử dụng số thập phân mà không cần quá lo lắng về cách chúng hoạt động. Ta chỉ cần nhập các số mà mình muốn sử dụng, và trong hầu hết các trường hợp, Python sẽ xử lý chúng đúng như ta mong đợi. Điều này giúp việc làm việc với số thập phân trở nên đơn giản và trực quan hơn cho người lập trình, đặc biệt là những người mới bắt đầu.

```python
print(0.1 + 0.1)  # 0.2
print(0.2 + 0.2)  # 0.4
print(2 * 0.1)  # 0.2
```

Tuy nhiên, ta cần lưu ý rằng đôi khi kết quả có thể có độ dài phần thập phân không mong muốn. Điều này xảy ra do cách máy tính biểu diễn và tính toán số thực trong bộ nhớ. Đây là một đặc điểm cần chú ý khi làm việc với số thực trong Python và các ngôn ngữ lập trình nói chung, đặc biệt là trong các tính toán đòi hỏi độ chính xác cao.

```python
print(0.2 + 0.1)  # 0.30000000000000004
print(3 * 0.1)  # 0.30000000000000004
```
Hiện tượng này xảy ra trong tất cả các ngôn ngữ lập trình và không phải là vấn đề quá đáng ngại. Hiện tại, ta có thể bỏ qua những chữ số thập phân dư thừa này. Sau này, ở các bài nâng cao hơn, mình sẽ hướng dẫn các bạn phương pháp để xử lý những số thập phân như thế này.

## Số nguyên và số thực

Khi ta chia 2 số bất kỳ cho nhau, ngay cả khi đó là các số nguyên và kết quả cũng là số nguyên, Python sẽ luôn trả về một số thực.

```python
print(8 / 4)  # 2.0
```

Khi ta kết hợp số nguyên và số thực trong bất kỳ phép toán nào, kết quả nhận được cũng là một số thực

```python
print(3 + 4.0)  # 7.0
print(3 * 4.0)  # 12.0
print(3 ** 4.0)  # 81.0
```

Ta có thể thấy, khi trong phép toán có số thực, kết quả trả về sẽ luôn là số thực, bất kể giá việc giá trị của nó có phần thập phân hay không.

## Sử dụng dấu gạch dưới trong kiểu dữ liệu số

Khi ta viết các số lớn, ta có thể sử dụng dấu gạch dưới để nhóm các chữ số lại, giúp cho những con số lớn dễ đọc hơn.

```python
salary = 12_000_000
print(salary)  # 12000000
```

Thay vì viết `12000000` (mười hai triệu) ta có thể viết `12_000_000`. Python sẽ bỏ qua các dấu gạch dưới khi xử lý số. Nhưng với người viết code và đọc code, cách này giúp dễ đọc hơn rất nhiều.
