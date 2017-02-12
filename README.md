## Tim hiểu về CSS
---
  Thực hiện: **Phạm Văn Đạt**

  Cập nhập lần cuối: *12/2/2017*

# Mục lục 

<a href="#1">1.Github</a>
  <ul>
    <li><a href="#Nội dung1">Nội dung</a></li>
    <li><a href="#Công dụng1">Công dụng</a></li>
  </ul>
<a href="#repository1">2.Tạo repository đặt tên là `Web_dev`</a> 
<a href="#Markdown">3.Markdown</a> 
  <ul>
   <li><a href="#Nội dung2">Nội dung</a></li>
   <li><a href="#Công dụng2">Công dụng</a></li>
  </ul>
<a href="#cu phap">4.Cú pháp thường gặp</a> 
<a href="#cài đặt">5.Cài đặt Sublime text</a> 
<a href="#cong cu">6.Các công cụ viết Markdown khác</a>
  <ul>
    <li><a href="#1">Stackedit</a></li>
    <li><a href="#2">Jbt</a></li>
    <li><a href="#3">Tablesgenerator</a></li>
  </ul>

# Nội dung.
---
##1. CSS là gì?.
  - là chữ viết tắt của **Cascading Style Sheets**
  - là ngôn ngữ định dạng cho các ngôn ngữ đánh dấu siêu vă bản như HTML, XML, SVG...
  - Trên website nó đóng vai trò làm đẹp website như chia cột, thêm màu sắc, biến đỏi khối..
<img src="http://2.bp.blogspot.com/-sccGa96-Dpg/V3oY68d-9rI/AAAAAAAAAfU/Wr0gLlUutKAiKp8tMldAmLXQZiCEdIt7QCK4B/s1600/su_dung_ma_mau_hexa_trong_css.PNG">
 - cấu truc của 1 đoạn css.
 ```
 vùng chọn
 {
   thuộc tính: giá trị;
   thuộc tính: giá trị;
   ...
 }
 ```
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
  - Theo kiểu **External style**: Chèn thông qua 1 file nào đó chứa đoạn mã CSS.
      Trên thẻ `<head>` có thẻ
        `<link rel="stylesheet" href="tên_file.css"/>`
      Tạo 1 tệp tin có tên là `tên_file.css`. nếu khác hu mục thì phải viết cả tên thư mục cách nhau bởi dấu `/`
##3. Vùng chọn và các kiểu vùng chọn.
  - Vùng chọn là một khu vục trong website được chỉ định áp dụng một đoạn CSS  nào đó.
  - Có 5 kiểu vùng chọn
    - Chọn theo tên thẻ HTML
        .bên HTML: có 1 đoạn thẻ tiêu đề, bên CSS: h1{....} chon theo kiểu này thì toàn bộ các phần trong các thẻ `h1` ddeuf được chọn
    - Chọn theo ID
         - bên HTML: `<h1 id="ten_id"> </h1>`, bên CSS thì là `#ten_id{....}` thì chỉ chọn 1 thẻ `<h1>` có `id` phù hợp
    + Chọn theo Class
         - bên HTML: `<h1 id="ten_class"> </h1>`, bên CSS thì là `.ten_class{....}` thì sẽ chọn những thẻ có `ten_class` phù hợn
    + Chọn theo thứ cấp
         - bên HTML: có 1 đoạn danh sách, bên CSS: `#id_cua_phan_tu_me ul li{....}` chọn phần tử con. 
         - **chú ý**: bên CSS mỗi phần phải cách ra để phân biệt phần tử mẹ con
    + Chọn thứ cấp liền nhau
        - bên HTML viết những đoạn danh sách lồng nhau, bên CSS: `#id_me ul ul > p{...}` sẽ chọn dững phần tử ngay sau phần phần nhỏ thứ 2, có dấu `>` nên sẽ không chọn những phần nhỏ thứ 3,4...
##4. Các đơn vị đo lường
  - Đơn vị tuyệt đối
     **px**
     **pt**
  - Đơn vị tương đối: Dùng trong các phần tử con
     **%** :Dùng trong các phần tử con
     **em** :Dùng trong các phần tử con
     **rem** :Dùng trong toàn bộ, mà nó căn cứ vào phần tử gốc html.

##5. Các thuộc tính trang trí văn bản

 - **text-align**: Căn lề văn bản(left-trái/right-phải/center-giữa/justify-đều 2 bên)
 - **text-decoration**: thêm gạch(underline-dưới/overline-trên/line-throught-giữa/none-không trang trí theo kiểu này nữa) 
 - **text-indent**: (px) tạo khoảng trống bên trái văn bản
 - **text-shadow**: mau_sắc tọa_độ_x(px) tọa_đọ_y(px) kíck_thước_bóng_mờ(px) đổ bóng văn bản
 - **text-transform**: capitalize(hoa chữ đầu)/uppercase(hoa hết)/lomercase(thường hết)/normal(trở về)

##6. Các thuộc tính trang trí chữ viết

 - **font-family**: Arial, Tahoma, sans-serif; tên font chữ
 - **font-style**: italic(in nghiêng)/oblique(in nghiêng)/normal(quay lại bt) chữ in nghiêng
 - **font-weight**: 100/20..(cao nhất là 900)/normal(bt)tùy trỉnh độ đậm nhạt
 - **Color**: tên màu chữ

##7. Phần tử Block và Inline

 - **Block**(khối) là phần tử HTML khi tạo ra nó sở hữu một hàng riêng biệt.vd `<div>,<h1>,<p>,<ul>...`
 - **Inline**(nội dung) là cá phần tử HTML khi tọa ra có thể đứng trên cùng một hàng.vd `<stong>,<span>,<a>...`
##8. Thẻ **div** và vai trò khi tạo bố cục
 - Thẻ `<div>` là một thẻ block dùng để gọp nhiều nhóm phần tử lại thành một khu vực.Thườngđược dùng đẻ tạo bố cục hoặc tạ một khu vực nào đó trong website 
 - ví dụ: `<div id="..">....</div>`

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

##10. Tùy chỉnh kích thước box (block)

 - **max-height**: cao_tối_đa(px);
 - **min-height**: thấp_tối_đa(px);
 - **max-width**: rộng_tối_đa;
 - **min-width**: hẹp_tối_đa;

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
