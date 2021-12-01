# Cookie Arena Season 1
## Cryptography
### XOR
#### Challenge
> [File_1](encrypt.py) 
> [File_2](cipher.txt)
---
#### Solution
- Đề cung cấp cho mình 1 bản cipher và 1 bản encrypt để decrypt cipher ra plan text.
- Và bài này cũng đã hint rõ đây là xor cipher nên mình đã thử brute bằng tool trước và đã lấy được flag.
### MORSE
#### Challenge
Suỵt! Tập trung và đeo tai nghe lên nào. Gà có nghe thấy nhịp beat không? Họ nói gì từ bên kia chiến tuyến Format: Flag{what_you_find}
> [File](cipher.wav)
---
#### Solution
- Bài này đơn giản là mình sẽ phải decode đoạn âm thanh morse và mình đã dùng web có sẵn:
https://morsecode.world/international/decoder/audio-decoder-adaptive.html
- Flag{M.O.R.S.E.C.O.D.E}
### Julius Caesar
#### Challenge
Vô tình khi khai quật khảo cổ, Gà tìm được một thông điệp bí ẩn khoảng hơn 100 năm trước công nguyên. Nghe đồn đây là một bí thuật đã bị thay đổi công thức của một vị tướng Julius Caesar, sau này trở thành vị vua đầu tiên của đế chế La Mã hùng mạnh.
Hãy giúp Gà giải mật thư này!
> [File](caesar.txt)
---
#### Solution
- Từ đề bài => Caecar cipher
- Decode bằng trang:
https://www.dcode.fr/caesar-cipher
![](FILES/2.png)
- Flag{El_Clasico_Cipher}
### Sixty Four
#### Challenge
Gà để lại một thông điệp bí mật nhưng nó không làm khó được trí thông minh của Mèo Yang Hồ.
> [File](cipher1.txt)
- Từ đề bài => 64 => Base 64
- Sau khi decode đoạn base 64 mình nhận được đoạn mã hex.
- Decode tiếp đoạn hex và nhận được flag.
- ```Flag{___Base64xHex___}```
## Web Exploitation
### Ét Quy Eo
#### Challenge
Đây là một lỗ hổng rất cơ bản nhưng lại dễ dàng bị bỏ qua trong quá trình phát triển ứng dụng.
Lỗ hổng này nguy hiểm tới mức cho phép các h@cker lấy quyền quản trị của website, thay đổi nội dung, lợi dụng để ăn cắp các thông tin nhạy cảm, hoặc thậm chí làm bàn đạp tấn công chiếm quyền quản trị toàn hệ thống.
Đây là phương thức tấn công yêu thích của Hacker khi lần đầu tiếp cận với website của bạn.
> http://chal13.web.letspentest.org/
---
#### Solution
- Từ đề bài thì đây là lỗ hổng SQL.
- Sau khi tìm hiểu trên [wiki](https://en.wikipedia.org/wiki/SQL_injection) thì mình tìm được:
![](FILES/3.png)
- Sau khi nhập username và password là: ' OR '1'='1' -- 
![](FILES/4.png)
- Decode đoạn "RmxhZ3tGcjMzX1N0eWwzfQ==" thì nhận được flag.
- Flag{Fr33_Styl3}
### Gatling gun
#### Challenge
Với chiếc Gatling gun mạnh mẽ trong tay, Mèo Yang Hồ có thể vượt qua bất kì cánh cửa bảo mật nào. Nhưng thật buồn cười là trong tay hắn lại không có một viên đạn nào.
Nếu bạn muốn nghịch súng với Mèo thì hãy đi nhặt đạn ở trong Github của Cookie Hân Hoan nhé.
> http://chal9.web.letspentest.org/
---
#### Solution
- Để nhặt đạn thì ta phải vào Github của Cookie Hân Hoan
![](FILES/5.png)
- Và mình thấy được 3 file ứng với 3 trưởng cần điền của bài.
- Tiếp theo thì mình sẽ mở burpsuite, nạp đạn cho 3 khẩu súng và sấy thôi
![](FILES/6.png)
- Sau khi bắn vài phút thì flag cũng đã xuất hiện
![](FILES/7.png)
- FLAG{e6c068faf9241fe9d1f2000516718377}
### The maze runner
#### Challenge
Lạc vào một mê cung với vô vàn những chuỗi kí tự bí ẩn. Vừa chạy vừa phải nghĩ đâu mới manh mối giúp Gà thoát ra.
Hãy giúp Gà một tay nhé?
> http://chal10.web.letspentest.org/
---
#### Solution
- Bài này thì mình mở từng file để check thôi =))
> http://chal10.web.letspentest.org/MS70RIE/2D5TA9DK/UGR85I0H/60ADG
- FLAG{6059e2117ea3eeecdad7faf1e15d16a2}
## Forensic
### AudiCaty
#### Challenge
Hazy gửi cho Gà một thông điệp bí mật, kèm một lời nhắn "Đừng vội vàng kết luận môt vấn đề, luôn phải để mắt thấy tai nghe"
[File](squitgaem.wav)
---
#### Solution
- Từ dữ kiện bài cho mình biết được bài này sử dụng audacity để xem flag bị giấu trong file âm thanh.
![](FILES/8.png)
- Flag{No_Bullets_for_Player_001}
### Basic Image
#### Challenge
Đố bạn biết bức ảnh này được nhắc tới bài viết nào trên Fanpage của Cookie Hân Hoan ấy. Hehe!
> https://www.facebook.com/cookie.han.hoan/
> ![](FILES/KB.jpg)
---
#### Solution
- Đầu tiên mình đã mò vào Fanpage của Cookie Hân Hoan để tìm kiếm bức ảnh được cung cấp.
> ![](FILES/9.png)
- Bài viết có đề cập đến Metadata => flag có thể được giấu trong đây => mở dùng HxD mở ảnh và lấy flag.
- Flag{metadataratatatataaaaaa}
### ExSeller
#### Challenge
Để không bị Mèo nhòm ngó tệp tài liệu quan trọng. Gà nhanh tay đặt mật khẩu, nhưng lại vô tình quên mất. Làm thế nào bây giờ T_T
> [File](bruteme.xlsx)
---
#### Solution
- File excel được cung cấp đã bị đặt pass và thay vì việc bypass nó thì mình đã giải nén luôn nó ra.
- Lục lọi 1 xíu thì mình tìm thấy flag trong: 
> bruteme\xl\sharedStrings.xml
- Flag{Micro$oft_Heck3r_Man}
### Streamer
#### Challenge
Anh nghệ sĩ nhiều đam mê đang vớt rác bên tàu. Ta lang thang với bản vẽ đời ta tự tô màu.
Ô! Vớt được cái gì thú zị này!
> [File](travis.pcapng)
---
#### Solution
- Bài này nó mình 1 file pcapng nên đầu tiên mình ném file lên [A-packets](https://apackets.com/) => view report.
- Mình tìm thấy một file zip trong mục HTTP down về thì cần pass để giải nén.
- Tiếp tục quay lại lục trong mục HTTP thì thấy có request login.
> ![](FILES/10.png)
- Thử lấy pass này mở file zip => mở được => lấy flag.
- Flag{TCP_streamin_go_skrrrrrrrt}
### Interceptor
#### Challenge
Rối loạn tiền đình là bệnh lý gây ra trạng thái mất cân bằng về tư thế, khiến người bệnh thường xuyên bị chóng mặt, hoa mắt, ù tai, đi đứng lảo đảo.
Nhưng sự thật não bạn đang muốn nhảy như điệu tanggo Khoan, dừng khoảng chừng là 2 giây!
> [File](cooooooooooookie.gif)
---
#### Solution
- Đầu tiên mình dùng https://ezgif.com/split để tách gif xem sao và mình đã nhận được 9 mảnh của 1 mã QR bị tách ra.
- Để ý 1 xíu thì vị trí mỗi mảnh trong những bức ảnh chính là vị trí của nó trong 1 mã QR hoàn chỉnh.
- Và giờ mình chỉ cần ghép các mảnh lại thôi.
> ![](FILES/11.png)
- Flag{1s_th1s_m1sc3llan30us?}
### Github
#### Challenge
Được biết tới như một kho lưu trữ mã nguồn khổng lồ của thế giới, và những thay đổi trong quá khứ đều được lưu lại và khôi phục. Hãy kiếm tìm những bí mật mà Gà con lon ton vô tình để lại.
> https://github.com/
---
#### Solution
- Để ý ở đề bài:
> Được biết tới như một kho lưu trữ mã nguồn khổng lồ của thế giới, và những thay đổi trong quá khứ đều được lưu lại và khôi phục
- Nên mình đã truy cập github và tìm github của BTC bằng từ khóa ``` cookiehanhoan ``` và có kết quả.
- Truy cập vào mình thấy có duy nhất 1 repo.
- Tiếp tục vào comnmit để xem lịch sử chỉnh sửa và xuất hiện ``` fLAG.txt```
> ![](FILES/12.png)
- Kiểm tra tiếp các lịch sử chỉnh sửa thì mình đã tìm thấy flag.
> ![](FILES/13.png)
- Flag{no_where_to_hide_gitleaks]
### From The Above
#### Challenge
Gà và Mèo Yang Hồ đã cùng nhau thoát khỏi trọng lực, lẩn trốn loài người tại một hành tinh đày đất đá, và một khí quyển mỏng.
Vượt qua chặng đường 472 triệu km trong 7 tháng, đây là bức ảnh đầu tiên họ gửi về trái đất.
Bạn có giải mã được những tín hiệu này không?
> [File](ufo.wav)
---
#### Solution
- Sau nhiều lần nghe đi nghe lại file âm thanh và thử decode bằng RX SSTV nhưng kết quả nhận được quá mù mịt, mà đề bài là "From The Above" mình đã nghĩ đây là âm thanh tín hiệu vệ tinh thời tiết và googling: https://noaa-apt.mbernardi.com.ar/
> ![](FILES/30.png)
- Flag{h3ll0_fr0m_th3_0th3r_Sky}
### Volatility
#### Challenge
> The true forenSeek
Giữ nguyên hiện trường là việc cần thiết trong quá trình điều tra số. Một trong những file lưu trữ hình ảnh của RAM trong quá trình làm đề thi được leak ra cho các chiến binh. Cho mình thấy các cậu tìm được gì nào :)

> https://drive.google.com/file/d/1PMbu0KbORvRD7Sp2-V-2e-97YIJUY86p/view?usp=sharing
---
#### Solution
- Mình khá bất ngờ vì bài này có thể lấy flag đơn giản bằng việc ném file raw vào HxD và tìm flag.
> ![](FILES/29.png)
- Flag{7ef31e58bd4086e294b4d700c721f35f}
## Network
### Post Office Man
#### Challenge
Anh bưu tá này là một người mà Gà rất tin tưởng. Gà ủy quyền cho anh ấy lên bưu điện, nói chuyện với anh kiểm thư để lấy thư về.
Nếu giấy ủy quyền hợp lệ, anh kiểm thư sẽ giữ lại bản gốc rồi photocopy ra một bản khác để anh bưu tá đem về cho Gà. Để nhỡ trong trường hợp Gà có tức quá xé thư đi thì vẫn có thể lên đây lấy lại.
Đố bạn anh bưu tá sử dụng giao thức email nào để nói chuyện với anh kiểm thư?
> network.letspentest.org 9002
---
#### Solution
- Sau khi netcat tới địa chỉ được cung cấp, mình thấy xuất hiện của ```pop3``` và thử nhập USER và kết quả là sai format USER command.
- Vì thế mình đã tìm kiếm về pop3 command
> ![](FILES/14.png)
- Sau khi tìm hiểu về pop3 thì mình đã hiểu nhiệm vụ của mình ở bài này là truy xuất được là thư.
- Đầu tiên mình log bằng user và password bất kì.
- Sau đó LIST command sẽ ```Liệt kê tất cả thư.```
- Tiếp theo mình chọn thư cần truy xuất ``` RETR 1 ```.
- Mình thử như vậy đến thư thứ 8
    ``` RETR 8```
> ![](FILES/15.png)
- Flag{1-Ha\/3-1o0o-UnS33n-3Ma1L}
### Very Good Shipper
#### Challenge
Hãy tham gia đấu trường Cookie phiên bản nhanh như chớp. Gà phải chọn ra đáp án đúng trong thời gian nhanh nhất.
Giao thức TCP sẽ giúp các câu trả lời của Gà luôn được đảm bảo gửi đến máy chủ của Cookie Arena mà không bị rơi rớt một từ nào.
Tuy nhiên, Gà đã quên cổng kết nối vào máy chủ. Chỉ nhớ mang máng là nó giống với thử thách "Scan me if you can"
> network.letspentest.org
---
#### Solution
``` Gà đã quên cổng kết nối vào máy chủ```
=> Đầu tiên mình phải đi tìm port của chall này.
- Sử dụng ```nmap``` để kiểm tra:
![](FILES/16.png)
- Sau khi thử từng port thì ``` 9003``` là port của chall này.\
- Netcat đến địa chỉ ,trả lời các câu hỏi và nhận flag.
>![](FILES/17.png)
- Flag{t00-ez-4-y0u}
### Where is my house?
#### Challenge
DNS CHÍNH LÀ XƯƠNG SỐNG CỦA INTERNET.
Tên miền hay Domain chính là địa chỉ trang web, thứ mà các bạn vẫn hay gõ vào trên thanh địa chỉ trên trình duyệt để đọc báo hay lướt web, xem phim.
Trên Internet mọi máy tính, máy chủ, các thiết bị mạng được kết nối và giao tiếp với nhau thông qua hệ thống cáp mạng chằng chịt và khổng lồ. Các máy tính sẽ được gán cho nhau những dãy số để định danh với nhau gọi là địa chỉ IP. Nói một cách dễ hiểu thì một ai đó muốn ghé thăm nhà bạn thì họ cần phải có địa chỉ nhà. Những dãy số địa chỉ này có độ dài có thể lên đến 12 hoặc 45 kí tự.
Đến mật khẩu 6 kí tự bạn còn không nhớ nổi, vì thế năm 1984 DNS (Domain Name System) được phát minh để giúp bạn kết nối với nhau bằng tên gọi.
Bạn chỉ cần nhớ letspentest.org thay vì những dãy số khô khan và kì quặc. Khi vừa Enter, hệ thống DNS bắt đầu hoạt động, nó như tấm bản đồ để chỉ cho bạn biết "Hey, cái tên miền của Cookie có địa chỉ IP là X.X.X.X, hãy tới đó mà lấy thông tin đê". DNS cũng trả lời cho bạn biết "X.X.X.X có phải địa chỉ nhà Cookie Hân Hoan hay không"
DNS cũng chứa các thông tin khác, nó gọi là các bản ghi (Record). Bạn thử tìm xem domain này còn có những bản ghi nào chứa những điều kì quặc không?
> letspentest.org
---
#### Solution
- Nhiệm vụ của mình là lấy record của ```letspentest.org```
- Sử dụng https://dnsdumpster.com/
- Nhập DNS và lấy flag
> ![](FILES/18.png)
- Flag{DNS_A_AAAA_TXT_CNAME}
### Scan me if you can
#### Challenge
Nếu coi mỗi máy chủ là một ngôi nhà, trước khi xâm nhập vào bên trong, các Hacker phải thực hiện việc thăm dò. Họ xem xét đâu là điểm yếu nhất của ngôi nhà, chỗ nào là điểm mù camera? Chủ nhà hoặc bảo vệ sẽ phản ứng thế nào khi có xuất hiện các dấu hiệu bất thường?
Trong quá trình tìm kiếm lỗ hổng, Hazy thường xem xét ngôi nhà này có bao nhiêu cánh cửa đang mở (Port). Hãy sử dụng công cụ thân quen để "ném đá" vào tất cả các cánh cửa của ngôi nhà.
Biết rằng, cửa sổ được đánh số từ 8100 tới 9100
Dựa vào sự phản hồi bạn sẽ biết được những điều thú vị!
> network-insecure.letspentest.org
---
#### Solution
- Đầu tiên mình sử dụng nmap để quét port của địa chỉ được cung cấp và port nằm trong khoảng ```8100 -> 9100``` nên mình xác định được port của địa chỉ này là ```9003```
- Mình đã thử netcat đến địa chỉ nhưng không thấy phản hổi từ server
- Thử truy vào địa chỉ với port 9003 trên trình duyệt 
>![](FILES/19.png)
- Sau một hồi mày mò mình tìm thấy flag trong network.
>![](FILES/20.png)
- Flag{Every-Header-Have-It-Own-Meaning}
### Secure HTTP
#### Challenge
HTTP và HTTPS đều là hai giao thức giúp trình duyệt của bạn truy cập, tương tác với các trang Web. Tuy nhiên khi sử dụng giao thức HTTP để truy cập Web ở một quán cà phê hay trong cùng một khu trọ thì tất cả các nội dung trao đổi nhạy cảm, cũng như mật khẩu của bạn trên Web đều có thể nghe lén.
Còn HTTPS (chữ S có nghĩa là Secure - Bảo mật) sinh ra để mã hóa dữ liệu trong quá trình trao đổi giữa trình duyệt và máy chủ bằng một chiếc Chứng chỉ (Certificate)
> network-insecure.letspentest.org 9004
---
#### Solution
- Mình giải được bài này sau khi tìm hiểu về ```Secure SSL connections with Ncat```:https://dev.nmap.narkive.com/uTngHJ9O/secure-ssl-connections-with-ncat
```
ncat --ssl-verify  network-insecure.letspentest.org 9004 -v
```
> ![](FILES/21.png)
- Flag{This-Is-A-Trusted-One}
## Web Basic
### Hân Hoan
#### Challenge
Thấy hộp bánh quy của chú Hazy để hớ hênh trên bàn. Với bản tính nghịch ngợm, Mèo Yang Hồ nhanh tay thêm chút gia vị để biến cuộc đời trở nên hài hước và hân hoan hơn.
> http://chal5.web.letspentest.org/
---
#### Solution
- Giao diện trang web
> ![](FILES/22.png)
- Đầu tiên thử nhập username và password bất kì.
>![](FILES/23.png)
- Đề bài có đề cập đến ```Thấy hộp bánh quy của chú Hazy để hớ hênh trên bàn```
- Vì vậy mình đã thử sửa cookie
```Guest -> CookieHanHoan``` và nhận được flag
> ![](FILES/24.png)
- Flag{Cookies_Yummy_Cookies_Yammy!}
### Header 401
#### Challenge
Để nhiều loại Trình duyệt và Web Server có thể nói chuyện và hiểu được nhau thì họ phải sử dụng chung một giao thức có tên gọi là HTTP Protocol. Khi người dùng bắt đầu truy cập Web, trình duyệt sẽ chuyển những hành động của họ thành yêu cầu (Request) tới Web Server. Còn Web Server sẽ trả lời (Response) xem có thể đáp ứng hay từ chối cung cấp thông tin cho trình duyệt.
Ví dụ, bạn Gà muốn LẤY danh sách các thử thách trong cookiearena<chấm>org, ở đường dẫn /challenges bằng TRÌNH DUYỆT Chrome. Trình duyệt của Gà sẽ phải điền vào một cái form mẫu có tên gọi là HTTP Header và gửi đi. Mỗi yêu cầu sẽ được viết trên một dòng, và nội dung của mỗi yêu cầu sẽ phải viết đằng sau dấu hai chấm.
Hãy đoán xem trong thử thách này có những Header thú vị nào nha
> http://chal3.web.letspentest.org/
---
#### Solution
- Sau khi truy cập link được cấp, mình kiểm tra source web và thấy gợi ý ``` Basic Authentication Credential: gaconlonton/cookiehanhoan ```
> ![](FILES/25.png)
- Tìm hiểu về gợi ý: https://en.wikipedia.org/wiki/Basic_access_authentication
- Giao diện đầu tiên là ``` GET Request ```. Dựa theo đề bài, mình sử dụng burpsuite, ```POST Request``` và thêm ```Authorization: Basic Z2Fjb25sb250b246Y29va2llaGFuaG9hbg==```
>![](FILES/26.png)
- Flag{m4g1c@l_h34d3r_xD}
### JS Bxxp Bxxp
#### Challenge
Sau nhiều đêm suy nghĩ về việc làm thế nào để bảo vệ mã nguồn. Cố gắng thoát khỏi ánh mắt soi mói của Mèo Yang Hồ.
Gà chẹp miệng rồi nói: "Đã tới lúc phải cho nó phải thốt lên rằng! WTF!!!"
> http://chal4.web.letspentest.org/
---
#### Solution
- Đầu tiên mình đã mở source để xem có đoạn code nào check các trường cần điền và mình thấy có 4 file js được encode bằng JSFuck.
- Sau khi decode JSFuck mình cần tìm hiểu nhiệm vụ của từng file JS này là gì.
- File js đầu tiên check username:
> function verifyUsername(username) {     if (username != "cookiehanhoan") {       return false     }     return true   }

```=> username: cookiehanhoan```
- File js thứ 3:
> function verifyPassword(password) {     if (reverseString(password) != "dr0Wss@p3rucreSr3pus") {       return false     }     return true   }

```=>pass: dr0Wss@p3rucreSr3pus```
- File js thứ 4:
> function verifyRole(role) {       if (role.charCodeAt(0) != 64) {         return false;       }       if ((role.charCodeAt(1) + role.charCodeAt(2) != 209) && (role.charCodeAt(2) - role.charCodeAt(1) != 9)) {         return false       }       if ((role.charCodeAt(3).toString() + role.charCodeAt(4).toString() != "10578") && (role.charCodeAt(3) - role.charCodeAt(4) != 27)) {         return false       }     return true   }

``` => role: @dmiN```
- Cuối cùng là file js thứ 2 nó sẽ đảo ngược chuối pass mình nhập vào. Và sau khi đảo ngược pass phải trùng với pass mà ta tìm thấy ở file js thứ 3.
> function reverseString(str) {   if (str === "")    { return "" }   else {   return reverseString(str.substr(1)) + str.charAt(0)}   }

``` => pass: sup3rSercur3p@ssW0rd```
- Giờ mình chỉ cần nhập thông tin vào và lấy flag.
- Flag{JAV-ascript_F*ck}
### Impossible
#### Challenge
Học lỏm được công thức chế tạo lá chắn tàng hình của Hazy. Gà nhanh chóng đem về xây dựng hệ thống phòng thủ của riêng mình. Liệu nó có làm khó được Mèo Yang Hồ không?
> http://chal7.web.letspentest.org/
---
#### Solution
- Trước hết, vào source xem và tìm thấy 1 hàm xử lý pass:
```
function checkPass()
{
	var password = document.getElementById('password').value;
	if (btoa(password.replace("cookiehanhoan", "")) == "Y29va2llaGFuaG9hbg==") {
		window.setTimeout(function() {
			window.location.assign('check.php?password=' + password);
		}, 500);
	}
}
```
- Đơn giản thì chức năng của hàm này sẽ thay chuỗi ```cookiehanhoan``` trong chuỗi nhập vào sau đó encode base64 chuỗi đó, nếu nó bằng ```Y29va2llaGFuaG9hbg==``` thì pass đúng.
- Chuỗi ```Y29va2llaGFuaG9hbg==``` decode ra là ```cookiehanhoan``` nên mình đã thử nhập ```cookiehanhoancookiehanhoan``` nhưng không được.
- Sau đó mình thử chèn vào giữa ```cookiecookiehanhoanhanhoan``` thì thành công.
- Flag{Javascript_is_not_safe???}
### Infinite Loop
#### Challenge
Cuộc đời luôn là vậy. Một giây trước tưởng đã cùng đường, một giây sau có lại đầy hy vọng. Các chiến binh đã có công cụ mạnh mẽ trong tay, hãy dùng nó để can thiệp dòng chảy.
> http://chal6.web.letspentest.org/
---
#### Solution
- Cũng như những bài trước mình thử check source nhưng lần này không có gì khả nghi.
- Và sau khi ấn Login mình thử kiểm tra Network và thấy rất nhiều request được gửi đi lặp đi lặp lại.
- Tới đây mình thử sử dụng burpsuite để có thể follow theo các request được gửi đi liên tục như thế.
- Sau khi ấn Send và Follow redirection vài lần thì flag xuất hiện.
> ![](FILES/27.png)
- Flag{Y0u_c4ptur3_m3_xD!!!}
### I am not a robot
#### Challenge
Nếu là người thì cho xem tai, còn nếu là robot thì đứng ở ngoài. Bạn đã bị chặn
> http://chal2.web.letspentest.org/
---
#### Solution
- Từ đề bài mình thử truy cập ```http://chal2.web.letspentest.org/robots.txt```
> ![](FILES/28.png)
- Truy cập theo đường dẫn được cho phép và lấy flag.
```http://chal2.web.letspentest.org/fl@g1337_d240c789f29416e11a3084a7b50fade5.txt```
- Flag{N0_B0T_@ll0w}
### Sause
#### Challenge
Trình duyệt đang rất vất vả để chuyển đổi các đoạn mã thành hình ảnh và màu sắc. Hãy trải nghiệm góc nhìn của trình duyệt nhé!
> http://chal1.web.letspentest.org/
---
#### Solution
- Đơn giản là mình chỉ cần mở source lên và flag sẽ xuất hiện.
- Flag{Web_Sause_Delicious}

















