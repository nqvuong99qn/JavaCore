> ## `static` and `final` in `Java`

Chắc hẳn chúng ta, không học Java đều biết hai tự khóa này. Nhưng có vấn đề là nhiều khi chúng ta không biết kĩ về nó, thật sự là như vậy. Mình cũng vậy, và khi đi phỏng vấn à không, trong một bài evaluation tại công ty, mình bị hỏi một câu cơ bản như vậy và trả lời rất lơ bơ chẳng hạn như: static là biến tĩnh, bla bla, mà không nói được cái bản chất, cái ý quan trọng của nó. Chính vì vậy, mà mình đã quyết viết bài viết này, gửi đến mọi người, nếu ai có ghé qua, đọc thì keep in mind nhé. Quan trọng đấy, kiểu gì đi phỏng vấn cũng gặp thôi. Nếu trả lời như cách mình trả lời bên dưới là auto ăn trọn điểm từ interviewer nhé! Rồi chúng ta cùng bắt đầu thôi nào

> ### `static`

static là gì? Nếu mà có một chút tiếng anh cơ bản, thì tao biết nó có nghĩa là tĩnh, là cái  gì đó bất biến, không thổi đổi. Đúng  chính xác là như vậy. Trong Java nó cũng có nghĩa như vậy: biến tĩnh, phương thức tĩnh thậm chí là class tĩnh. Quá dễ hiểu đúng không nào cơ mà. Nó tĩnh  như vậy thì dùng ở đâu, dùng như thế nào, khi nào cần dùng nè. 

Nói ngắn gọn từ khóa static giúp ta `quản lý bộ nhớ tốt` và `cho phép truy cập trực tiếp từ lớp mà không cần phải khởi tạo`. Quá tiện đúng không nè. 


Ví dụ thế này cho dễ hiểu: Một đối tượng hình tròn có thông tin về bán kính, phương thức tính diện tích, số `pi` cũng là 1 field ở class ấy. Vậy khi tính toán diện tích cho nhiều đối tượng hình tròn, ta luôn dùng một giá trị `pi`. Khi ấy, biến `pi` khi có từ khóa `static` đi kèm nó sẽ được cấp phát vùng nhớ một lần duy nhất, sau đó cách đối lượng đường tròn khác được tạo, sử dụng tiếp cái value `pi` ở `class` đường tròn đầu tiên. Nếu chúng ta không sử dụng từ khóa `static` thì hiểu nhiên, mỗi lần khởi tạo đối tượng đường tròn thì đối tượng `pi` cũng được cấp phát mới, ví dụ tao tạo 100 hình tròn khác nhau, mà giá trị `pi` cũng được cấp phát 100 lần, trong khi giá trị của nó có thay đổi gì đâu, Dư quá thừa quá đúng không nè. Chính vì vậy đây là một trong những cái lợi của từ khóa `static` nè. Chắc là mọi người đã hiểu đúng không nà!!!!



> ### `final`

