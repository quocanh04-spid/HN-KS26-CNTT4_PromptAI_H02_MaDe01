# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề: 01** 
- **Họ tên: Phạm Danh Quốc Anh**
- **Lớp: HN-KS26-CNTT4**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini): ChatGPT**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt tour ra JSON

**KET QUA AI**

```text
[
  {
    "ma_tour": "SP2N",
    "ngay_khoi_hanh": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_phong": "doi",
    "ghi_chu": null
  },
  {
    "ma_tour": null,
    "ngay_khoi_hanh": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_phong": null,
    "ghi_chu": "Một người ăn chay"
  },
  {
    "ma_tour": null,
    "ngay_khoi_hanh": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_phong": "doi",
    "ghi_chu": "Ông nội đi xe lăn"
  }
]
```

**Link trò chuyện: https://chatgpt.com/share/6afd02f3-35b4-83ec-9cac-c5ad9a1516ed**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
1. Tiền người lớn
- Số người lớn: 5.
- Giá tour DL3N: 3.200.000 đồng/người.
- Tiền người lớn = 5 × 3.200.000 = 16.000.000 đồng.
2. Tiền trẻ em
- Trẻ em 8 tuổi: 3.200.000 × 70% = 2.240.000 đồng.
- Trẻ em 10 tuổi: 3.200.000 × 70% = 2.240.000 đồng.
- Bé 3 tuổi: miễn phí = 0 đồng.
Tiền trẻ em = 2.240.000 + 2.240.000 + 0 = 4.480.000 đồng.

3. Tiền tour

Tiền tour = Tiền người lớn + Tiền trẻ em.

= 16.000.000 + 4.480.000

= 20.480.000 đồng.

4. Giảm giá đoàn
- Đoàn có 5 người lớn nên đủ điều kiện giảm 5%.
- Tiền giảm = 20.480.000 × 5% = 1.024.000 đồng.
- Tiền tour sau giảm = 20.480.000 − 1.024.000 = 19.456.000 đồng.
5. Phụ thu
- Có 1 người lớn ở phòng đơn.
- Phụ thu = 1 × 800.000 = 800.000 đồng.
6. Tổng tiền

Tổng tiền = Tiền tour sau giảm + Phụ thu.

= 19.456.000 + 800.000

= 20.256.000 đồng.

[RESULT: 20.256.000 đồng]
```

**Link trò chuyện: https://chatgpt.com/share/6afd0362-5380-83ec-8d51-69bdd25f8a7f**

### b) Kiểm tra kết quả AI

- Kết luận của AI là đúng, đầy đủ các bước

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "khach_san",
  "so_khach": 2,
  "so_dem_bi_anh_huong": 2,
  "tom_tat": "2 khách bị chuyển sang khách sạn 3 sao thay vì 4 sao trong 2 đêm đầu, phòng ẩm mốc."
}
```

**Link trò chuyện: https://chatgpt.com/share/6afd03fb-c880-83ec-952c-222c497dba7d**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Tiêu chí	Điểm	Minh chứng	Đề xuất sửa
Đúng thông tin (50%)	0/5	Lỗi 1: “Tour Sa Pa 2N1Đ bên em giá 2.200.000đ/người lớn” — Sai giá, giá chuẩn là 2.400.000 đồng/người lớn. Lỗi 2: “Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh.” — Sai chính sách. Huỷ trước 3 ngày thuộc mức hoàn 50%, không phải 100%.	Sửa lỗi 1: “Tour Sa Pa 2N1Đ bên em có giá 2.400.000 đồng/người lớn ạ.” Sửa lỗi 2: “Nếu anh huỷ trước ngày đi từ 7 ngày trở lên, công ty hoàn 100%; từ 3 đến 6 ngày hoàn 50%; dưới 3 ngày không hoàn tiền ạ.”
Đầy đủ (30%)	1/3	Nhân viên đã trả lời cả hai câu hỏi về giá và chính sách huỷ tour. Tuy nhiên, chưa mời khách cung cấp ngày đi và số lượng khách để hỗ trợ đặt tour.	Bổ sung: “Anh vui lòng cho em xin ngày khởi hành dự kiến và số lượng khách tham gia để em hỗ trợ tư vấn và đặt tour ạ.”
Giọng điệu (20%)	1/2	Lỗi 1: “đi rất vui luôn ạ” — Cách diễn đạt thiếu tính chuyên nghiệp. Lỗi 2: “Anh cần gì cứ nhắn em nhé!” — Cách diễn đạt hơi suồng sã.	Sửa lỗi 1: “Tour có lịch trình tham quan hấp dẫn và nhiều trải nghiệm thú vị ạ.” Sửa lỗi 2: “Nếu cần thêm thông tin, anh vui lòng liên hệ để em hỗ trợ ạ.”
Tổng điểm	2/10	Nhân viên trả lời đủ hai nội dung khách hỏi nhưng sai cả giá và chính sách huỷ, đồng thời chưa đạt yêu cầu về tính chuyên nghiệp.	Cần kiểm tra thông tin chuẩn trước khi tư vấn và bổ sung lời mời khách cung cấp thông tin đặt tour.

Kết luận: Nhân viên đạt 2/10 điểm. Cần cải thiện độ chính xác thông tin và phong cách giao tiếp chuyên nghiệp.
```

**Link trò chuyện: https://chatgpt.com/share/6afd044c-4100-83ec-babc-ff8a912a409b**
