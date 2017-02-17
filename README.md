## Tim hiểu về CSS
---
  Thực hiện: **Phạm Văn Đạt**

  Cập nhập lần cuối: *12/2/2017*

# Mục lục 
 
<a href="#1">1. CSS là gì?</a>  

<a href="#2">2. Nhúng css vào website.</a> 

<a href="#3">3. Vùng chọn và các kiểu vùng chọn.</a> 

<a href="#4">4. Các đơn vị đo lường</a> 

<a href="#5">5. Các thuộc tính trang trí văn bản</a> 

<a href="#6">6. Các thuộc tính trang trí chữ viết</a> 

<a href="#7">7. Phần tử Block và Inline</a> 

<a href="#8">8. Thẻ div và vai trò khi tạo bố cục</a> 

<a href="#9">9. Kỹ thuật Box Model cơ bản</a> 

<a href="#10">10. Tùy chỉnh kích thước box (block)</a> 

<a href="#11">11. Tính toán lại kích thước của box với box-sizing.</a> 

<a href="#12">12. Thêm nền cho block</a> 

<a href="#13">13. Float và Clear Float</a>

<a href="#14">14. Reset CSS là gì</a>

<a href="#15">15. Trang trí danh sách với list-style</a>

<a href="#16">16. Thuộc tính display</a>

<a href="#17">17. Thuộc tính position</a>

<a href="#18">18. Pseudo-classes cơ bản</a>

<a href="#19">19. Cách làm menu ngang dropdown cơ bản</a>

<a href="#20">20. Làm menu dọc có dropdown đơn giản</a>

<a href="#21">21. Thiết kế giao diện đơn giản</a>

<a href="#22">22. CSS Framework là gì và cách sử dụng</a>

<a href="#23">23. Tạo chuyển động với Transition</a>

<a href="#24">24. Thay đổi hình dạng đối tượng với Transform</a>

# Nội dung.
---
<id="1>
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

<id="2>
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

<id="3>
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

<id="4>
##4. Các đơn vị đo lường

  - Đơn vị tuyệt đối

     **px**

     **pt**
<img src="http://imageshack.com/a/img924/4320/DJbSB3.png">

  - Đơn vị tương đối: Dùng trong các phần tử con

     **%** :Dùng trong các phần tử con

     **em** :Dùng trong các phần tử con

     **rem** :Dùng trong toàn bộ, mà nó căn cứ vào phần tử gốc html.

<id="5>
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

<id="6>
##6. Các thuộc tính trang trí chữ viết

 - **font-family**: Arial, Tahoma, sans-serif; tên font chữ
 - **font-style**: italic(in nghiêng)/oblique(in nghiêng)/normal(quay lại bt) chữ in nghiêng
 - **font-weight**: 100/20..(cao nhất là 900)/normal(bt)tùy trỉnh độ đậm nhạt
 - **Color**: tên màu chữ

<id="7>
##7. Phần tử Block và Inline

 - **Block**(khối) là phần tử HTML khi tạo ra nó sở hữu một hàng riêng biệt.vd `<div>,<h1>,<p>,<ul>...`
 - **Inline**(nội dung) là cá phần tử HTML khi tọa ra có thể đứng trên cùng một hàng.vd `<stong>,<span>,<a>...`
<img src="http://imageshack.com/a/img924/825/LtC0ve.png">

<id="8>
##8. Thẻ **div** và vai trò khi tạo bố cục

 - Thẻ `<div>` là một thẻ block dùng để gọp nhiều nhóm phần tử lại thành một khu vực.Thườngđược dùng đẻ tạo bố cục hoặc tạ một khu vực nào đó trong website 
 - ví dụ:
 <img src="http://imageshack.com/a/img924/8703/Ch3UNg.png">

<id="9>
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

<id="10>
##10. Tùy chỉnh kích thước box (block)

 - **max-height**: cao_tối_đa(px);
 - **min-height**: thấp_tối_đa(px);
 - **max-width**: rộng_tối_đa;
 - **min-width**: hẹp_tối_đa;

<id="11>
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

<id="12>
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

<id="13>
13. Float và Clear Float
 - clear float là tạo neo để cho các phàn tử con không bị tràn ra khỏi phần tử mẹ.
 - có 2 cách tạo clear float:
  + bên HTML tạo 1 thẻ `<div>` trống ở cuối cùng. thuộc tính clear: both; ơt thẻ `<div>` trống này sẽ như là cái neo hay cái dới hạn mà k cho các phần tử con chạy ra ngoài đk.
  + tại thẻ `<div>` me ta cho thuộc tính overfloat: auto;
 - **chú ý**: tại thẻ mẹ và những thẻ con chúng ta phải tùy chỉnh chiều rộng sao cho phù hợn thì những nọi dung của các thẻ `<div>` con sẽ tạo thành những cột riêng biệt nằm cạnh nhau trên cùng 1 hàng.

<id="14>
14. Reset CSS là gì
 - reset trên mạng, có 2 cách:
  + **normalize.css.** download về và tạo 1 file css sau đó chèn vào html(để lên trước để cho nó chạ trước)
  + **meyerweb css tools.** copy và làm như cách trên.

<id="15>
15. Trang trí danh sách với list-style
 - list-style-type: disc(dấu chấm tron);/clrele(dường tròn);/aquare(vuông);decimai(so);/nome(k có gì);
 - list-style-position: inside;/outside;
 - list-style-image: url('linh anh');

<id="16>
16. Thuộc tính display
 - display: inline(2 thẻ hiển thị trên 1 hàng); block(bt); list-item(chuyển thẻ `<div>` giống thẻ ``<li>);/table(tạo bảng với nhiều thẻ <div>);``

<id="17>
17. Thuộc tính position
 - position: relative(không thay đổi);
             top: (px);/bottom: (px); chạy xuống lên
             left: (px);/right: (px); chạy phải trái

<id="18>
18. Pseudo-classes cơ bản

<id="19>
19. Cách làm menu ngang dropdown cơ bản

<id="20>
20. Làm menu dọc có dropdown đơn giản

<id="21>
21. Thiết kế giao diện đơn giản

<id="22>
22. CSS Framework là gì và cách sử dụng

<id="23>
23. Tạo chuyển động với Transition

<id="24>
24. Thay đổi hình dạng đối tượng với Transform