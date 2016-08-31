---
layout: post
title: "Những lỗi khi áp dụng các mẫu thiết kế UX trên web di dộng:"
author: phuonglm
date: 2016-08-06 04:40
comments: true
categories:
    - "vi"
    - "trans"
tags:
    - "ux"
    - "mobile"
    - "design"
cover: /images/2015/12/21/django_celery.png
description: How to use django-celery-email on Heroku?
keywords: UX, mobile, design
published: true
---

Nếu bạn là một nhà thiết kế có kinh nghiệm, bạn nên hiểu rằng trong thiết kế UI (giao diện người dùng), việc lấy cảm hứng từ những sản phẩm của người khác không phải là ăn cắp ý tưởng mà là việc học hỏi những kinh nghiệm tốt nhất của những người đi trước, là sử dụng các kiểu mẫu thiết kế và làm theo các chỉ dẫn  nhằm đảm bảo sử dụng các mẫu quen thuộc và tạo nên các giao diện thực sự hữu ích cho người dùng.

Một số người nói rằng việc cứ bám theo các quy tắc cứng nhắc và bắt chước người khác thì sẽ giết chết sự sáng tạo và rồi cuối cùng mọi ứng dụng sẽ cứ na ná nhau. Với quan điểm của một người thiết kế UX (trải nghiệm người dùng), tôi lại thấy vấn đề khác. Việc quen áp dụng các cách khuyên dùng tốt nhất có thể khiến bạn tin rằng Google/Facebook/Instagram hay các ứng dụng khác luôn đúng, mục tiêu thiết kế của họ cũng giống của bạn nên bạn sẽ không bao giờ tự hỏi “có gì sai ở đây?!”. Để chứng minh điều này, dưới đây là một số mẫu thiết kế (hoặc đã từng) được coi là những mẫu thiết kế tốt nhất nhưng rút cuộc nó lại không thực sự tốt như bạn nghĩ.

### 1. Ẩn menu điều hướng

Ít nhất cũng có đến nửa triệu bài báo chủ yếu được viết bởi các designer tranh cãi về menu dạng hamburger (☰). Nếu bạn đã bỏ lỡ chúng thì hãy đọc ở trang [techcrunch](http://techcrunch.com/2014/05/24/before-the-hamburger-button-kills-you/) và [deep.design](http://deep.design/the-hamburger-menu/). Các bài viết ấy thường không bàn cãi về việc sử dụng biểu tượng hamburger mà đó là về việc có nên ẩn các menu điều hướng và hiển thị nó khi người dùng nhấn vào biểu tượng hamburger.
Ban đầu thì việc ẩn hàng loạt menu điều hướng đăng sau nút hamburger này có vẻ như rất tiện lợi cho người thiết kế - bạn không phải lo lắng về việc màn hình bị chiếm diện tích bởi những menu cha con dài trên màn hình quá nhỏ của thiết bị di động, mọi thứ sẽ được ẩn một cách mặc định và chỉ hiện ra khi người dùng muốn.
Tuy nhiên các thực nghiệm lại chỉ ra rằng việc hiển thị menu điều hướng thường trực trên màn hình lại tăng khả năng tương tác giữa người dùng và ứng dụng, làm người dùng hài lòng hơn và thậm chí còn tăng doanh thu từ ứng dụng. Đó là lý do vì sao các ứng dụng lớn đang dần thay đồi bằng cách bỏ đi nút hamburger và quay lại hiển thị những tính năng hay được sử dụng ngay trên màn hình.

{% img center /images/2016/08/06/image_0.png %}

-> Sự thay đổi menu điều hướng của Youtube - Luke Wroblewski <-

Nếu điều hướng của bạn phức tạp, việc ẩn nó đi cũng không khiến nó trở nên thân thiện. Vậy thì việc tối ưu các điều hướng là cần thiết.

### 2. Lạm dụng icon.

Do giới hạn về màn hình, nên nhiều khi bạn sẽ tìm cách tiết kiệm không gian bằng cách thay thế các nhãn bằng các icon ở mọi nơi nếu có thể. Bạn có thể có nhiều lý do để dùng icon như chúng chiếm ít không gian hơn, chúng không bị dịch sang ngôn ngữ khác và người dùng đều rất quen với các icon này rồi. Bạn thấy các ứng dụng khác cũng làm như thế.

Với kiểu suy nghĩ như vậy các bảng thiết kế nhiều khi vô tình dấu đi các tính năng của chương trình đằng sau những icon khó hiểu hoặc đôi lúc mình cũng chẳng biết là cái gì nữa và dưới đây là một ví dụ: 

{% img center /images/2016/08/06/image_1.png %}

-> Liệu bạn có đoán được icon này trong Instagram là để gửi tin nhắn không! <-

{% img center /images/2016/08/06/image_2.png %}

-> Hay icon này trong Google Translate dùng để làm gì? <-

Sẽ là sai lầm khi bạn nghĩ rằng người dùng đã quen với việc dùng những icon trừu tượng như thế này hay bá đạo hơn là nghĩ rằng họ sẽ tò mò mà bỏ thời gian ra tìm hiểu xem nó là cái gì.

{% img center /images/2016/08/06/image_3.png %}

-> Một số icon của Bloom.fm mà thật mình cũng chẳng hiểu nó dùng để làm gì! <-

Nếu bạn là người thiết kế một icon và bạn cảm thấy sản phẩm của mình cần nhãn để người khác có thể hiểu được thì sản phẩm của bạn thật sự có vấn đề, kể cả khi người dùng sẵn sàng hiểu về nó.

Điều này không có nghĩa là bạn không nên dùng icon, thật sự thì có rất nhiều icon mà người dùng đã quen thuộc và phần lớn những chức năng quen thuộc của một ứng dụng đều đã có icon tương ứng (tìm kiếm, phát video, email, cài đặt...). Tuy vậy vẫn có nhiều icon khá là mơ hồ đối với người dùng vì mỗi ứng dụng sẽ có hành vi khác nhau một chút trên cùng một chức năng (ví như chuyện gì xảy ra nếu ta nhấn vào nút trái tim nhỉ (yêu thích, đánh dấu) ??? ).

{% img center /images/2016/08/06/image_4.png %}

Với những tính năng không quen thuộc và phức tạp thì bạn nên sử dụng icon kèm theo nhãn đầy đủ, nhãn sẽ giúp tính năng của bạn rõ ràng hơn và icon sẽ giúp người dùng nhận dạng tính năng nhanh hơn và đem lại một chút cá tính cho ứng dụng của bạn.

{% img center /images/2016/08/06/image_5.png %}

-> Một ví dụ trong ứng dụng Pixelmator. <-

### 3. chuyển hướng dựa vào cử chỉ

Khi Apple giới thiệu Iphone vào năm 2007, công nghệ cảm ứng đa điểm đã thu hút sự chú ý của ngưới dùng và họ thấy rằng không những có thể chạm và nhấn vào giao diện mà còn có thể phóng to, thu nhỏ và vuốt.

Tương tác dùng cảm ứng đã trở nên quen thuộc hơn với người thiết kế giao diện và đã có nhiều ứng dụng được thử nghiệm sử dụng nhận dạng cử chỉ đa điểm để tương tác.

{% img center /images/2016/08/06/image_6.jpg %}

-> Chuyển hướng dựa vào cử chỉ trong ứng dụng Clear. <-

Cũng giống như trường hợp ẩn điều hướng và lạm dụng các icon thay vì dùng nhãn văn bản, đôi khi các nhà thiết kế cũng bị cuốn vào việc sử dụng cử chỉ để tiết kiệm không gian màn hình (Một khi không có biểu tượng nào thể hiện việc bạn có thể vuốt sang trái để xóa thì người dùng chẳng có cách nào để biết là nó tồn tại). Và cũng như vấn đề về hamburger menu, tính năng nào bị dấu đi thì sẽ ít người dùng nó. Thêm nữa là phần lớn nhận dạng cử chỉ chưa được chuẩn và nhất quán trên các  ứng dụng khác nhau - thiết kế giao diện đa điểm vẫn là một lĩnh vực khá mới mẻ. Thậm chí một cử chỉ đơn giản như là vuốt một email sang phải của mỗi ứng dụng mail khác nhau lại có ý nghĩa khác nhau. 

{% img center /images/2016/08/06/image_7.png %}

-> Với Apple mail vuốt sang phải sẽ hiện ra tùy chọn Đánh dấu chưa đọc. <-

{% img center /images/2016/08/06/image_8.png %}

-> Trong khi đó với ứng dụng Gmail thì vuốt sang phải sẽ là chuyển email sang mục lưu trữ. <-

Vậy nên hãy nhớ rằng những tính năng sử dụng nhận dạng cử chỉ là tính năng ẩn và điều đó khiến cho người dùng mất nhiều công sức để ghi nhớ - may mắn lắm thì bạn mới có thể dạy cho cả thế giới biết vuốt sang phải có nghĩa là gì.

### 4. Giới thiệu tính năng mới trực quan trên màn hình cho người dùng mới (Onboarding).

Onboarding, đang là chủ đề nóng trong việc thiết kế giao diện. Tính năng này tự động chạy chỉ dùng một lần khi người dùng lần đầu tiên mở dụng dụng. Phần lớn tính năng này được dùng để giới thiệu và giải thích các tính năng của chương trình một cách trực quan trên màn hình:

{% img center /images/2016/08/06/image_9.png %}

-> Một ví dụ về Onboarding <-

Nhìn thì hay nhưng thật ra thì đây là một giải pháp khá tệ đấy. Bởi vì nhiều người đôi lúc sẽ bỏ qua phần giới thiệu của bạn, họ đang muốn sử dụng ứng dụng của bạn ngay cơ mà. Thậm chí nếu họ dành thời gian xem hướng dẫn của bạn thì họ cũng sẽ nhanh chóng quên mọi thứ ngay khi đóng cửa sổ hướng dẫn đó lại. (đặc biệt là với màn hình hướng dẫn có quá nhiều thông tin). Và cuối cùng là, nếu bạn phải giải thích giao diện của mình với người dùng thì điều đó đồng nghĩa rằng giao diện bạn đang có trên ứng dụng thật sự đang có vấn đề.

{% img center /images/2016/08/06/image_10.jpg %}

-> Việc thiết kế giao diện giống như bạn đang kể truyện cười. Nếu bạn phải giải thích câu chuyện thì chẳng còn gì hay nữa. <-

Onboarding có thể được thiết kế theo nhiều cách khác nhau để trở nên hữu ích hơn đối với người dùng. Như với Slack, màn hình chào của họ tập trung việc giới thiệu khái quát về lợi ích mang lại hơn là giới thiệu chi tiết về các tính năng.

{% img center /images/2016/08/06/image_11.png %}

Duolingo thì biến Onboarding thành các bài học và cổ vũ người dùng học các bài học đấy. Hướng tiếp cận này cũng giúp người dùng quen dần và hiểu hơn các tính năng/ giá trị của ứng dụng.

{% img center /images/2016/08/06/image_12.jpg %}

Bạn còn nhớ vấn đề khác nhau giữa Mailbox và AppleMail khi dùng tính năng vuốt sang phải qua email? đây là cách hướng dẫn người dùng mới về tính năng đó: Người dùng sẽ cần xem những cử chỉ đó được thực hiện như thế nào,và ở đâu trước khi thực sự bắt đầu sử dụng ứng dụng:

{% img center /images/2016/08/06/image_13.png %}

Trước khi áp dụng rập khuôn Onboarding bằng cách tạo một lớp bán trong suốt trên chính ứng dụng của mình để giới thiệu các tính năng và hướng dẫn cho người dùng mới, hãy nên dừng lại và thử nghĩ xem liệu người dùng nên được chào đón như thế nào cho hợp lý và bạn sẽ thấy có nhiều cách giải quyết khác hay hơn việc rập khuôn lại từ ứng dụng khác.

5. Sử dụng màn hình trống

Màn hình trống đôi lúc là một thứ dễ bị bỏ sót bởi các nhân viên thiết kế thiếu kinh nghiệm, tuy nhiên nó là một phần quan trong trong thiết kế ứng dụng của bạn.

Đôi khi bạn nghĩ rằng trang báo lỗi hay màn mình trống là cơ hội tốt để thể hiện tính sáng tạo của mình nhưng thực ra lại không như vậy.

Hãy xem ví dụ dưới đây của Google photos:

{% img center /images/2016/08/06/image_14.png %}

Nhìn qua thì có vẻ ổn nhưng hãy thử nhìn lại màn hình bạn sẽ thấy có một số vấn đề ở đây:

* Tại sao lại có nút tìm kiếm trong khi người dùng chưa tạo cái gì cả?

* Tại sao hình ảnh chính trong màn hình này lại không có phản ứng gì khi tôi chạm vào?

* Gợi ý ở màn hình trên bảo rằng "bạn có thể tạo nội dung bằng cách sử dụng nút + ở phía trên màn hình" và điều đó thật là vụng về, bản thân cái gợi ý ở trên nên tự bao gồm nút để tạo nội dung luôn nhỉ?

Và như thế màn hình trống này không làm cho việc sử dụng ứng dụng dễ dàng hơn, nó không giúp người dùng hiểu rõ hơn về ứng dụng của bạn.

Màn hình trống sẽ làm mọi thứ dễ dàng hơn nếu nó thiết kế theo kiểu dưới đây.

{% img center /images/2016/08/06/image_15.png %}

Đừng quên rằng màn hình trống (tương tự như các trang 404 trên web) không chỉ là nơi thể hiện khả năng sáng tạo và đặc tính thương hiệu mà còn có vai trò quan trọng hơn để thể hiện tính năng của chương trình. Vì vậy hãy làm cho màn hình trống trở nên trực quan hơn.

### 5. Hãy luôn tự hỏi mọi thứ:

Những điều tôi chia sẽ ở đây không phải là để chỉ trích các mẫu thiết kế hay các cách thực hiện tốt nhất. Hãy nhớ rằng các mẫu thiết kế trên các ứng dụng nổi tiếng đôi lúc có đối tượng người dùng khác với ứng dụng mà bạn tạo và điều đó có nghĩa rằng không có chìa khóa vàng chung cho tất cả mọi thứ. Vì thế hay tự nghiên cứu để tạo nên một thiết kế riêng cho mình, mọi thứ cần phải được đo đếm và kiểm thử để rút ra cách giải quyết tốt nhất cho ứng dụng của mình.

Lược dịch từ https://medium.com/@kollinz/misused-mobile-ux-patterns-84d2b6930570

