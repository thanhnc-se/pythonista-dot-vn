+++
title = 'Bài 4: Kiểu dữ liệu danh sách'
date = 2024-06-22T17:01:00+07:00
draft = false
tags = ["Cơ bản"]
categories = ["Python cơ bản cho người mới bắt đầu"]
+++

Cùng tìm hiểu về cách sử dụng kiểu dữ liệu danh sách trong Python

<!--more-->

Ta có thể hiểu danh sách (`list`) như một tập hợp các phần tử được sắp xếp theo thứ tự nhất định. Danh sách có thể chứa bất cứ thứ gì, từ các chữ cái trong bảng chữ cái, các số từ 0 đến 9, cho đến tên của mọi người trong gia đình,... Các phần tử trong danh sách không nhất thiết phải liên quan đến nhau.

Vì danh sách thường chứa nhiều phần tử, nên tốt nhất là đặt tên biến cho danh sách ở dạng số nhiều, ví dụ như `messages`, `numbers` hay `names`.

Trong Python, chúng ta sử dụng dấu ngoặc vuông (`[]`) để biểu thị một danh sách, và các phần tử riêng lẻ được ngăn cách bằng dấu phẩy. Sau đây là ví dụ đơn giản về 1 danh sách chứa vài loại quả.

```python
fruits = ["orange", "mango", "banana"]
print(fruits)  # ['orange', 'mango', 'banana']
```

## Truy cập vào phần tử trong danh sách

Khi ta yêu cầu Python in ra một danh sách, nó sẽ in ra giá trị của các phần tử trong danh sách, bao gồm cả dấu ngoặc vuông. Tuy nhiên, đây có thể không phải là kết quả mà ta muốn người dùng thấy.

Vì vậy, chúng ta cần học cách truy cập từng phần tử riêng lẻ trong danh sách. Danh sách là tập hợp có thứ tự, nên ta có thể truy cập bất kỳ phần tử nào thông qua `chỉ mục (index)` của nó. Để làm điều này, ta viết tên biến của danh sách, theo sau là `index` của phần tử được đặt trong dấu ngoặc vuông. Ví dụ, nếu muốn lấy ra loại quả đầu tiên trong danh sách `fruits`, ta có thể làm như sau:

```python
fruits = ["orange", "mango", "banana"]
print(fruits[0])  # orange
```

Đây là kết quả mà chúng ta muốn người dùng thấy: đầu ra sạch sẽ và được định dạng gọn gàng. Ta cũng có thể áp dụng các phương thức xử lý chuỗi đã học ở `Bài 2` cho bất kỳ phần tử nào trong danh sách này. Ví dụ, để làm cho phần tử `orange` trông đẹp mắt hơn, ta có thể sử dụng phương thức title() như sau:

```python
fruits = ["orange", "mango", "banana"]
print(fruits[0].title())  # Orange
```

{{< admonition title="Lưu ý" type=note open=true >}}
Index bắt đầu từ 0 chứ không phải 1
{{< /admonition >}}

Trong Python và hầu hết các ngôn ngữ lập trình khác, phần tử đầu tiên trong danh sách được coi là ở vị trí 0, không phải vị trí 1. Điều này liên quan đến cách thức hoạt động của danh sách ở cấp độ thấp hơn.

Phần tử thứ hai trong danh sách có index là 1. Với cách đếm này, ta có thể lấy bất kỳ phần tử nào trong danh sách bằng cách trừ 1 từ vị trí của nó. Ví dụ, để truy cập phần tử thứ 3 trong `fruits` (banana), ta sẽ dùng index 2.

```python
fruits = ["orange", "mango", "banana"]
print(fruits[2].title())  # Banana
```

Python có một cú pháp để truy cập phần tử cuối cùng trong danh sách. Khi ta truy cập phần tử ở index -1, Python sẽ luôn trả về phần tử cuối cùng:

Cách này rất hữu ích khi ta muốn truy cập các phần tử cuối danh sách mà không cần biết chính xác độ dài của nó. Quy ước này cũng áp dụng cho các chỉ mục âm khác. chỉ mục -2 sẽ trả về phần tử thứ hai từ cuối danh sách, chỉ mục -3 trả về phần tử thứ ba từ cuối, và cứ thế.

```python
fruits = ["orange", "mango", "banana"]
print(fruits[-1].title())  # Banana
```

## Sử dụng các giá trị riêng lẻ từ danh sách

Ta có thể sử dụng các giá trị riêng lẻ từ danh sách giống như cách ta sử dụng bất kỳ biến nào khác. Ví dụ, chúng ta có thể dùng `f-strings` để tạo một thông điệp dựa trên giá trị từ danh sách.

Hãy thử lấy loại quả đầu tiên từ danh sách và tạo một `message` sử dụng giá trị đó:

```python
fruits = ["orange", "mango", "banana"]
message = f"{fruits[0].title()} is my favorite fruit"
print(message)  # Orange is my favorite fruit
```

Ta đã tạo một `message` sử dụng giá trị ở `fruits[0]` và gán nó cho biến `message`. Kêt quả là một đoạn văn bản đơn giản về loại quả đầu tiên trong danh sách.

## Thay đổi, thêm và xóa phần tử

Hầu hết các danh sách ta tạo ra sẽ là động (`dynamic list`), nghĩa là ta sẽ xây dựng một danh sách và sau đó thêm hoặc xóa các phần tử khi chương trình chạy.

Ví dụ, ta có thể tạo một trò chơi mà người chơi phải bắn hạ các người ngoài hành tinh. Ta có thể lưu trữ tập hợp ban đầu của người ngoài hành tinh trong một danh sách, rồi xóa một người ngoài hành tinh khỏi danh sách mỗi khi nó bị bắn hạ. Mỗi khi một người ngoài hành tinh mới xuất hiện trên màn hình, ta thêm nó vào danh sách. Như vậy, danh sách người ngoài hành tinh sẽ tăng giảm độ dài trong suốt quá trình chơi.

### Thay đổi giá trị của phần tử

Cú pháp để thay đổi một phần tử tương tự như cú pháp để truy cập một phần tử trong danh sách. Để thay đổi một phần tử, ta sử dụng tên danh sách, theo sau là chỉ mục của phần tử muốn thay đổi, rồi cung cấp giá trị mới cho phần tử đó.

Ví dụ, giả sử ta có một danh sách các xe máy và phần tử đầu tiên trong danh sách là `"honda"`. Sau đó, ta thay đổi giá trị của phần tử đầu tiên thành `"ducati"`. Kết quả hiển thị rằng phần tử đầu tiên đã được thay đổi, trong khi phần còn lại của danh sách vẫn giữ nguyên:

```python
motorcycles = ["honda", "yamaha", "suzuki"]
print(motorcycles)  # ['honda', 'yamaha', 'suzuki']
motorcycles[0] = "ducati"
print(motorcycles)  # ['ducati', 'yamaha', 'suzuki']
```

Ta có thể thay đổi giá trị của bất kỳ phần tử nào trong danh sách, không chỉ giới hạn ở phần tử đầu tiên.

### Thêm phần tử

Có nhiều lý do khiến ta muốn thêm một phần tử mới vào danh sách. Ví dụ, ta có thể muốn tạo ra những người ngoài hành tinh mới trong trò chơi, thêm dữ liệu mới vào một biểu đồ, hoặc thêm người dùng mới đăng ký vào trang web mà ta đã xây dựng. Python cung cấp nhiều cách để thêm dữ liệu mới vào danh sách hiện có.

#### Thêm phần tử vào cuối danh sách

Cách đơn giản nhất để thêm một phần tử mới vào danh sách là sử dụng phương thức `append()`. Khi ta thêm một phần tử bằng cách này, nó sẽ được đặt ở cuối danh sách. Sử dụng cùng danh sách từ ví dụ trước, chúng ta sẽ thêm phần tử mới `"ducati"` vào cuối danh sách:

```python
motorcycles = ["honda", "yamaha", "suzuki"]
print(motorcycles)  # ['honda', 'yamaha', 'suzuki']
motorcycles.append("ducati")
print(motorcycles)  # ['honda', 'yamaha', 'suzuki', 'ducati']
```

Phương thức `append()` giúp ta dễ dàng xây dựng danh sách linh hoạt. Ví dụ, ta có thể bắt đầu với một danh sách trống và sau đó thêm các thành phần vào danh sách bằng cách sử dụng một loạt các lệnh `append()`. Bây giờ, hãy cùng thử thêm các hãng xe 'honda', 'yamaha' và 'suzuki' vào một danh sách trống nhé!

```python
motorcycles = []
motorcycles.append("honda")
motorcycles.append("yamaha")
motorcycles.append("suzuki")
print(motorcycles)  # ['honda', 'yamaha', 'suzuki']
```

Cách xây dựng danh sách như thế này rất phổ biến, bởi vì thông thường ta không thể biết trước dữ liệu người dùng muốn lưu trữ trong chương trình cho đến khi chương trình chạy. Để trao quyền kiểm soát cho người dùng, hãy bắt đầu bằng cách định nghĩa một danh sách trống để chứa các giá trị của người dùng. Sau đó, ta có thể thêm từng giá trị mới được cung cấp vào danh sách vừa tạo.

#### Chèn phần tử vào danh sách

Thay vì chỉ thêm vào cuối danh sách, ta có thể chèn một phần tử mới ở bất kỳ vị trí nào bằng phương thức `insert()`. Để sử dụng `insert()`, ta cần cung cấp vị trí và giá trị của phần tử mới mà ta muốn chèn.

```python
motorcycles = ["honda", "yamaha", "suzuki"]
motorcycles.insert(0, 'ducati')
print(motorcycles)
```

Ở ví dụ trên, chúng ta đã sử dụng phương thức `insert()` để chèn giá trị `"ducati"` vào vị trí thứ 0, các phần tử ở đằng sau sẽ được dịch chuyển sang phía bên phải.

### Xóa phần tử khỏi danh sách

Thường thì chúng ta sẽ muốn xóa một phần tử hoặc một tập hợp các phần tử khỏi danh sách. Ví dụ, khi một người chơi bắn hạ một người ngoài hành tinh từ trên trời, chúng ta sẽ muốn xóa nó khỏi danh sách những người ngoài hành tinh đang hoạt động. Hoặc khi một người dùng quyết định hủy tài khoản trên ứng dụng web mà chúng ta tạo ra, chúng ta sẽ muốn xóa người dùng đó khỏi danh sách người dùng đang hoạt động. Chúng ta có thể xóa một phần tử theo vị trí của nó trong danh sách hoặc theo giá trị của nó.

#### Xóa phần tử sử dụng lệnh del

Nếu ta đã biết vị trí của phần tử mà ta muốn xóa nằm ở đâu trong danh sách, ta có thể sử dụng lệnh `del` để xóa nó.

```python
motorcycles = ["honda", "yamaha", "suzuki"]
print(motorcycles)  # ['honda', 'yamaha', 'suzuki']
del motorcycles[0]
print(motorcycles)  # ['yamaha', 'suzuki']
```

Ở trên, chúng ra đã sử dụng lệnh `del` để xóa phần tử đầu tiên (`"honda"`) khỏi danh sách các loại xe máy. Ta có thể xóa một phẩn tử khỏi danh sách từ bất kỳ vị trí nào nếu ta biết vị trí của nó. Để xóa phần tử thứ 2 (`"yamaha"`) khỏi danh sách, ta viết như sau:

```python
motorcycles = ["honda", "yamaha", "suzuki"]
print(motorcycles)  # ['honda', 'yamaha', 'suzuki']
del motorcycles[1]
print(motorcycles)  # ['honda', 'suzuki']
```

#### Xóa phần tử sử dụng phương thức pop()

Đôi khi, chúng ta sẽ muốn sử dụng giá trị của một phần tử sau khi đã xóa nó khỏi danh sách. Ví dụ, khi rút một lá bài, ta xóa một lá bài khỏi bộ bài, nhưng vẫn muốn lấy giá giá trị của lá bài đó để có thể tính điểm.

Phương thức `pop()` xóa phần tử cuối cùng khỏi danh sách, nhưng nó cho phép ta có thể lấy được giá trị của phần tử mà ta vừa xóa. Thuật ngữ `pop` (bật nảy) xuất phát từ việc nghĩ về danh sách như một chồng cách phần tử và ta có thể làm cho phần tử ở trên cùng bật nảy lên rồi bắt lấy nó. Trong phép so sánh này, đỉnh của chồng tương ứng với phần tử cuối của danh sách.

Bây giờ, chúng ta thử `pop` một chiếc xe máy ra khỏi danh sách.

```python
motorcycles = ["honda", "yamaha", "suzuki"]
print(motorcycles)  # ['honda', 'yamaha', 'suzuki']
popped_motorcycle = motorcycles.pop()
print(motorcycles)  # ['honda', 'yamaha']
print(popped_motorcycle)  # suzuki
```

Ngoài ra, ta cũng có thể sử dụng phương thức `pop()` để lấy ra một phần tử ở bất kỳ vị trí nào trong danh sách bằng cách cung cấp cho phương thức vị trí của phần tử mà ta muốn lấy ra.

```python
motorcycles = ["honda", "yamaha", "suzuki"]
print(motorcycles)  # ['honda', 'yamaha', 'suzuki']
popped_motorcycle = motorcycles.pop(1)
print(motorcycles)  # ['honda', 'suzuki']
print(popped_motorcycle)  # yamaha
```

#### Xóa phần tử sử dụng phương thức remove

Đôi khi, ta có thể chỉ biết giá trị của phần tử mà ta muốn xóa chứ không biết nó nằm ở vị trí nào trong danh sách. Trong trường hợp này, ta có thể sử dụng phương thức `remove()`.

Ví dụ, giả sử chúng ta muốn xóa xe `suzuki` khỏi danh sách

```python
motorcycles = ["honda", "yamaha", "suzuki", "ducati"]
print(motorcycles)  # ['honda', 'yamaha', 'suzuki', 'ducati']
motorcycles.remove("suzuki")
print(motorcycles)  # ['honda', 'yamaha', 'ducati']
```

## Quản lý thứ tự các phần tử trong danh sách

Thường thì danh sách của chúng ta sẽ được tạo ra theo một thứ tự không thể đoán trước, vì chúng ta không thể luôn kiểm soát thứ tự mà người dùng cung cấp dữ liệu của họ. Tuy nhiên, chúng ta thường muốn trình bày thông tin của mình theo một thứ tự cụ thể. Python cung cấp nhiều cách khác nhau để tổ chức danh sách của chúng ta, tùy thuộc vào tình huống.

### Sắp xếp danh sách với phương thức sort

Phương thức `sort()` của Python làm cho việc sắp xếp một danh sách khá dễ dàng. Hãy tưởng tượng chúng ta có một danh sách các loại ô tô và muốn thay đổi thứ tự của danh sách để lưu chúng theo thứ tự bảng chữ cái. Để đơn giản hóa nhiệm vụ, hãy giả sử rằng tất cả các giá trị trong danh sách đều là chữ thường.

```python
cars = ["bmw", "audi", "toyota", "subaru"]
cars.sort()
print(cars)  # ['audi', 'bmw', 'subaru', 'toyota']
```

Ta cũng có thể sắp xếp danh sách này theo thứ tự bảng chữ cái giảm dần bằng cách truyền đối số `reverse=True` vào phương thức `sort()`

```python
cars = ["bmw", "audi", "toyota", "subaru"]
cars.sort(reverse=True)
print(cars)  # ['toyota', 'subaru', 'bmw', 'audi']
```

Khi chúng ta dùng phương thức `sort()`, ta đã thay đổi vị trí các phần tử trong danh sách theo 
thứ tự tăng dần hoặc giảm dần. khi danh sách được sắp xếp lại bằng cách này, không có cách nào để danh sách trở về thứ tự như ban đầu (khi chưa sắp xếp) được nữa.

### Sắp xếp danh sách với hàm sorted

Để duy trì thứ tự ban đầu của một danh sách nhưng hiển thị nó theo thứ tự đã sắp xếp, bạn có thể sử dụng hàm `sorted()`. Hàm `sorted()` cho phép ta hiển thị danh sách của mình theo một thứ tự cụ thể, nhưng không ảnh hưởng đến thứ tự thực sự của danh sách.

```python
cars = ["bmw", "audi", "toyota", "subaru"]
print("Here is the original list:")
print(cars)  # ['bmw', 'audi', 'toyota', 'subaru']
print("\nHere is the sorted list:")
print(sorted(cars))  # ['audi', 'bmw', 'subaru', 'toyota']
print("\nHere is the original list again:")
print(cars)  # ['bmw', 'audi', 'toyota', 'subaru']
```

Chú ý rằng danh sách vẫn tồn tại trong thứ tự ban đầu của nó sau khi đã sử dụng hàm `sorted()`. Hàm `sorted()` cũng có thể chấp nhận đối số `reverse=True` nếu bạn muốn hiển thị danh sách theo thứ tự chữ cái đảo ngược.

### Đảo ngược vị trí các phần tử trong danh sách


Để đảo ngược thứ tự ban đầu của một danh sách, bạn có thể sử dụng phương thức `reverse()`. Nếu ban đầu chúng ta lưu trữ danh sách các ô tô theo thứ tự thời gian, theo thứ tự chúng ta sở hữu chúng, chúng ta có thể dễ dàng sắp xếp lại danh sách theo thứ tự ngược lại, từ mới nhất đến cũ nhất:

```python
cars = ["bmw", "audi", "toyota", "subaru"]
print(cars)  # ['bmw', 'audi', 'toyota', 'subaru']
cars.reverse()
print(cars)  # ['subaru', 'toyota', 'audi', 'bmw']
```

Chú ý rằng phương thức `reverse()` không sắp xếp ngược theo thứ tự chữ cái, nó chỉ đơn giản là đảo ngược thứ tự của danh sách.

Phương thức `reverse()` thay đổi thứ tự của danh sách ban đầu, nhưng ta có thể quay lại thứ tự ban đầu bất kỳ lúc nào bằng cách áp dụng `reverse()` lần thứ 2 vào cùng một danh sách.

### Kiểm tra độ dài của danh sách

Ta có thể kiểm tra độ dài (số lượng các phần tử) của danh sách một cách nhanh chóng bằng cách sử dụng hàm `len()`. Danh sách trong ví dụ của chúng ta có 4 phần tử, nên độ dài của nó sẽ là 4.


```python
cars = ["bmw", "audi", "toyota", "subaru"]
print(len(cars))  # 4
```
