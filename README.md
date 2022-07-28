- 👋Hi, I'm Hong Cuc but you can call me to Selena
- 👀 I’m interested in Java Softwave Engineer
- 🌱 I’m currently learning at University Information Technology - VNU HCMC in Vietnam
- 📫 How to reach me 
  - Email: cuclth2701@gmail.com
  - Facebook: https://www.facebook.com/LTHC9/
  - Linkedin: https://www.linkedin.com/in/lthc9/


Xin chào BTC và toàn thể các bạn đang có mặt trong hội trường ngày hôm nay. Em là Lê Thị Hồng Cúc, thành viên của team 8 Infinity. Hôm nay em xin phép đại diện team em trình bày về web app mà nhóm em làm cho Challenge nhóm em đã chọn. Đó là Challenge 6: Event: Picture Finder và web của tụi em tên là infinity.

Trước tiên, em xin phép giới thiệu đôi nét về thành viên của team. Mentor của team là anh Thông Huỳnh. Team em có 7 thành viên bao gồm: Hoàng Thị Hường, Nguyễn Thanh Sang, Nguyễn Hứa Tiến Trình, Nguyễn Huy Tú, Trần Mạnh Hùng, Phan Quang Minh Long
Phần trình bày của m sẽ bao gồm 7 nội dung chính: 
Thứ 1 là Tình huống đặt ra và vấn đề cần giải quyết
Thứ 2 là Giải pháp
Thứ 3 là Lợi ích của giải pháp
Thứ 4 là các tính năng 
Thứ 5 là kiến trúc phần mềm
Thứ 6 phần demo
Và cuối cùng là hướng phát triển
Phần 1 Tình huống đặt ra và vấn đề cần giải quyết:
Tình huống mà challenge đặt ra đó là: Hầu hết các event hiện nay, hình ảnh được chụp và được lưu trên nhiều nguồn khác nhau như gg drive, one drive,facebook vv..
Và với một lượng lớn ảnh như thế, nếu bạn chỉ muốn lưu trữ những hình có chứa ảnh của bản thân thì sẽ phải mất hàng giờ để tìm kiếm phân loại. Việc này vừa gây lãng phí thời gian, vừa dễ bỏ bị sót ảnh, thậm chí có thể gây stress cho bạn trong trường hợp sau khi xem hơn ngàn tấm ảnh và phát hiện bản thân chỉ xuất hiện duy nhất trong một khung hình. 

Từ tình huống trên nhóm em tìm ra 2 vấn đề cần phải giải quyết:
_Làm thế nào để có thể integrate ảnh từ nhiều nguồn khác nhau?
_Làm thế nào để nhận diện được ảnh có chứa đối tượng cần tìm và vị trí của đối tượng trong ảnh?
Sau khi xác định rõ được vấn đề cần giải quyết, mời mọi người sang với giải pháp mà nhóm em đưa ra:
•	Giải pháp này hướng đến 02 dạng đối tượng là Nhà tổ chức sự kiện (doanh nghiệp) và Người dùng cá nhân. 
•	Về Workflow: 
o	Hệ thống sẽ thu nhận và tích hợp các dữ liệu đầu vào (hình ảnh) từ các nguồn khác nhau
o	Thông qua AI / ML, hệ thống sẽ thực hiện trích xuất hình ảnh khuôn mặt , lưu trữ nhúng-> Tạo ra các chỉ số khuôn mặt 
o	Từ đó, giúp nhận diện những hình ảnh giống với hình ảnh khuôn mặt của người dùng 
Vậy những giải pháp mà nhóm em đưa ra mang lại lợi ích gì?
Đó là tiết kiệm thời gian hay spend less time. Khi mà thay vì có thể sẽ mất 1 ngày để lựa ảnh rồi nếu muốn sống ảo trên Facebook hay insta thì lại mất thêm một khoảng để chỉnh ảnh, sau từng ấy thời gian có thể ta chẳng còn hứng thú để đăng ảnh  thì nay chỉ cần tốn chưa đến 1 phút lọc ảnh và have more time để chỉnh ảnh sống ảo. Như vậy ta sẽ have more fun.
Hiện nay, các ông lớn như google hay facebook đều có những thuật toán để nhận dạng, như facebook khi mà ta đăng ảnh thì fb sẽ Tự động phát hiện khuôn mặt và đề xuất tên tài khoản sở hữu khuôn mặt. Hay google photo sẽ nhận dạng khuôn mặt của những người khác nhau từ lưu trữ ảnh của người dùng tự động và yêu cầu người dùng chọn khuôn mặt cụ thể mà họ đang tìm kiếm. Hay gần đây nhất là https://bibpix.net/ một web app cho phép các vận động viên tìm ảnh của họ bằng số BIB. 
Nhưng nhìn chung đa phần các giải pháp hiện tại đều được tự động hóa một phần, yêu cầu sự trợ giúp của người dùng nhiều hơn để đạt được kết quả mong muốn. Do đó ứng dụng của chúng em được mong đợi là một hệ thống hoàn toàn tự động nhanh chóng cung cấp cho người dùng hình ảnh của họ mà không cần bất kỳ sự can thiệp thủ công nào

Tiếp theo em sẽ nói qua về những tính năng nổi bật mà ứng dụng chúng em cung cấp:
_Thứ nhất là cho phép integrate từ nhiều nguồn khác nhau như facebook, gg drive, one drive
_Thứ hai là xác định chính xác tất cả hình có chứa ảnh của đối tượng cần tìm trong một kho ảnh lớn
_Thứ bà là Dễ dàng detect đuọc vị trí của đối tượng cần tìm trên hình ảnh.


Ok nói đến đây mọi người sẽ tự hỏi Làm thế nào và bằng cách nào ứng dụng của chúng em có thể làm được điều đó? Mời mọi người cùng em tìm hiểu về kiến trúc ứng dụng của web app infinity: 
Hệ thống xây dựng dựa trên mô hình client server. Giao tiếp giữa các service sử dụng RESTful API. Kết nối đến chung cơ sở dữ liệu GG cloud storage. Web server được xây dựng bằng Nodejs. Ứng dụng client page được xây dựng bằng Angular. Phần face recognition/ AI/ML được implement serverless bằng GG functions, giúp dễ dàng mở rộng và phát triển sau này  theo hướng microservices.

CI/CD

Tiếp đến là phần demo webapp:

Cuối cùng là hướng phát triển:
Trong thời gian tới nhóm em sẽ hoàn thiện các tính năng còn lại bao gồm cho phép integrate từ nhiều source, nhận dạng bằng số BIB, hoàn thiện các chức năng hỗ trợ admin
Cải tiến thuật toán để có thể nhận dạng khuôn mặt cho dù hình ảnh được chụp trong điều kiện xấu để phục vụ cho việc cứu hộ
Cho phép Tìm kiếm ảnh thông qua tư thế đứng, ngồi của người dùng trong ảnh dựa trên chiều cao, khuôn mặt của đối tượng 

