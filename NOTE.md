# PHÂN TÍCH 
MAIN
- Header(<Header> .header)
    NavBar (<nav> .navbar)        
    Search
- Container(<div> .container)
- Footer(<footer> .footer)
# FONT-SIZE
- Mặc định: 16px (100%)
- Set font-size(html) = 62.5% - 1rem = 10px
# BOX_SIZING
- box-sizing: inherit (*) : Set các thẻ child sẽ kế thừa thẻ parent
- box-sizing: border-box (html - thẻ parent max): nên các thẻ child của thẻ parent(html) sẽ kế thừa box-sizing: border-box
# RESPONSIVE
- Tối ưu hiển thị trên các kích thước màn hình khác nhau.
- (1) Đặt base responsive:
    .grid {
    width: 1200px;
    max-width: 100%;
    margin: 0 auto;
    }
        Kích thước màn hình >1200px => Kích thước tối đa của .grid là 1200px.
        Kích thước màn hình <1200px thì max-width:100% => Giảm kích thước .grid bằng kích thước màn hình mà <1200px.
        Tự động căn giữa .grid khi .grid nằm trong một khối khác.

    .grid__full-width {
    width: 100%;
    }
        Dùng khi không muốn đặt kích thước màn hình bằng 1200px.
    
    .grid__row {
    display: flex;
    flex-wrap: wrap;
    }
        Set nằm trên cùng một hàng ngang (row).
        wrap: Đẩy xuống hàng nếu tràn màn hình nằm ngang.
# DISPLAY: BLOCK
Thẻ có tính chất này sẽ kế thừa chiều ngang của thẻ chứa nó.
(html có display:block sẽ kế thừa chiều ngang của trình duyệt)
# LIST-STYLE: NONE
Bỏ dấu chấm đầu dòng của thẻ ul,li.
Ngoài ra, Thẻ ul còn có padding-left mặc định là 40px.
# DISPLAY: FLEX
- Gắn tại thẻ parent
- justify-conten: flex-start/end; center ; space-between/around
- align-content: flex-start/end ; center

- justify-self: flex-start/end; center
- align-self:  flex-start/end ; center

- flex-direction: row/column: Thay đổi hướng của main axis.
- flex-wrap: nowrap/wrap/wrap-reverse : Thay đổi chiều cross start/end.
- flex-basic: <length>: Kích thước main size.
- flex-grow: <number>: Kích thước main size khi phóng to.
- flex-shrink: <number>: Kích thước main size khi thu nhỏ.
- flex: grow | shrink | basis : short-hand.
- flex-flow: direction | wrap : short-hand.
- order: <number>: Thay đổi chiều main start/end.
# TEXT-DECORATION: NONE
Bỏ gạch chân của thẻ a.
# FONT_WEIGHT: <number>
Thay đổi độ dày của chữ
# TRANSFORM: translateY(-50%)
Đạt kích thước bằng - 50% kích thước chiều cao (height) của chính nó.
# :first-child  = nth-child(1)
# .header__navbar-item--has-qr:hover .header__qr
{
    display: block;
}
.header__qr {
    display: none;
}
Khi ta hover vào .header__navbar-item--has-qr
thì sẽ CSS display: block; vào .header__qr
# line-height
Chiều cao của dòng.
# text-align
Căn chữ
# user-select: none;
Di chuột, không cho copy.
# transform-origin: top right
Đổi tâm transform.
# will-change: opacity, transform;
Trình duyệt tối ưu chuyển động.
# z-index
Đổi layer
# Ctrl [ or Ctrl ]
Di chuyển code.
# Border-radius
Bo góc.
# box-shadow: 0 0 3px #ccc
Đổ bóng
# .header__search-input:focus ~ .header__search-history
{
    display: block;
}
.header__search-history {
    display: none;
}
Khi ta nhấp chuột vào ô input hiện ra lịch sử tìm kiếm
# Dấu ... khi một dòng
text-overflow: ellipsis;
    white-space: nowrap;
# Transition
Định nghĩa ra animation (...) áp animation linear 0.1s
# Checkbox
Nhấn vào icon search => thanh tìm kiếm
<!-- <label for="mobile-search-checkbox" class="header___mobile-search">
    <i class="header___mobile-search-icon fas fa-search"></i>
</label>

<input type="checkbox" hidden id="mobile-search-checkbox">
//CSS
.header__search-checkbox:checked ~ .header__search {
    display: flex;
} -->
# Khi đối tượng con vượt quá đối tượng cha theo trục x thì hiện thanh scroll để kéo
overflow-x: auto; (.mobile-category__list)
# Khi đối tượng con nằm trong thẻ cha bị giới hạn kích thước thì co lại
flex-shrink: 0; (.mobile-category__item)
# Bỏ highlight khi chọn đối tượng trên mobile
-webkit-tap-highlight-color: transparent; (.header__cart-wrap)
# Truy cập điện thoại (Cùng mạng wifi)
Terminal -> New terminal -> Gõ ipconfig
Xem IPv4 Address
Trên đt gõ: Địa chỉ ipv4 trên máy tính : port trên live server trên máy tính (:5500)
=> Truy cập