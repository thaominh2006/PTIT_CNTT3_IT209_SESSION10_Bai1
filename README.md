## 4. Thông số trích xuất từ lệnh `docker info`

| Thông số | Giá trị | Ý nghĩa |
|---|---|---|
| Server Version | 29.7.2 | Phiên bản Docker Engine đang chạy |
| Cgroup Driver | cgroupfs | Trình điều khiển cgroups mà Docker dùng để giới hạn tài nguyên |
| Containers | 2 | Tổng số container hiện có (đang chạy, tạm dừng, đã dừng) |
| Images | 3 | Số image đã tải về hoặc build trên máy |

Nhận xét: Cgroup Driver là `cgroupfs` và phiên bản cgroup là 2 (cgroup v2), cho
thấy Docker tự quản lý cây cgroup trực tiếp qua hệ thống tệp cgroup của kernel
Linux. Máy đang dùng Docker Desktop trên Windows, nên Docker Engine chạy bên
trong một máy ảo Linux; điều này minh họa rằng container vẫn dựa vào kernel
Linux (Namespaces và cgroups) để cô lập và giới hạn tài nguyên. Các lệnh
`docker version` và `docker info` đều chạy thành công trong PowerShell bằng tài
khoản thường, không cần quyền Administrator.