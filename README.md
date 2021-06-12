# Card Infomation Detection

Dữ liệu đầu vào của quá trình detection là ảnh chứng minh nhân dân. Với mỗi ảnh chứng minh nhân dân, model cần thiết trích xuất được các thông tin cơ bản: id cá nhân, tên, ngày tháng năm sinh, quê quán, nơi cư trú hoặc ảnh nếu cần thiết.

Quá trình trích xuất bao gồm 3 giai đoạn:
1. Chuẩn bị dữ liệu
2. Lựa chọn model và thực hiện training model với tập dữ liệu đã được xử lý
3. Thực hiện quá trình trích xuất

Trong đó repo này tập trung vào quá trình 2: lựa chọn model, chủ yếu là sử dụng các neural network để tiến hành quá trình học với dữ liệu. Ở đây bài toán thực hiện là bài toán object detection, bài toán được thực hiện trước bài toán ocr để trích xuất thông tin.
Trong đó dữ liệu đầu vào của quá trình này là các ảnh chứa đối tượng là chứng minh nhân dân (đã được xử lý qua các bước: detect CMND trong ảnh (có thể sử dụng các model key-point based để detect 4 góc)rồi tiến hành transformation về góc 90 độ) và các nhãn đối tượng dưới dạng bounding box.
