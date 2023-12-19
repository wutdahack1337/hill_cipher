# hill_cipher
Hill cipher và cách giải mã cho học sinh cấp 2

Hôm nay t tìm hiểu về Hill cipher và đây là cách nó hoạt động: 
- Chọn một khóa K, với K là một [ma trận](https://vi.wikipedia.org/wiki/Ma_tr%E1%BA%ADn_(to%C3%A1n_h%E1%BB%8Dc)#%C4%90%E1%BB%8Bnh_ngh%C4%A9a) m * m (chọn làm sao cho: m là ước của độ dài plaintext, nếu khó tìm m thì thêm những kí tự vô nghĩa ở cuối && K là [ma trận khả nghịch](https://vi.wikipedia.org/wiki/Ma_tr%E1%BA%ADn_kh%E1%BA%A3_ngh%E1%BB%8Bch) - nói đơn giản là chọn làm sao cho K tồn tại ma trận nghịch đảo)
- Chia plaintext thành những ma trận size 1 * m - tạm gọi chung là E
- Mã hóa: E(1 * m) * K(m * m) % 26 = D(1 * m)
- Giải mã: E = D * K^(-1) % 26 ([cách tìm](https://vi.wikipedia.org/wiki/Ma_tr%E1%BA%ADn_kh%E1%BA%A3_ngh%E1%BB%8Bch#T%C3%ACm_ma_tr%E1%BA%ADn_ngh%E1%BB%8Bch_%C4%91%E1%BA%A3o) ma trận nghịch đảo K (K^-1))

Sau khi t đọc cách tìm ma trận nghịch đảo, t chả hiểu gì hết (chắc là do t chưa học môn đại số tuyến tính), t thử suy nghĩ xem có cách nào tìm K^(-1) đơn giản hơn không, cũng sau 5' nháp các kiểu, t đã tìm ra được:
- Mấu chốt của vấn đề là: K * K^(-1) % 26 = I (I là [ma trận đơn vị](https://vi.wikipedia.org/wiki/Ma_tr%E1%BA%ADn_(to%C3%A1n_h%E1%BB%8Dc)#Ma_tr%E1%BA%ADn_%C4%91%C6%A1n_v%E1%BB%8B))
- Từ đó t có thể lập ra m * m hệ phương trình, rồi sau đó giải hệ phương trình để tìm từng ô của ma trận nghịch đảo thôi (khi tính hệ phương trình kết quả ra (số âm) || (phân số) thì đừng vội lo lắng, hãy % cho 26 là sẽ ổn thôi)

Thế thôi ~~


