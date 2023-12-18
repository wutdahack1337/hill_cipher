# hill_cipher
Hill cipher và cách giải mã cho học sinh cấp 2

Hôm nay t tìm hiểu về Hill cipher và đây là cách nó hoạt động: 
- Chọn một khóa K, với K là một [ma trận](vi.wikipedia.org/wiki/Ma_trận_(toán_học)#Định_nghĩa) m * m (chọn làm sao cho: m là ước của độ dài plaintext, nếu khó tìm m thì thêm những kí tự vô nghĩa ở cuối && K là [ma trận khả nghịch](vi.wikipedia.org/wiki/Ma_trận_khả_nghịch) - nói đơn giản là chọn làm sao cho K tồn tại ma trận nghịch đảo)
- Chia plaintext thành những ma trận size 1 * m - tạm gọi chung là E
- Mã hóa: E(1 * m) * K(m * m) = D(1 * m)
- Giải mã: E = D * K^(-1) ([cách tìm](vi.wikipedia.org/wiki/Ma_trận_khả_nghịch#Tìm_ma_trận_nghịch_đảo) ma trận nghịch đảo K (K^-1))

Sau khi t đọc cách tìm ma trận nghịch đảo, t chả hiểu gì hết (chắc là do t chưa học môn đại số tuyến tính), t thử suy nghĩ xem có cách nào tìm K^(-1) đơn giản hơn không, cũng sau 5' nháp các kiểu, t đã tìm ra được:
- Mấu chốt của vấn đề là: K * K^(-1) = I (I là [ma trận đơn vị](vi.wikipedia.org/wiki/Ma_trận_(toán_học)#Ma_trận_đơn_vị))
- Từ đó t có thể lập ra m * m hệ phương trình, rồi sau đó giải hệ phương trình để tìm từng ô của ma trận nghịch đảo thôi (nhớ là mod 26, vì khi tính hệ phương trình kết quả sẽ ra số âm || phân số)

Thế thôi ~~


