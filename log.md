# **NHẬT KÝ TÌM HIỂU KIVY FRAMEWORK**

**Ứng dụng demo:** *Quản lý các nhiệm vụ, hoạt động hằng ngày của cá nhân*

## PHẦN MỀM CON
- Dashboard (thông kê tình trạng công việc, hiệu suất công việc)
- Trình quản trị lịch trình công việc (CRUD công việc)
- Handbook (Cho phép khi nhận công thông tin ghi chú tạm thời )
- Draw: Hỗ trợ handbook

## KIẾN THỨC
- Tìm hiểu python cơ bản (Syntax, OOP)
- Tìm hiểu kivy framework (2 part: *design*, *main*)
- API của kivy object
- Thư viện python hỗ trợ cho ứng dụng (có thể có)

## CHUẨN BỊ CHÍNH
- Kiến thức về kivy framework
- Mô hình dữ liệu (4 ứng dụng con)
- Mô hình quan hệ
- Các công cụ cần có trong quá trình phát triển

## GIAI ĐOẠN
- **Giai đoạn 1**: Cài đặt kivy với pip (python install package)
- **Giai đoạn 2**: Nghiên cứu các khái niệm, công cụ, thư viện của kivy
- **Giai đoạn 3**: Xây dựng, thiết kế hệ thống thông tin
- **Giai đoạn 4**: Thiết kế giao diện phần mềm
- **Giai đoạn 5**: Lập trình, xây dựng phần mềm

## ƯỚC TÍNH THỜI GIAN TỪNG GIAI ĐOẠN
- **Giai đoạn 1 + 2**: 2 tuần
- **Giai đoạn 3**: 2 tuần
- **Giai đoạn 4**: 2 tuần
- **Giai đoạn 5**: 2 tuần

(1 tháng)

## MỤC ĐÍCH
- Tìm hiểu về python (nền tảng), kivy framework 
- Xây dựng mô hình hệ thống thông tin
- Xây dựng một ứng dụng tương đối đơn giản với cái nhìn tổng quát về kivy framewor

## PHẠM VI:
- Hiểu về kivy framework
- Xây dựng ứng dụng với các tính năng đủ để hiểu về kivy framework


## NHẬT KÝ GIAI ĐOẠN

### GIAI ĐOẠN 1

<!-- Cách thức cài đặt kivy framework và project -->

Để cài đặt kivy cần phải cài đặt một virtual environment trước, bằng cách sử dụng pip.

```
python -m install --upgrade pip wheel setuptools virtualenv
```

Tiếp đến, tạo project với virtualenv
```
python -m virtualenv [tên_project]
```

Đối với mọi terminal mới (tức là khi mở lên lại) cần phải activate virtualenv trước.
```
kivy_venv\Scripts\activate
```
Sau khi activate xong nó sẽ hiện thị con trỏ CLI có `(tên_project)` ở phía trước

Và cần phải cài đặt nền tảng kivy, bao gồm các thư viện, plugin vào project sau khi thực hiện tác vụ `activate`
```
python -m pip install --pre kivy[base]
```

Nếu quá lạ lẫm với kivy thì cần cài thêm các example mà đội ngũ phát triển kivy khuyến khích các devs sử dụng. Chỉ cần bổ sung `kivy-examples` vào sau câu lệnh trên.
```
python -m pip install --pre kivy[base] kivy-examples
```

Log sau khi thực hiện xong
```
(da_httt) C:\DA_HTTT>python -m pip install --pre kivy[base] kivy-exampl
es
Collecting kivy-examples
  Using cached Kivy_examples-2.0.0-py2.py3-none-any.whl (9.2 MB)
Collecting kivy-deps.angle~=0.3.0
  Using cached kivy_deps.angle-0.3.0-cp39-cp39-win_amd64.whl (4.7 MB)
Collecting kivy-deps.glew~=0.3.0
  Using cached kivy_deps.glew-0.3.0-cp39-cp39-win_amd64.whl (123 kB)
Collecting kivy-deps.sdl2~=0.3.1
  Using cached kivy_deps.sdl2-0.3.1-cp39-cp39-win_amd64.whl (2.5 MB)
Collecting Kivy-Garden>=0.1.4
  Using cached Kivy_Garden-0.1.4-py3-none-any.whl
Collecting kivy[base]
  Using cached Kivy-2.0.0-cp39-cp39-win_amd64.whl (4.1 MB)
Collecting docutils
  Using cached docutils-0.16-py2.py3-none-any.whl (548 kB)
Collecting pillow
  Using cached Pillow-8.1.0-cp39-cp39-win_amd64.whl (2.2 MB)
Collecting pygments
  Using cached Pygments-2.7.4-py3-none-any.whl (950 kB)
Collecting pypiwin32
  Using cached pypiwin32-223-py3-none-any.whl (1.7 kB)
Collecting pywin32>=223
  Using cached pywin32-300-cp39-cp39-win_amd64.whl (9.2 MB)
Collecting requests
  Using cached requests-2.25.1-py2.py3-none-any.whl (61 kB)
Collecting certifi>=2017.4.17
  Using cached certifi-2020.12.5-py2.py3-none-any.whl (147 kB)
Collecting chardet<5,>=3.0.2
  Using cached chardet-4.0.0-py2.py3-none-any.whl (178 kB)
Collecting idna<3,>=2.5
  Using cached idna-2.10-py2.py3-none-any.whl (58 kB)
Collecting urllib3<1.27,>=1.21.1
  Using cached urllib3-1.26.2-py2.py3-none-any.whl (136 kB)
Installing collected packages: urllib3, idna, chardet, certifi, requests, pywin32, pypiwin32, py
gments, Kivy-Garden, kivy-deps.sdl2, kivy-deps.glew, kivy-deps.angle, docutils, pillow, kivy, ki
vy-examples
Successfully installed Kivy-Garden-0.1.4 certifi-2020.12.5 chardet-4.0.0 docutils-0.16 idna-2.10
 kivy-2.0.0 kivy-deps.angle-0.3.0 kivy-deps.glew-0.3.0 kivy-deps.sdl2-0.3.1 kivy-examples-2.0.0
pillow-8.1.0 pygments-2.7.4 pypiwin32-223 pywin32-300 requests-2.25.1 urllib3-1.26.2
```

Cuối cùng tạo một folder thực hiện app chạy chính.

<!-- Cách CLI hỗ trợ cài đặt khác -->

### GIAI ĐOẠN 2

<!-- Khái niệm, thuật ngữ -->

<!-- Thư viện, API -->

<!-- Công cụ -->

### GIAI ĐOẠN 3

<!-- Ứng dụng: dasboard -->

<!-- Ứng dụng: quản trị lịch trình công việc -->

<!-- Ứng dụng: handnote -->

<!-- Tool: simple drawing cho handnote-->

### GIAI ĐOẠN 4

<!-- Ứng dụng: dasboard -->

<!-- Ứng dụng: quản trị lịch trình công việc -->

<!-- Ứng dụng: handnote -->

<!-- Tool: simple drawing cho handnote-->

### GIAI ĐOẠN 5

<!-- Ứng dụng: dasboard -->

<!-- Ứng dụng: quản trị lịch trình công việc -->

<!-- Ứng dụng: handnote -->

<!-- Tool: simple drawing cho handnote-->

## TÀI LIỆU THAM KHẢO

- Cài đặt: https://kivy.org/doc/stable/gettingstarted/installation.html
- Nghiên cứu, khám phá (Bắt đầu): 
    - https://kivy.org/doc/stable/gettingstarted/intro.html
    - https://kivy.org/doc/stable/guide/basic.html
- Xây dựng, thiết kế hệ thống thông tin
- Thiết kế giao diện phần mềm
- Lập trình, xây dựng phần mềm