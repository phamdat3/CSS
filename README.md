## Tim hiểu về CSS
---
  Thực hiện: **Phạm Văn Đạt**

  Cập nhập lần cuối: *12/2/2017*

# Mục lục 
 
[1. CSS là gì?](#1)

[2. Nhúng css vào website.](#2)

[3. Vùng chọn và các kiểu vùng chọn.](#3) 

[4. Các đơn vị đo lường](#4) 

[5. Các thuộc tính trang trí văn bản](#5) 

[6. Các thuộc tính trang trí chữ viết](#6)

[7. Phần tử Block và Inline](#7) 

[8. Thẻ div và vai trò khi tạo bố cục](#8) 

[9. Kỹ thuật Box Model cơ bản](#9)

[10. Tùy chỉnh kích thước box (block)](#10) 

[11. Tính toán lại kích thước của box với box-sizing.](#11)

[12. Thêm nền cho block](#12)

[13. Float và Clear Float](#13)

[14. Reset CSS là gì](#14)

[15. Trang trí danh sách với list-style](#15)

[16. Thuộc tính display](#16)

[17. Thuộc tính position](#17)

[18. Pseudo-classes cơ bản](#18)

[19. Cách làm menu ngang dropdown cơ bản](#19)

[20. Làm menu dọc có dropdown đơn giản](#20)

[21. Thiết kế giao diện đơn giản](#21)

[22. CSS Framework là gì và cách sử dụng](#22)

[23. Tạo chuyển động với Transition](#23)

[24. Thay đổi hình dạng đối tượng với Transform](#24)

# Nội dung.
---
<a name="1"></a>
##1. CSS là gì?.
  - là chữ viết tắt của **Cascading Style Sheets**
  - là ngôn ngữ định dạng cho các ngôn ngữ đánh dấu siêu vă bản như HTML, XML, SVG...
  - Trên website nó đóng vai trò làm đẹp website như chia cột, thêm màu sắc, biến đỏi khối..
<img src="http://2.bp.blogspot.com/-sccGa96-Dpg/V3oY68d-9rI/AAAAAAAAAfU/Wr0gLlUutKAiKp8tMldAmLXQZiCEdIt7QCK4B/s1600/su_dung_ma_mau_hexa_trong_css.PNG">
<img src="https://thachpham.com/wp-content/uploads/2015/04/html-css-webpage.png">
<img src="http://blogloi.com/wp-content/uploads/2015/12/thiet-ke-layout-web-bang-css-02.jpg">
 - cấu truc của 1 đoạn css.
 ```
 vùng chọn
 {
   thuộc tính: giá trị;
   thuộc tính: giá trị;
   ...
 }
 ``` 

<a name="2"></a>
##2. Nhúng css vào website.
  - Theo kiểu **Inline style**: Chèn trực tiếp vào HTML luôn.
    + Cách chèn
      Trên thẻ `<head>` có thẻ:
       ```
       <style type="text/css">
         p {
             các thuộc tính.
           }
       </style>
       ```
  <img src="http://imageshack.com/a/img922/9213/e8MGNa.png">
  - Theo kiểu **External style**: Chèn thông qua 1 file nào đó chứa đoạn mã CSS.
      Trên thẻ `<head>` có thẻ
        `<link rel="stylesheet" href="tên_file.css"/>`
      Tạo 1 tệp tin có tên là `tên_file.css`. nếu khác hu mục thì phải viết cả tên thư mục cách nhau bởi dấu `/`

<a name="3"></a>
##3. Vùng chọn và các kiểu vùng chọn.

  - Vùng chọn là một khu vục trong website được chỉ định áp dụng một đoạn CSS  nào đó.
  - Có 5 kiểu vùng chọn
    - Chọn theo tên thẻ HTML
        .bên HTML: có 1 đoạn thẻ tiêu đề, bên CSS: h1{....} chon theo kiểu này thì toàn bộ các phần trong các thẻ `h1` ddeuf được chọn
<img src="http://imageshack.com/a/img924/2461/EkJRtO.png">
    - Chọn theo ID
         - bên HTML: `<h1 id="ten_id"> </h1>`, bên CSS thì là `#ten_id{....}` thì chỉ chọn 1 thẻ `<h1>` có `id` phù hợp
<img src="http://imageshack.com/a/img924/7463/oNnZoj.png">
    + Chọn theo Class
         - bên HTML: `<h1 id="ten_class"> </h1>`, bên CSS thì là `.ten_class{....}` thì sẽ chọn những thẻ có `ten_class` phù hợn
<img src="http://imageshack.com/a/img924/7232/PxHaXd.png">
    + Chọn theo thứ cấp
         - bên HTML: có 1 đoạn danh sách, bên CSS: `#id_cua_phan_tu_me ul li{....}` chọn phần tử con. 
         - **chú ý**: bên CSS mỗi phần phải cách ra để phân biệt phần tử mẹ con
<img src="http://imageshack.com/a/img922/7743/skhYya.png"> 
    + Chọn thứ cấp liền nhau
<img src="http://imageshack.com/a/img922/2368/ojLfgT.png">
        - bên HTML viết những đoạn danh sách lồng nhau, bên CSS: `#id_me ul ul > p{...}` sẽ chọn dững phần tử ngay sau phần phần nhỏ thứ 2, có dấu `>` nên sẽ không chọn những phần nhỏ thứ 3,4...

<a name="4"></a>
##4. Các đơn vị đo lường

  - Đơn vị tuyệt đối

     **px**

     **pt**
<img src="http://imageshack.com/a/img924/4320/DJbSB3.png">

  - Đơn vị tương đối: Dùng trong các phần tử con

     **%** :Dùng trong các phần tử con

     **em** :Dùng trong các phần tử con

     **rem** :Dùng trong toàn bộ, mà nó căn cứ vào phần tử gốc html.

<a name="5"></a>
##5. Các thuộc tính trang trí văn bản

 - **text-align**: Căn lề văn bản(left-trái/right-phải/center-giữa/justify-đều 2 bên) 
<img src="http://imageshack.com/a/img923/8086/U6Jfcn.png">
 - **text-decoration**: thêm gạch(underline-dưới/overline-trên/line-throught-giữa/none-không trang trí theo kiểu này nữa) 
<img src="http://imageshack.com/a/img923/4412/rohAKl.png"> 
 - **text-indent**: (px) tạo khoảng trống bên trái văn bản
 - **text-shadow**: mau_sắc tọa_độ_x(px) tọa_đọ_y(px) kíck_thước_bóng_mờ(px) đổ bóng văn bản
<img src="http://imageshack.com/a/img923/8276/H5QoP7.png">
 - **text-transform**: capitalize(hoa chữ đầu)/uppercase(hoa hết)/lomercase(thường hết)/normal(trở về)
<img src="http://imageshack.com/a/img923/6011/cbndlw.png">

<a name="6"></a>
##6. Các thuộc tính trang trí chữ viết

 - **font-family**: Arial, Tahoma, sans-serif; tên font chữ
 - **font-style**: italic(in nghiêng)/oblique(in nghiêng)/normal(quay lại bt) chữ in nghiêng
 - **font-weight**: 100/20..(cao nhất là 900)/normal(bt)tùy trỉnh độ đậm nhạt
 - **Color**: tên màu chữ

<a name="7"></a>
##7. Phần tử Block và Inline

 - **Block**(khối) là phần tử HTML khi tạo ra nó sở hữu một hàng riêng biệt.vd `<div>,<h1>,<p>,<ul>...`
 - **Inline**(nội dung) là cá phần tử HTML khi tọa ra có thể đứng trên cùng một hàng.vd `<stong>,<span>,<a>...`
<img src="http://imageshack.com/a/img924/825/LtC0ve.png">

<a name="8"></a>
##8. Thẻ **div** và vai trò khi tạo bố cục

 - Thẻ `<div>` là một thẻ block dùng để gọp nhiều nhóm phần tử lại thành một khu vực.Thườngđược dùng đẻ tạo bố cục hoặc tạ một khu vực nào đó trong website 
 - ví dụ:
 <img src="http://imageshack.com/a/img924/8703/Ch3UNg.png">

<a name="9"></a>
##9. Kỹ thuật Box Model cơ bản

 - Box model là kỹ thuật để tinh chỉnh lại các phần tử box(block)
 - Box model gồm 4 thành phần chính:
   . **Margin**: Lề bên ngoài box
   . **Borde**: Viền của box
   . **Padding: Phần lót bên trong box ngăn cách với nội dung
   . **Content**: Phần nội dung bên trong box
 - Cách dùng
   **margin**: trên(px) phải dưới trái;/margin-top: trên(px);/margin: (px);/margin:trên&dưới(px) trái&phải;
   **borde**: độ-dày loại_viền màu_viền;
   *các loại viền*: double/solid/dotted/groove/inset/outset...
  **padding**:(giống margin)
<img src="http://imageshack.com/a/img924/6531/GDjy6c.png">
<img src="http://imageshack.com/a/img923/3143/a5YDDs.png">

<a name="10"></a>
##10. Tùy chỉnh kích thước box (block)

 - **max-height**: cao_tối_đa(px);
 - **min-height**: thấp_tối_đa(px);
 - **max-width**: rộng_tối_đa;
 - **min-width**: hẹp_tối_đa;

<a name="11"></a>
##11. Tính toán lại kích thước của box với box-sizing.

 - khi dùng thì tổng chu vi của **box** không đổi
 - **box-sizing**: content-box(mặc định);/border-box;/padding-box;
 - Chọn tất cả các phần tử để căn chỉnh.
```
   *{
      box-sizing: border-box;
      -moz-box-sizing: border-box;(để cho mấy trình duyệt cũ vẫn đọc được)
      -webkit-box-sizing: borber-box;(để cho mấy trình duyệt cũ vẫn đọc được)
   }
```

<a name="12"></a>
##12. Thêm nền cho block

 - Màu nền
   `backgruad-clolor: mã_màu(có dấu **#** ở trước)/tên_màu;`
 - Ảnh nền
   ```
   background-image: url('link_ảnh')
     width: (rộng);
     height: (px);
     background-repeat: no-repeat(không lặp ảnh);/repeat-x(lặp ngang);/repeat-y(lặp dọc);/space(lặp đều);...
  ```
<img src="http://imageshack.com/a/img923/9808/mJFAwg.png">

<a name="13"></a>
##13. Float và Clear Float
 - clear float là tạo neo để cho các phàn tử con không bị tràn ra khỏi phần tử mẹ.
 - có 2 cách tạo clear float:
  + bên HTML tạo 1 thẻ `<div>` trống ở cuối cùng. thuộc tính clear: both; ơt thẻ `<div>` trống này sẽ như là cái neo hay cái dới hạn mà k cho các phần tử con chạy ra ngoài đk.
  + tại thẻ `<div>` me ta cho thuộc tính overfloat: auto;
 - **chú ý**: tại thẻ mẹ và những thẻ con chúng ta phải tùy chỉnh chiều rộng sao cho phù hợn thì những nọi dung của các thẻ `<div>` con sẽ tạo thành những cột riêng biệt nằm cạnh nhau trên cùng 1 hàng.

<a name="14"></a>
##14. Reset CSS là gì
 - reset trên mạng, có 2 cách:
  + **normalize.css.** download về và tạo 1 file css sau đó chèn vào html(để lên trước để cho nó chạ trước)
  + **meyerweb css tools.** copy và làm như cách trên.

<a name="15"></a>
##15. Trang trí danh sách với list-style
 - list-style-type: disc(dấu chấm tron);/clrele(dường tròn);/aquare(vuông);decimai(so);/nome(k có gì);
 - list-style-position: inside;/outside;
 - list-style-image: url('linh anh');

<a name="16"></a>
##16. Thuộc tính display
 - **Block**: Các phần tử hiển thị trên mỗi hàng riêng biết. Như thẻ `<div>`, `<li>`, `<h1>`,....
 - **Inline**: Các phần tử hiển thi trên cùng 1 hàng.Như các thẻ `<span>`, `<strong>`, `<a>`,....
 - Chuyển phần tử về cùng một hàng nhờ thẻ `display: inline`
 <img src="http://imageshack.com/a/img922/4051/DY1sGf.png">
 - Chuyển phần thử về cùng 1 hàng nhưng vẫn mang các đặc tính của block như có thể tùy chỉnh kích thước hoặc màu nền.
 - Chuyển phần tử về hàng riêng biệt.
 <img src="http://imageshack.com/a/img922/358/XI4YFr.png">
 - Chuyển phần tử giống như danh mục (như dùng thử `<div>`)
 
<a name="17"></a>
##17. Thuộc tính position
 - position: relative(không thay đổi);
             top: (px);/bottom: (px); chạy xuống lên
             left: (px);/right: (px); chạy phải trái

<a name="18"></a>
##18. Pseudo-classes cơ bản
  Một số Pseudo Class thông dụng
 Cho 1 thẻ:
 <img src="http://imageshack.com/a/img922/5417/MsUIWz.png">
 - **hover**: Chọn trạng thái khi rê chuột vào một phần tử.
 <img src="http://imageshack.com/a/img922/235/F9Mmfb.png">
 - **visited**: Được sử dụng cho liên kết, chọn liên kết khi đã được truy cập (dựa vào History trên trình duyệt).
 - **link**: Được sử dụng cho liên kết, chọn liên kết khi chưa nhấp vào
 - **active**: Chọn phần tử khi họ chọn/nhấp vào.
 <img src="http://imageshack.com/a/img924/6383/EFzXoT.png">
 
<a name="19"></a>
##19. Cách làm menu ngang dropdown cơ bản
 - Trước tiên phải tạo một danh sách bằng thẻ `<li>`, chú ý danh sách được tạo ra phải nắm trong một thẻ `<div>`.
 - Tiếp theo xóa dấu chấm ở đầu dòng mõi danh mục, thêm màu nền cho thẻ `<div>` hay nói cách khác là vùng chọn và căn chúng ra giữa.
 <img src="http://imageshack.com/a/img924/5277/bEualf.png">
 - Tiếp theo dùng thuộc tính `display` để cho các thu mục nằm trên cùng một hàng và căn chỉnh chiều cao và chiều rộng của vùng chọn và để cho mỗi thư mục các đều nhau thì cho thuộc tính `line-height` bằng với `height`.
 <img src="http://imageshack.com/a/img923/9163/8602Y2.png">
 - Tiếp theo xóa gạch chân ở dưới mỗi mục và chọn màu chữ cho các mục.
 <img src="http://imageshack.com/a/img922/7126/WnS0al.png">
 - Để khi rê chuột tới thư muc đó để dễ nhận biết ta cho màu nền của mục rê tới có màu nền khác và màu chữ khác đi
 <img src="http://imageshack.com/a/img924/5569/STaSun.png">
 - Khi có thêm thư mục con ở một mục nào đó:
   + Tạo thư mục con cho mục tương ứng. Chú ý là tạo thêm thư mục con ở thẻ `<li>` thì phải tạo thêm 1 thẻ `<ul>` nữa.
 <img src="http://imageshack.com/a/img923/6007/JNwhqZ.png">
   + Vì các thu mục con nằm trên thư mục mẹ và làm vùng chọn bị lớn ra nên ta ản vùng chọn con đi.
 <img src="http://imageshack.com/a/img924/4463/oFXt2S.png">
   + Ẩn rồi thì phải hiện thư mục con lên. Khi rê chuột tới thì thư muc con hiện lên.
 <img src="http://imageshack.com/a/img923/2680/AjahBX.png">

<a name="20"></a>
##20. Làm menu dọc có dropdown đơn giản
 - Tương tự làm menu ngang:
 <img src="http://imageshack.com/a/img922/9607/wKEykw.png">
 - Khác những phàn sau:
   + Không cho các phần tử cùng nằm trên 1 hàng nên phải tạo cho chúng một bảng riêng để phân cách chúng ra. Dùng thuộc tính `border-bottom` để tạo bảng, `padding: o 1em` để cho chũng lùi đâu dòng 1em và `display: block` để tạo vùng riêng cho chúng.
   <img src="http://imageshack.com/a/img924/8592/qkXxiT.png">
   + Khi tạo thê thư mục con thì chũng ta dùng thêm các thuộc tính để căn chỉnh: `left` đê đẩy cho các mục con ra ngoài không bị chồng lên các mục sau( chú ý tới kích thước) `top:0` để cho thư mục con nắm ngnag hàng với thu mục mẹ sang.
   <img src="http://imageshack.com/a/img922/2746/MWNx3a.png">


<a name="21"></a>
##21. Thiết kế giao diện đơn giản

<a name="22"></a>
##22. CSS Framework là gì và cách sử dụng
 - **CSS Framework** là bộ mã nguồn CSS đã được viết sẵn để chúng ta có thể sử dụng trong bất kỳ dự án nào.
 - **Chức năng** là có sẵn các định dạng trang trí cho phần tử Website như tạo menu, nút bấm, chia cột.
 - **Mục đích** là hỗ trợ thiết kế website nhanh hơn cứ không phải viết CSS từ đầu.
 - Có hai lại CSS Framework cơ bản nhất:
   + **Grib Framework**: Bộ CSS Framework chuyên cho mục đích chia cột website.
   + **UI Framework**: Bộ CSS hoàn chỉnh bao gồm các thành phần cho website như menu, nút bấm, from,..
 - Những bộ CSS Framework phổ biến nhất:
   + [Bootstrap](http://getbootstrap.com/css/): Phổ biết nhất, vì nó rất đầy đủ nhưng phúc tạp dành cho những người thành thục rồi.
    <img src="http://imageshack.com/a/img922/3055/b04XxV.png">
   + [960 Grid system](http://960.gs/): Khá đơn giản dễ hiểu dành cho những người mới học CSS, dùng đê chia cột.
   <img src="http://imageshack.com/a/img922/5077/lxaIRw.png">
   + [Purecss](https://purecss.io/): Chia cột, cấu trúc rất dễ hiểu.
   <img src="http://imageshack.com/a/img923/3244/7C5fJQ.png">
   + [Golden grid system](http://goldengridsystem.com/): Chia cột và đơn giản.
   <img src="http://imageshack.com/a/img922/9484/ornT2Y.png">
   + [Foundation](http://foundation.zurb.com/develop/getting-started.html): Cũng dễ sử dụng. Nên sử dụng khi đã sử dụng 960 Grid system và Purecss rồi.
   <img src="http://imageshack.com/a/img924/7735/1hImvN.png">
 
<h3>Hướng dẫn sử dụng Framework với bộ Purecss</h3>

 - Bước 1: Tải bộ framework về máy, nó sẽ bao gồm các file CSS và Javascript (nếu có) và một tài liệu HTML mẫu.
 - Bước 2:  Sau đó bạn tiến hành nhúng các file CSS của framework đó vào tài liệu bạn cần thiết kế với thẻ `<link>`.
 - Bước 3: Cuối cùng là thêm class của framework vào các phần tử bạn muốn sử dụng.
 - *Lời kết*: Mỗi Framework có một vấn đề khác nhau nên khó có thể làm ví dụ cụ thể được. Vì thế nấu muốn sử dụng hay bắt đầu từ **960Grid** bắng cách tải về máy va chia cột vói các class như hướng dẫn, nấu bạn chưa biết class của nó thì mở tài liệu HTML lên sẽ thấy.

<a name="23"></a>
##23. Tạo chuyển động với Transition
 - **Transition** là một trong các kỹ thuật phổ biến ở các website hiện đại là có các hiệu ứng chuyển động cho từng đối tượng rất đẹp mắt được làm hoàn toàn bằng CSS3.
 - Cấu trúc khai báo lệnh: 
   transition: [thuộc tính chuyển động] [thời gian chuyển động] [thời gian delay] [kiểu chuyển động]; 
   + Thuộc tính chuyển động: Bắt buộc có, bạn có thể tham khảo những thuộc tính chuyển động [tại đây](https://www.w3.org/TR/css3-transitions/#animatable-properties). Khi tạo hiệu ứng chuyển động là bạn phải đặt thuộc tính `transition` vào phần tử muốn làm chuyển động.
   + Kiểu chuyển động: Có thể có hoặc không, các kiểu chuyển động tham khảo [tại đây](https://developer.mozilla.org/en-US/docs/Web/CSS/single-transition-timing-function).
 - Chú ý: Transition là thuộc tính CSS3 nên bạn cần nên khai báo thêm hai thuộc tính tương tự kèm hai tiền tố -moz- và -webkit- để nó hoạt động tốt trên mọi trình duyệt.
 - Ví dụ:
   <img src="http://imageshack.com/a/img922/396/Nw4KYI.png">
   + Khi rê chuột vào:
   <img src="http://imageshack.com/a/img922/9900/foKve6.png">
   <img src="http://imageshack.com/a/img923/9825/PXjJbi.png">
   + Khi bỏ chuột ra:
   <img src="http://imageshack.com/a/img922/5417/lvpn6p.png">

<a name="24"></a>
##24. Thay đổi hình dạng đối tượng với Transform
 - Ngoài thuộc tính `transition` của CSS3 giúp bạn tạo ra các hiệu ứng chuyển động của các phần tử trong website, thì nó còn một thuộc tính khác được sử dụng kèm với `transition` rất thường xuyên đó là thuộc tính `transform` có chức năng đổi hình dạng các phần tử block trong website.
###Tính năng xoay: rotate();
 - <img src="http://imageshack.com/a/img924/4149/gBMkxR.png">
 - Khi rê chuột vào hình trên:
  <img src="http://imageshack.com/a/img922/3888/OFQmtE.png">
 - Khi rê chuột vào hình dưới: Nó xẽ xoay liên tục.
  <img src="http://imageshack.com/a/img924/413/t7nmZt.png">
###Tính năng co giãn: scale();
 - <img src="http://imageshack.com/a/img923/4791/4Nh4dc.png">
 - Khi rê chuột vào hình trên:
 <img src="http://imageshack.com/a/img923/6267/ObYmVa.png">
 - Khi rê chuột vào hình dưới: nó xẽ to dần ra.
 <img src="http://imageshack.com/a/img924/1006/ecCbHU.png">
###Tính năng kéo nghiêng: skew();
 - <img src="http://imageshack.com/a/img924/9295/xlNv9Y.png">
 - Khi rê chuột vào hình trên:
 <img src="http://imageshack.com/a/img923/1754/Wb3VTY.png">
 - Khi rê chuột vào hình dưới: nó xẽ nghiêng từ từ.
 <img src="http://imageshack.com/a/img922/4923/pLxfWd.png">
###Tính năng tùy chỉnh tâm hịnh dạng: transform-origin;
 - Loại rotale:
 <img src="http://imageshack.com/a/img922/6188/NrfOKR.png">
 <img src="http://imageshack.com/a/img921/7945/IuZNGM.png">
 - Loại scale:
 <img src="http://imageshack.com/a/img923/2372/yNeEsL.png">
 <img src="http://imageshack.com/a/img922/5452/3k0BWN.png">
 - Loại skew:
 <img src="http://imageshack.com/a/img922/6243/Hu9EXr.png">
 <img src="http://imageshack.com/a/img921/9613/zbVHMQ.png">
 

