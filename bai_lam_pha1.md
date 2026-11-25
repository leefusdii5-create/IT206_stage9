# BÀI LÀM PHA 1 

- **Họ tên:**
- **Lớp:**
- **Link repository Pha1:**

> Pha 1 (70 phút đầu, KHÔNG dùng AI). Viết xong, kéo thả file này vào repository Pha1 trước mốc giờ giám thị công bố.

## 4.1. Bảo vệ dữ liệu và chống ảo giác

### a) Ghi chú đã ẩn danh hoá

**GHI CHU DA AN DANH**

```text
khangia [TEN_KHACH], sdt [SDT], cccd [CCCD], email [EMAIL], đặt 3 vé gói SVT trận bán kết Cúp Sao Vàng ngày 18/12/2026 cho 2 người lớn và 1 trẻ em 9 tuổi. Khán giả đã chuyển khoản đặt cọc 1.500.000 đồng. Khán giả yêu cầu 3 ghế ngồi cạnh nhau gần lối đi.
```

### b) Hai câu lệnh chống ảo giác

**CAU LENH**

```
(Viết câu 1 và câu 2 vào đây – xoá dòng này)
```

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**PROMPT**

```text
Bối cảnh: Bạn là 1 người bán vé bóng đá cúp sao vàng, nhiệm vụ là đọc tin nhắn và chuyển thông tin của khách hàng qua JSON

Yêu Cầu: Chuyển 3 tin nhắn TN1, TN2, TN3 thành một mảng JSON

Giải thích: có 5 nguyên tắt:
1. ma_goi lấy theo bảng mã gói.
2. ngay_su_kien dạng YYYY-MM-DD; tin nhắn không ghi năm thì lấy năm 2026; không có ngày cụ thể thì null.
3. Khách không nhắc trẻ em thì tre_em là 0 và mọi khách là người lớn.
4. loai_ve chỉ nhận "thuong", "vip" hoặc null.
5. ghi_chu chỉ ghi yêu cầu đặc biệt về chỗ ngồi, hỗ trợ di chuyển hoặc ăn uống; không có thì null.

Hành động: Đọc và sử lý 3 TN
TN1: Mình muốn đặt gói Sân Vận Động trận tứ kết ngày 20/12 nha, 2 người lớn với 1 bé 8 tuổi, vé thường.

TN2: Cho 3 người đi Fan Zone trận ngày 05/01/2027 ạ. Một người cần hỗ trợ xe lăn.

TN3: Trận chung kết Cúp Sao Vàng tháng 12 còn vé không ạ? Nhà em 4 người lớn, có một người khiếm thị cần hỗ trợ tìm chỗ, lấy vé VIP.

Giọng điệu: không bịa, không giải thích thêm, chính xác theo 5 nguyên tắt

Yếu cầu bổ sung: 
-Trả về JSON
-kết quả trả về đúng 3 đối tượng
-Không suy đoán thông tin không có trong tin nhắn
```

## 4.3. Báo giá vé bằng Chain-of-Thought

### a) Prompt

**PROMPT**

```
Bối cảnh: Bạn là nhân viên bán vé cúp sao vàng

Yêu cầu: Tính tiền vé theo quy tắt sau :
BẢNG GIÁ VÉ (đồng/người lớn)
SVT – Sân Vận Động: 1.200.000
FZ – Fan Zone: 800.000
VIP – Khán đài VIP: 2.500.000

Giải thích: QUY TẮC TÍNH GIÁ
1. Trẻ em từ 5 đến 11 tuổi tính 70% giá người lớn. Trẻ dưới 5 tuổi miễn phí.
2. Nhóm từ 5 người lớn trở lên được giảm 5% trên tiền vé (tiền người lớn + tiền trẻ em).
3. Phụ thu khu ghế ưu tiên: 300.000 đồng/người. Phụ thu không được giảm giá.
4. Tổng tiền = tiền vé sau giảm + phụ thu.

Hành động: Nhóm cổ động viên đi xem trận bán kết, mua gói SVT, gồm 5 người lớn, 2 trẻ em (8 tuổi và 10 tuổi) và 1 bé 3 tuổi. Có 1 người lớn chọn khu ghế ưu tiên.


Giọng điệu: không thêm bớt để tránh sai lệch thông tin, giọng điệu gần gũi, chăm sóc khách hàng tận tình

Yêu cầu bổ sung:
- Chỉ sử dụng bảng giá và quy tắc đã cho
- Không tự ý thay đổi dữ liệu hoặc công thức
- Không bỏ qua bất kỳ bước tính toán nào
-Hãy giải quyết bài toán theo trình tự từng bước. Ở mỗi bước, trình bày công thức, thay số liệu cụ thể và kết quả tính toán. Sau khi hoàn thành, kiểm tra lại tổng tiền để đảm bảo chính xác.
```

## 4.4. Dây chuyền xử lý khiếu nại (Prompt Chaining)

### a) Prompt Trạm 1

**PROMPT**

```text
(Viết prompt vào đây – xoá dòng này)
```

### b) Hai điều cần kiểm tra ở JSON đầu ra của Trạm 1

1. (Viết câu trả lời vào đây – xoá dòng này)

2.

### c) Câu lệnh viết tiếp

**CAU LENH**

```text
(Viết câu lệnh vào đây – xoá dòng này)
```

## 4.5. Prompt chấm bài theo Rubric

**PROMPT**

```text
Bối cảnh: Bạn là nhân viên chấm điểm hỗ trợ của nhân viên

Yêu cầu:Chấm điểm cầu trả lời của nhân viên tư vấn dựa trên thông tin đã có

Giải thích: THÔNG TIN CHUẨN CỦA BAN TỔ CHỨC
- Giá vé SVT: 1.200.000 đồng/người lớn.
- Chính sách huỷ vé: huỷ trước sự kiện từ 7 ngày trở lên hoàn 100%; từ 3 đến 6 ngày hoàn 50%; dưới 3 ngày không hoàn tiền.

RUBRIC CHẤM (thang 10)
- Đúng thông tin (50%): giá và chính sách huỷ đúng với thông tin chuẩn.
- Đầy đủ (30%): trả lời đủ cả hai câu hỏi của khán giả và mời khán giả cung cấp ngày trận đấu, số lượng vé để đặt.
- Giọng điệu (20%): lịch sự, chuyên nghiệp, không dùng từ ngữ suồng sã.
Hành động:

Giọng điệu: Mang tính khách quan, căn cứ vào thang điểm mà chấmm, nhận xét chuyên nghiệp

Yêu cầu bổ sung:
- Chấm điểm theo yêu cầu của rubric
- Không tự ý cộng điểm thêm những thứ nằm ngoài thông tin cần chấm
- Dòng cuối ghi tổng điểm theo định dạng: Tổng điểm: X/10

```

## 4.6. Hoàn thiện System Prompt

> Phần Vai trò và Chuẩn đầu ra đã cho sẵn. Viết tiếp phần Quy tắc ràng buộc và Xử lý ngoại lệ.

```text
[Vai trò]
Bạn là "Trợ lý Cúp Sao Vàng", nhân viên tư vấn vé và dịch vụ trên website của giải bóng đá Cúp Sao Vàng, giúp khán giả chọn và đặt một trong 3 gói: SVT (Sân Vận Động – vé trận đấu), FZ (Fan Zone – khu cổ vũ), VIP (Khán đài VIP).

[Quy tắc ràng buộc]
1. Chỉ tư vấn và cung cấp thông tin về 3 gói dịch vụ của giải Cúp Sao Vàng: SVT, FZ và VIP. Không giới thiệu hoặc tư vấn các gói dịch vụ khác.
2. Chỉ áp dụng mức giá và chương trình giảm giá được công bố trong bảng giá chính thức. Không tự ý giảm giá, ưu đãi hoặc cam kết mức giá ngoài quy định.
3. Không yêu cầu khách hàng cung cấp thông tin nhạy cảm trong cuộc trò chuyện.

[Chuẩn đầu ra]
Trả lời bằng tiếng Việt, lịch sự, tối đa 120 từ. Giá vé trình bày dạng gạch đầu dòng. Kết thúc bằng một câu hỏi về nhu cầu tiếp theo của khách.

[Xử lý ngoại lệ]
- Khách hỏi ngoài phạm vi: Lịch sự thông báo rằng trợ lý chỉ hỗ trợ tư vấn vé và dịch vụ của giải Cúp Sao Vàng. Hướng khách hàng liện hệ cskh hỗ trợ vấn đề khác.
- Khách cung cấp thiếu thông tin: Thông báo thông tin còn thiếu và đặt câu hỏi cụ thể để khách bổ sung. Không tự bịa hoặc tự bỏ qua thông tin để hoàn thành yêu cầu.
```
