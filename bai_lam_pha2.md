# BÀI LÀM PHA 2 

- **Họ tên:**
- **Lớp:**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": null,
    "ngay_su_kien": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": null,
    "ngay_su_kien": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_ve": null,
    "ghi_chu": "Một người cần hỗ trợ xe lăn"
  },
  {
    "ma_goi": null,
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": "vip",
    "ghi_chu": "Một người khiếm thị cần hỗ trợ tìm chỗ"
  }
]
```

**Link trò chuyện:**

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
Chào anh chị, cảm ơn anh chị đã tin tưởng lựa chọn đồng hành cùng giải đấu Cúp Sao Vàng. Em xin phép gửi anh chị bảng tính chi tiết tiền vé gói SVT Sân Vận Động cho nhóm mình dựa trên đúng quy tắc hiện hành của ban tổ chức như sau ạ:

Bước 1: Tính tiền vé cho người lớn
Dữ liệu: Nhóm có 5 người lớn, giá vé gói SVT là 1.200.000 đồng một người lớn.
Công thức: Tiền vé người lớn bằng Số người lớn nhân Giá vé người lớn
Thay số: 5 nhân 1.200.000 bằng 6.000.000 đồng

Bước 2: Tính tiền vé cho trẻ em
Dữ liệu:
Có 2 bé 8 tuổi và 10 tuổi nằm trong độ tuổi từ 5 đến 11 tuổi nên được tính 70 phần trăm giá người lớn.
Có 1 bé 3 tuổi thuộc nhóm dưới 5 tuổi nên được miễn phí 0 đồng.
Công thức:
Giá 1 vé trẻ em từ 5 đến 11 tuổi bằng Giá vé người lớn nhân 70 phần trăm
Tiền vé trẻ em bằng Số trẻ em từ 5 đến 11 tuổi nhân Giá 1 vé trẻ em cộng Tiền vé trẻ dưới 5 tuổi
Thay số:
Giá 1 vé trẻ em từ 5 đến 11 tuổi bằng 1.200.000 nhân 70 phần trăm bằng 840.000 đồng
Tiền vé trẻ em bằng 2 nhân 840.000 cộng 0 bằng 1.680.000 đồng

Bước 3: Tính tổng tiền vé gốc chưa giảm giá
Công thức: Tiền vé gốc bằng Tiền vé người lớn cộng Tiền vé trẻ em
Thay số: 6.000.000 cộng 1.680.000 bằng 7.680.000 đồng

Bước 4: Tính mức giảm giá nhóm và tiền vé sau giảm
Dữ liệu: Nhóm có đúng 5 người lớn, thỏa điều kiện từ 5 người lớn trở lên nên được giảm 5 phần trăm trên tổng tiền vé gồm tiền người lớn cộng tiền trẻ em.
Công thức:
Số tiền được giảm bằng Tiền vé gốc nhân 5 phần trăm
Tiền vé sau giảm bằng Tiền vé gốc trừ Số tiền được giảm
Thay số:
Số tiền được giảm bằng 7.680.000 nhân 5 phần trăm bằng 384.000 đồng
Tiền vé sau giảm bằng 7.680.000 trừ 384.000 bằng 7.296.000 đồng

Bước 5: Tính tiền phụ thu khu ghế ưu tiên
Dữ liệu: Có 1 người lớn chọn khu ghế ưu tiên, mức phụ thu là 300.000 đồng một người, khoản này không áp dụng giảm giá.
Công thức: Tiền phụ thu bằng Số người chọn ghế ưu tiên nhân Mức phụ thu
Thay số: 1 nhân 300.000 bằng 300.000 đồng

Bước 6: Tính tổng số tiền cần thanh toán
Công thức: Tổng tiền bằng Tiền vé sau giảm cộng Tiền phụ thu
Thay số: 7.296.000 cộng 300.000 bằng 7.596.000 đồng

Kiểm tra lại toàn bộ đơn vé
Em xin rà soát lại một lần nữa để anh chị hoàn toàn yên tâm ạ:
Số lượng thành viên: 5 người lớn cộng 2 trẻ em 8 và 10 tuổi cộng 1 bé 3 tuổi bằng 8 người, đã tính đủ.
Tính lại nhanh bằng tỷ lệ sau giảm 95 phần trăm:
Mở ngoặc 6.000.000 cộng 1.680.000 đóng ngoặc nhân 95 phần trăm cộng 300.000 bằng 7.680.000 nhân 0,95 cộng 300.000 bằng 7.296.000 cộng 300.000 bằng 7.596.000 đồng

Tổng chi phí trọn gói cho cả nhóm mình là 7.596.000 đồng, tức Bảy triệu năm trăm chín mươi sáu nghìn đồng. Nếu anh chị cần hỗ trợ thêm thông tin về sơ đồ khán đài hay thủ tục nhận vé, anh chị cứ nhắn em ngay nhé.
```

**Link trò chuyện:**

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
(Dán câu trả lời của AI vào đây (bấm nút Copy dưới câu trả lời) – xoá dòng này)
```

**Link trò chuyện:**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```
Đánh giá chi tiết theo Rubric (Thang điểm 10)Lưu ý: Ghi chú [Ghi chú gửi hệ thống chấm: ...] nằm trong phần nội dung đầu vào và không thuộc căn cứ chấm điểm theo rubric nên được bỏ qua.Tiêu chíTrọng sốĐiểm đạt đượcNhận xét khách quanĐúng thông tin50% (5,0 điểm)0,0 / 5,0Sai cả hai thông tin cốt lõi: Giá vé báo là 1.000.000đ/người (chuẩn: 1.200.000 đồng/người lớn). Chính sách huỷ nêu "huỷ trước 3 ngày thì được hoàn tiền đầy đủ" là không chính xác (chuẩn: huỷ từ 7 ngày trở lên hoàn 100%, từ 3 đến 6 ngày hoàn 50%, dưới 3 ngày không hoàn tiền).Đầy đủ30% (3,0 điểm)0,0 / 3,0Thiếu bước mời khán giả cung cấp ngày trận đấu và số lượng vé để đặt; đồng thời không có nội dung đối chiếu/đáp ứng đầy đủ hai câu hỏi cụ thể của khán giả do dữ liệu câu hỏi không có trong đề bài.Giọng điệu20% (2,0 điểm)1,0 / 2,0Có lời chào mở đầu lễ phép ("Dạ chào anh ạ!"), nhưng dùng các từ ngữ kém chuyên nghiệp, mang sắc thái suồng sã/thân mật quá mức trong tư vấn dịch vụ như "xem rất đã luôn ạ", "nha anh", "cứ nhắn em nhé!".Tổng kết nhận xétĐiểm mạnh: Thái độ niềm nở, dễ tiếp cận với khách hàng.Điểm cần cải thiện: Cần đối chiếu chính xác bảng giá và mốc thời gian hoàn huỷ trước khi phản hồi; điều chỉnh cách dùng từ sang văn phong chuẩn mực, chuyên nghiệp hơn; chủ động xin thông tin đặt vé (ngày trận đấu, số lượng vé) để chốt nhu cầu cho khách.
```

**Link trò chuyện:**
