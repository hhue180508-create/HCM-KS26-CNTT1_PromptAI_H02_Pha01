# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 05
- **Họ tên:**Nguyễn Thị Hồng Huệ
- **Lớp:**CNTT1
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xem phim ra JSON

**KET QUA AI**

```text
[\
&#x20; {\
&#x20;   "loai_ve": "P2D",\
&#x20;   "ngay_chieu": "2026-12-24",\
&#x20;   "ve_nguoi_lon": 2,\
&#x20;   "ve_tre_em": 1,\
&#x20;   "loai_ghe": "thuong",\
&#x20;   "ghi_chu": null\
&#x20; },\
&#x20; {\
&#x20;   "loai_ve": "P3D",\
&#x20;   "ngay_chieu": "2027-01-01",\
&#x20;   "ve_nguoi_lon": 3,\
&#x20;   "ve_tre_em": 0,\
&#x20;   "loai_ghe": null,\
&#x20;   "ghi_chu": "1 người hay chóng mặt, cần ngồi gần lối ra"\
&#x20; },\
&#x20; {\
&#x20;   "loai_ve": "GOLD",\
&#x20;   "ngay_chieu": null,\
&#x20;   "ve_nguoi_lon": 4,\
&#x20;   "ve_tre_em": 0,\
&#x20;   "loai_ghe": "doi",\
&#x20;   "ghi_chu": "1 bạn đi xe lăn"\
&#x20; }\
]
```

**Link trò chuyện:**https://chatgpt.com/share/6b078f7b-ce14-83ec-b800-a50caaac3300

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
### **Bước 1: Tính tiền vé người lớn**

- Số lượng: 5 người.
- Giá vé P3D: 130.000 đồng/vé.

\\(5 \times 130.000 = 650.000\\) đồng.

### **Bước 2: Tính tiền vé trẻ em**

- Trẻ cao 1,1 m: \\(130.000 \times 70\\% = 91.000\\) đồng.
- Trẻ cao 1,25 m: \\(130.000 \times 70\\% = 91.000\\) đồng.
- Bé cao 0,9 m: Miễn phí vì dưới 1 m.

Tổng tiền trẻ em:

\\(91.000 + 91.000 + 0 = 182.000\\) đồng.

### **Bước 3: Tính tổng tiền vé trước giảm giá**

\\(650.000 + 182.000 = 832.000\\) đồng.

### **Bước 4: Giảm giá nhóm 10%**

Nhóm có 5 người lớn nên đủ điều kiện giảm 10%.

\\(832.000 \times 10\\% = 83.200\\) đồng.

Tiền vé sau giảm:

\\(832.000 - 83.200 = 748.800\\) đồng.

### **Bước 5: Tính tiền combo bắp nước**

- Số lượng: 3 combo.
- Giá mỗi combo: 75.000 đồng.

\\(3 \times 75.000 = 225.000\\) đồng.

Combo không được giảm giá.

### **Bước 6: Tính tổng tiền**

\\(748.800 + 225.000 = 973.800\\) đồng.

Kết quả

[RESULT: 973.800 đồng]
```

**Link trò chuyện:**https://chatgpt.com/share/6b07904d-ea64-83ec-98cd-7348531dff25

### b) Kiểm tra kết quả AI
Đúng
## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{\
&#x20; "loai_su_co": "loi_ky_thuat",\
&#x20; "so_khach": 4,\
&#x20; "so_suat_bi_loi": 2,\
&#x20; "tom_tat": "Bốn khách gặp lỗi mất tiếng ở hai suất; mức hoàn 640.000 đồng, cần Quản lý rạp duyệt trước khi gửi."\
}
```

**Link trò chuyện:**https://chatgpt.com/share/6b079121-d6c4-83ec-a99a-4e15cc4d7e03

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
## **BẢNG CHẤM ĐIỂM BÀI LÀM**

| Tiêu chí                               | Điểm | Minh chứng                                                                                                                                       | Đề xuất sửa                                                                                        |
| -------------------------------------- | ---- | ------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| **Đúng thông tin (50%)**               | 2/5  | “Vé đi Nha Trang bên em 350.000đ nha chị” sai giá vé. Giá chuẩn là **380.000 đồng/vé người lớn**.                                                | “Vé tuyến Sài Gòn – Nha Trang có giá 380.000 đồng/vé người lớn.”                                   |
| **Đúng thông tin (chính sách đổi vé)** | 0/5  | “Chị đổi trước 12 tiếng thì đổi free nha chị.” Sai chính sách vì đổi trước 12 tiếng thuộc khoảng từ 6 đến dưới 24 giờ, phải chịu phí 20% giá vé. | “Nếu chị đổi vé trước giờ xe chạy 12 tiếng, phí đổi vé là 20% giá vé, tương đương 76.000 đồng/vé.” |
| **Đầy đủ thông tin (30%)**             | 1/3  | “Cần gì chị nhắn em liền!” Chưa chủ động mời khách cung cấp ngày đi và số lượng vé để đặt chỗ.                                                   | “Chị vui lòng cung cấp ngày khởi hành và số lượng vé để bên em hỗ trợ đặt chỗ.”                    |
| **Giọng điệu (20%)**                   | 1/2  | “Xe xịn lắm luôn”, “nha chị”, “nhắn em liền” mang tính suồng sã, thiếu chuyên nghiệp.                                                            | Sử dụng ngôn ngữ lịch sự, chuyên nghiệp và tư vấn rõ ràng hơn.                                     |

## **Tổng kết điểm**

# **4/10**

Chưa đạt

**Các lỗi cần khắc phục:**

1. Báo sai giá vé: 350.000 đồng thay vì 380.000 đồng.
2. Áp dụng sai chính sách đổi vé trước 12 tiếng.
3. Chưa mời khách cung cấp ngày đi và số lượng vé.
4. Giọng văn chưa phù hợp với phong cách tư vấn chuyên nghiệp.

**Nhận xét:** Bài làm đã trả lời được hai nội dung khách hàng hỏi nhưng mắc lỗi nghiêm trọng về giá vé và chính sách đổi vé. Cần kiểm tra kỹ thông tin chuẩn trước khi phản hồi khách hàng.
```

**Link trò chuyện:**https://chatgpt.com/share/6b079234-fb68-83ec-92a6-abe1ed31ffd8
