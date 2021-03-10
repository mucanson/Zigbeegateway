# Hướng Dẫn Kết Nối Công Tắc Thông Minh Tuya Và Google Home Mini Với Home Assistant

## I. Kết nối công tắc thông minh Tuya với Home Assistant :

### Bước 1: Chuẩn bị và kết nối các thiết bị với nguồn điện
* Mô hình và các đi dây cho công tắc

  ![diday](../_static/images/congtactruonghop.jpg)

### Bước 2: Kết nối công Tắc Tuya với ứng dụng của nhà sản xuất *"TuyaSmart"*.

* Tải App TuyaSmart trên AppStore hoặc CHPlay

  ![app](../_static/images/appTuya.jpg)

* Đăng ký tài khoản và đăng nhập vào ứng dụng Tuya đã tải

  ![B1](../_static/images/loginTuya.jpg)

* Giao diện màn hình chính khi đăng nhập, nhấn vào icon dấu "+" màu cam góc trên bên phải màn hình để thêm thiết bị

  ![B1](../_static/images/B1giaodienapp.jpg)

* Kéo xuống danh sách thiết bị, chọn Scenario Switch (Wi-Fi)

  ![B2](../_static/images/B2giaodienapp.jpg)

* Kết nối thiết bị công tắc Tuya với WiFi tại nhà

  ![B3](../_static/images/B3giaodienapp.jpg)

* Nhấn giữ vào thiết bị để kích hoạt trạng thái chờ kết nối và chờ cho đến khi hoàn thành kết nối

  ![B4](../_static/images/B4giaodienapp.jpg)

* Nếu thời gian hết 2 phút vẫn chưa kết nối được thì làm lại từ bước thêm thiết bị

  ![B5](../_static/images/B5giaodienapp.jpg)

* Kết nối thành công, thiết bị đã được tìm thấy

  ![B6](../_static/images/B6giaodienapp.jpg)

### Bước 3: Cấu hình cài đặt Home Assistant.

* Đăng nhập Home Assistant -> Chọn Supervisor -> Chọn Add-on Store -> install File editor(Xem thêm hướng dẫn ở bài [Hướng dẫn cài đặt Home Assistant cho Raspberry PI 3 trên Ubuntu](./SetupHASS.html))

  ![B1](../_static/images/B1cauhinhhass.png)

* Mở giao diện chính của [Home Assistant](https://www.home-assistant.io/) -> chọn Intergrations

  ![B2](../_static/images/B2cauhinhhass.png)

* Tìm kiếm Tuya

  ![B3](../_static/images/B3cauhinhhass.png)

* Tìm kiếm Configuration via YAML, copy đoạn code config

  ![B4](../_static/images/B4cauhinhhass.png)

* Cách 1: Ấn vào icon folder ở góc trên bên trái màn hình -> Lưu ý tìm đúng folder như hướng dẫn của Tuya -> Dán đoạn code config vào File editor (/config/configuration.yaml)

* Cách 2: SSH vào raspberry để điều chỉnh trực tiếp (Xem thêm hướng dẫn ở bài docs "Kết nối các thiết bị với Home Assistant")

* Lưu trạng thái vừa được cập nhật

  ![B5](../_static/images/B5cauhinhhass.png)

* Chọn Configuration -> Chọn General -> Chọn Server Controls

  ![B6](../_static/images/B6cauhinhhass.png)

* Tiến hành kiểm tra config -> Chọn CHECK CONFIGURATION

* Chọn RESTART ở mục Server management để tiến hành khởi động lại Home Assistants

  ![B7](../_static/images/B7cauhinhhass.png)



### Bước 4: Tìm kiếm và thêm thiết bị vào Home Assistant

* Chọn Developer Tools

    ![B8](../_static/images/B8cauhinhhass.png)

* Tìm kiếm tên thiết bị đã được đặt ở trong TuyaSmart app

    ![B9](../_static/images/B9cauhinhhass.png)

* Tiến hành thiết lập trạng thái cho thiết bị

    ![B10](../_static/images/B10cauhinhhass.png)

* Thêm thiết bị vào Home -> Overview -> Góc trên bên phải màn hình -> Chọn Edit Dashboard

    ![B11](../_static/images/B11cauhinhhass.png)

    ![B12](../_static/images/B12cauhinhhass.png)

    ![B13](../_static/images/B13cauhinhhass.png)

## II. Kết nối Google Home Mini với Home Assistant :

### Bước 1: Kết nối thiết bị Google Home Mini với ứng dụng của nhà sản xuất *"Google Home"*

Video hướng dẫn : https://www.youtube.com/watch?v=eO9Es81unB0&t=435s

### Bước 2: Tạo tài khoản Home Assistant Cloud

* Chọn Configuration -> Chọn Home Assistant Cloud

    ![createcloud](../_static/images/createcloud.png)

* Tiến hành đăng ký tài khoản theo hướng dẫn

    ![createcloud](../_static/images/createcloud1.png)

### Bước 3: Kết nối ứng dụng Goole Home với Home Assistant Cloud

* Chọn mục Profile ở góc trên bên phải màn hình -> Chọn Assistants Settings

  ![AssistantSettings](../_static/images/AssistantSettings.jpg)

* Chọn Home Control

  ![AssistantSettings](../_static/images/AssistantSettings1.jpg)

* Chọn vào biểu tượng thêm vào ở góc dưới bên phải màn hình

  ![homecontrol1.jpg](../_static/images/homecontrol1.jpg)

* Tìm kiếm thông tin thiết bị cần link

  ![homecontrol2.jpg](../_static/images/homecontrol2.jpg)

* Tìm Home Assistants -> Chọn mục đầu tiên

  ![homecontrol3.jpg](../_static/images/homecontrol3.jpg)

* Nhập tài khoản Home Assistant cloud

  ![homecontrol4.jpg](../_static/images/homecontrol4.jpg)


### Bước 4: Đồng bộ các thiết bị ở Home Assistant với App Google Home.

* Tiến hành thêm thiết bị từ Home Assistants xuống Google Home

  ![homecontrol5.jpg](../_static/images/homecontrol5.jpg)

* Thêm thiết bị vào home của mình mong muốn

  ![homecontrol6.jpg](../_static/images/homecontrol6.jpg)

* Thêm thiết bị vào phòng mình mong muốn

  ![homecontrol7.jpg](../_static/images/homecontrol7.jpg)

  ![hoanchinh.jpg](../_static/images/hoanchinh.jpg)
