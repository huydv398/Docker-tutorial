# docker cmd

| cmd | des |
| --- | --- |
| docker version | Kiểm tra version của docker |
| docker container ls = docker ps | Hiển thị các container đã tạo |
| docker inspect container_id / name_container | Hiển thị toàn bộ thông tin contaner |
| docker run -d httpd | Tạo container, tùy chọn d (-detach) để container luôn hoạt động |
| docker exec -it 20ca3a5602da /bin/bash | Thực thi một lệnh cho container đang chạy, 
-it - Cho phép tương tác trực tiếp trong Container |
| docker rm <ten_hoac_ID_Container>
docker rm -f <ten_hoac_ID_Container>
docker rm -f `docker ps -aq` | Xóa container |
| docker images -a | các Image trên hệ thống
Các image có mặc định: httpd, busybox, hello-world |
|  |  |
| docker start <ten_hoac_ID_Container>  | Chạy container (ở trạng thái Exited) |
| docker commit container_name |  |
| docker history | Show the history of an image |
| docker pull ubuntu | Thực hiện kéo image ubuntu từ Docker Hub |
| docker run ubuntu | Thực hiện tạo container có Image là Ubuntu, Nếu chưa có image trong repo thì nó tự kéo về rồi thực hiện tạo container |
| docker run -d -p 4000:80 httpd | tạo một container httpd có port là 80, và port để truy cập từ bên ngoài vào là port 4000. |
| docker cp . 5b8d00ee4566:/usr/share/nginx/html | Thực hiện copy file từ local vào container |
| docker attach ID_Container | để truy cập vào container sử dụng |
| docker events | Lệnh dùng để show các tiến trình mà docker đang thực hiện |
| docker attach ID_Container | Truy cập vào container |
| Docker Volume command |  |
| docker run --name apache_test -p 8080:80 -p 443:443 -v /opt/web_test:/var/www/ -d eboraas/apache | • docker run: Thực hiện lệnh docker

    ◦ --name apache_test: đặt tên cho container
    ◦ -p 8080:80 -p 443:443: Forward port của container
    ◦ -v /opt/web_test:/var/www/: gắn thư mục /opt/web_test tại Docker host vào thư mục /var/www/ tại Container (Phân cách nhau bằng dấu :)
    ◦ -d: Thực hiện chạy nền container
    ◦ eboraas/apache: Image mà container được tạo ra.(Nếu image này chưa có trong local thì docker run sẽ tải về và chạy image) |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |