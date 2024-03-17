Chỉ với vài bước đơn giản, bạn có thể nhanh chóng tạo ra một sản phẩm mới:

 

1. Trên trang chủ của nền tảng, nhấp vào nút "Tạo sản phẩm" để vào trang tạo sản phẩm mới. (Như hình bên dưới)

              



2. Điền chính xác tên sản phẩm và chọn cảnh và mô-đun cần thiết. (Như hình bên dưới)



3. Vào trang cài đặt của nền tảng hệ thống liên quan và định cấu hình các khả năng của SDK liên quan.

( 1 ) Từ đánh thức sản phẩm được tùy chỉnh và từ trả lời đánh thức

Hỗ trợ cấu hình tùy chỉnh các từ đánh thức gồm 3-6 ký tự;
Để đảm bảo trải nghiệm đánh thức tốt nhất cho các sản phẩm giọng nói, nền tảng này cung cấp chức năng tính điểm cho cách phát âm các từ đánh thức và cung cấp thông tin hướng dẫn cụ thể;
Không thể sử dụng các từ ngữ liên quan đến nội dung khiêu dâm, cờ bạc, ma túy, nhạy cảm về chính trị, lăng mạ thô tục và các nội dung bất hợp pháp khác;
Để hoàn thiện các quy tắc định nghĩa từ đánh thức, hãy nhấp vào "Quy tắc tùy chỉnh đánh thức từ" trên giao diện
Hỗ trợ tối đa 5 câu trả lời đánh thức và sẽ được phát ngẫu nhiên sau khi cài đặt.


( 2 ) Điền từ lệnh và câu trả lời theo quy tắc

         Như trong hình bên dưới, bạn có thể nhập trực tiếp định nghĩa của từ lệnh và từ phản hồi vào trang, bạn có thể tham khảo định dạng kiểu chữ mặc định của nền tảng để cài đặt.



 

Mô tả định dạng cú pháp và giới thiệu quy tắc

Để tạo điều kiện thuận lợi cho việc xây dựng sản phẩm, nền tảng xác định một tập hợp các định dạng cú pháp, bao gồm:

hành động = từ lệnh 1| từ lệnh 2... @reply từ

 

Ví dụ: TempSet15 = Đặt mười lăm độ | Mười lăm độ @ đã được đặt thành mười lăm độ

Hành động là mã định danh duy nhất của lệnh điều khiển. Khi người dùng nói "đặt mười lăm độ" và "mười lăm độ" với thiết bị và được hiểu về mặt ngữ nghĩa, nếu thiết bị được kết nối, mô-đun hiểu ngữ nghĩa sẽ chuyển TempSet15 đến thiết bị.

Từ lệnh là thuật ngữ giọng nói mà bạn muốn xác định, người dùng phải nói theo thuật ngữ đã xác định mới có hiệu quả. Ví dụ: người dùng có thể sử dụng "đặt mười lăm độ" và "mười lăm độ" để kiểm soát cùng một nhiệt độ đã đặt là 15 độ.

Reply: Trả lời thiết bị về lệnh điều khiển này.

Các hành động, từ lệnh và từ trả lời đều do người dùng xác định. Hành động trước dấu bằng là một giá trị duy nhất; có thể nhập nhiều từ lệnh sau dấu bằng, phân tách bằng ký hiệu |; @ được theo sau bởi từ trả lời và mỗi lệnh điều khiển có thể xác định một câu trả lời tương ứng.

 

Bấm vào dấu chấm hỏi sau định dạng ngữ pháp để xem yêu cầu về định dạng ngữ pháp:

Ø Hành động bao gồm tiếng Anh, gạch chân "_" và số, phải bắt đầu bằng tiếng Anh, không phân biệt chữ hoa chữ thường và phải dài trong 15 ký tự.

Ø Hỗ trợ tối đa 100 từ lệnh, mỗi từ giới hạn 2-10 ký tự và chỉ hỗ trợ tiếng Trung

Ø Một hành động chỉ hỗ trợ một câu trả lời, tổng số từ trong câu trả lời không quá 500 ký tự, hỗ trợ tiếng Trung, số, dấu phẩy, dấu chấm, dấu chấm hỏi.

 

Bấm vào dấu chấm hỏi sau câu ngữ pháp để xem hướng dẫn sử dụng nhãn phát âm đặc biệt cho câu trả lời:

Ø  <py> : Khi cần sửa lại cách phát âm của một ký tự tiếng Trung.

Lưu ý: Các âm Bính âm nằm trong khoảng từ 1 đến 5, 1 đến 4 tương ứng với âm thứ nhất đến âm thứ tư và 5 tương ứng với âm nhẹ.

Ví dụ: <py>tiao2</py> đã được điều chỉnh về vị trí gió <py>zhong1</py> ở giữa

Thông báo là: đã điều chỉnh (tiao2) về vị trí gió giữa (zhong1)

Ø  <value> : Số cần báo theo cách đọc số

Ví dụ: Nó đã được đặt thành <value>15</value> độ

Thông báo là: Nó đã được đặt ở mức mười lăm độ

Ø  <code> : Các số cần báo từng chữ số theo chuỗi chữ số.

Ví dụ: Nó đã được đặt thành <code>15</code> độ

Thông báo là: đặt ở mức một và năm độ

 

Nhà phát triển lưu ý:

 

1.        Sản phẩm mặc định hỗ trợ điều chỉnh âm lượng, cấu trúc câu mặc định để điều khiển điều chỉnh âm lượng như sau:

  VolumeUpUni= tăng âm lượng

  VolumeDownUni= Giảm âm lượng

Nếu bạn cần tùy chỉnh âm lượng, kỹ thuật kiểm soát thoát hoạt động và phát sóng phản hồi, bạn có thể thêm các câu điều khiển ở trên vào tệp ngữ pháp, chỉ cần giữ nguyên hành động trước dấu = và sửa đổi nội dung sau dấu =.

Ví dụ như sau:

VolumeUpUni=To hơn|Tăng âm lượng to hơn@Âm lượng đã được tăng cho bạn

exitUni=Bye|Tạm biệt@Được rồi, tôi sẽ thoát trước.

2.        Sản phẩm có logic điều khiển mức âm lượng ba cấp tích hợp, logic này không được bật theo mặc định. Nếu cần sử dụng logic này, bạn có thể xác định các từ lệnh ngoại tuyến và các từ phát sóng, đồng thời thêm các thuật ngữ để có hiệu lực:

   Âm lượng tối đaMaxUni

   âm lượng trung bìnhMidUni

Khối    lượng tối thiểuMinUni

Nếu muốn thêm điều chỉnh âm lượng tối đa, bạn có thể tham khảo ví dụ bên dưới để thêm câu:

VolumeMaxUni=Âm lượng tối đa|Âm lượng được điều chỉnh ở mức tối đa@đã được điều chỉnh ở mức âm lượng tối đa

 

3.        Người dùng có thể chỉ định các hành động cụ thể trong phần tùy chỉnh từ lệnh ngoại tuyến và xác định chương trình phát ngôn ngữ phản hồi tương tác không bằng giọng nói cho các tình huống tương tác bằng giọng nói bất thường.

Định dạng như sau:

Đặc biệt_Trả lời@Trả lời 1|Trả lời 2|Trả lời 3

Chẳng hạn như phát sóng cảnh báo: lấy ấm đun nước thông minh làm ví dụ, cảm biến trong sản phẩm phát hiện tình trạng thiếu nước và tự động đưa ra cảnh báo bằng giọng nói;

Ví dụ: giới hạn phát sóng: lệnh điều hòa "tăng nhiệt độ" và phát sóng bình thường là "nhiệt độ đã tăng"; khi nhiệt độ đạt đến giới hạn trên, phát sóng "nhiệt độ đã được điều chỉnh lên cao nhất".

Ví dụ như sau:

Special_Replies@Neidan Dry Cooking|Ấm hết nước|Không có nước|Chủ nhân, vui lòng thêm nước

 

4.        Người dùng có thể chỉ định các từ cạnh tranh cụ thể (có thể hiểu là các từ lệnh không hợp lệ) trong phần tùy chỉnh từ lệnh ngoại tuyến để tránh nhận dạng sai với một xác suất nhất định.

Định dạng như sau:

Special_Gabages=từ lệnh 1|từ lệnh 2|từ lệnh 3|...

Lấy sản phẩm điều hòa làm ví dụ, không có hướng dẫn điều chỉnh nhiệt độ cao hơn 32 độ, khi người dùng nói “36 độ” là họ không muốn điều hòa nhận ra “16 độ”,
lấy sản phẩm điều hòa làm ví dụ. là không có hướng dẫn gió tự động, khi người dùng nói "gió tự động" là họ không muốn máy điều hòa nhận biết "gió tự nhiên" (nếu ngưỡng được đặt ở mức thấp).

Ví dụ như sau:

Ví dụ: Special_Gabages=36 độ|46 độ|56 độ|66 độ

 

( 3 ) Các từ lệnh không đánh thức

Bạn có thể điều khiển thiết bị bằng cách nói các từ lệnh mà không cần thức dậy. Các từ lệnh không cần đánh thức ở đây cần được đặt trong mô-đun tùy chỉnh từ lệnh ngoại tuyến trước khi bạn có thể chọn và định cấu hình chúng.

Sau khi lệnh đánh thức miễn phí có hiệu lực, thiết bị sẽ ở trạng thái đánh thức.

Các từ lệnh không đánh thức và các từ đánh thức có thể tồn tại cùng lúc hoặc riêng lẻ và tổng số lượng của cả hai không được vượt quá 10. Đối với một số sản phẩm giọng nói cụ thể, chỉ có thể sử dụng các từ lệnh đánh thức thay vì các từ đánh thức.

 



 

(4 ) Để định vị sản phẩm hãy chọn loa phù hợp với mẫu sản phẩm

Huyền Huyền và KiYo sôi nổi và dễ thương, Tangtang và Tiantian ngây thơ và trẻ con, Lingling dịu dàng và đáng yêu, Xiaowenyu và Xiaofeng trang trọng và nghiêm túc, bảy âm sắc để lựa chọn;
Điều chỉnh âm lượng và tốc độ nói;


( 5 ) Các cấu hình khác

1)     Cấu hình âm khởi động

Sản phẩm được đặt mặc định là nhạc chuông khởi động. Nếu bạn cần tùy chỉnh lời chào khởi động, bạn cũng có thể chọn tùy chỉnh nội dung và sản phẩm sẽ tự động phát nội dung đó sau khi khởi động. Bài phát biểu chào mừng có thể tùy chỉnh được giới hạn ở tiếng Trung và bạn có thể nhập 30 ký tự, bạn cũng có thể chọn không sử dụng giai điệu khởi động.



2)     Xác định các cấu hình liên quan đến thoát trạng thái

Để đảm bảo trải nghiệm cho người dùng, các sản phẩm giọng nói sẽ chủ động thoát khỏi trạng thái nhận dạng nếu không có giọng nói đầu vào trong một khoảng thời gian sau khi thức dậy, nếu cần nhập từ lệnh thì bạn cần phải thức dậy lại.

Thời gian hiệu quả trong khoảng thời gian này để chờ người dùng nhập lệnh thoại là "thời gian thoát khi hết thời gian thức".

Để đảm bảo trải nghiệm người dùng tốt hơn cho sản phẩm, cài đặt thời gian thoát thời gian chờ được hỗ trợ từ 5 giây đến 60 giây, mặc định là 10 giây.
Có thể đặt tối đa 2 câu trả lời cho thời gian chờ thoát.
Khi người dùng muốn kết thúc cuộc trò chuyện, họ có thể chủ động yêu cầu thoát khỏi trạng thái nhận dạng.

Các lệnh thoát mặc định là "Thoát" và "Tạm biệt", có thể được sửa đổi theo định nghĩa sản phẩm. Có thể đặt tối đa 3 lệnh.
Bạn có thể thiết lập tối đa 2 câu trả lời thoát đang hoạt động.
 

4. Sau khi cài đặt hoàn tất, nhấp vào "Tạo phiên bản mới" để tạo sản phẩm thành công.

