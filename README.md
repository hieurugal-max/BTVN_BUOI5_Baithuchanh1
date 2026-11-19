# BÀI THỰC HÀNH 1: LẬP KẾ HOẠCH TÀI CHÍNH CÁ NHÂN BẰNG CHAIN-OF-THOUGHT

## 1. Prompt Chain-of-Thought

**Vai trò:** Bạn là chuyên gia tư vấn tài chính cá nhân, có nhiệm vụ lập kế hoạch quản lý thu nhập và chi tiêu hàng tháng.

**Nhiệm vụ:** Phân tích dữ liệu tài chính, tính toán ngân sách và đưa ra phương án phân bổ tiền hợp lý.

**Dữ liệu đầu vào:**
- Tổng thu nhập (Gross Income): 25.000.000 VNĐ.
- Thuế thu nhập cá nhân: 2.500.000 VNĐ.
- Chi phí cố định bắt buộc: 7.000.000 VNĐ.
- Các khoản nợ cần trả tối thiểu: 4.000.000 VNĐ.
- Mục tiêu tiết kiệm: Tối thiểu 20% thu nhập ròng.

**Chỉ thị Chain-of-Thought:**

Hãy suy nghĩ từng bước một và tính toán chi tiết trước khi đưa ra quyết định. Không bỏ qua các phép tính trung gian và phải kiểm tra tính chính xác của số liệu trước khi lập bảng ngân sách cuối cùng.

**Quy trình thực hiện:**

1. Bước 1: Tính thu nhập ròng sau khi trừ thuế và số tiền còn lại sau chi phí cố định.
2. Bước 2: Trừ khoản nợ tối thiểu cần thanh toán.
3. Bước 3: Trích lập khoản tiết kiệm tối thiểu 20% thu nhập ròng.
4. Bước 4: Chia số tiền còn lại theo quy tắc 50/30/20 cải tiến:
   - 50% cho nhu cầu thiết yếu phát sinh.
   - 30% cho nhu cầu cá nhân và giải trí.
   - 20% cho quỹ dự phòng.

**Yêu cầu đầu ra:**
- Phần 1: Trình bày các bước tính toán, công thức và số liệu trung gian.
- Phần 2: Lập bảng ngân sách bằng Markdown Table gồm Hạng mục, Số tiền, Tỷ lệ %, Ghi chú.
- Tổng tỷ lệ phân bổ phải bằng chính xác 100%.
- Không sử dụng Pydantic hoặc Python. Thực hiện hoàn toàn bằng Prompting logic.

---

## 2. Nhật ký suy luận logic (Reasoning Steps)

### Bước 1: Tính thu nhập ròng và số dư sau chi phí cố định

Thu nhập ròng sau thuế:

25.000.000 - 2.500.000 = 22.500.000 VNĐ.

Số tiền còn lại sau khi trừ chi phí cố định:

22.500.000 - 7.000.000 = 15.500.000 VNĐ.

### Bước 2: Phân bổ khoản tiền trả nợ tối thiểu

Trừ khoản nợ cần thanh toán hàng tháng:

15.500.000 - 4.000.000 = 11.500.000 VNĐ.

Khoản nợ này cần được ưu tiên thanh toán đúng hạn để tránh phát sinh phí phạt và lãi quá hạn.

### Bước 3: Trích lập quỹ tiết kiệm cam kết

Mục tiêu tiết kiệm tối thiểu 20% thu nhập ròng:

22.500.000 × 20% = 4.500.000 VNĐ.

Số tiền còn lại sau khi tiết kiệm:

11.500.000 - 4.500.000 = 7.000.000 VNĐ.

### Bước 4: Phân bổ chi tiêu theo quy tắc 50/30/20 cải tiến

Số tiền còn lại là 7.000.000 VNĐ. Tiếp tục chia thành ba nhóm để tránh tập trung toàn bộ tiền vào chi tiêu linh hoạt.

**1. Nhu cầu thiết yếu phát sinh (50%):**

7.000.000 × 50% = 3.500.000 VNĐ.

Dùng cho ăn uống, đi lại, vật dụng cá nhân và các nhu cầu thiết yếu phát sinh.

**2. Nhu cầu cá nhân và giải trí (30%):**

7.000.000 × 30% = 2.100.000 VNĐ.

Dùng cho mua sắm cá nhân, giải trí và các hoạt động ngoài nhu cầu thiết yếu.

**3. Quỹ dự phòng (20%):**

7.000.000 × 20% = 1.400.000 VNĐ.

Dành cho những khoản chi bất ngờ hoặc phát sinh ngoài kế hoạch.

Kiểm tra tổng số tiền:

3.500.000 + 2.100.000 + 1.400.000 = 7.000.000 VNĐ.

Như vậy, số tiền được phân bổ đầy đủ, không vượt quá ngân sách còn lại.

---

## 3. Bảng phân bổ ngân sách cuối cùng

| Hạng mục | Số tiền (VNĐ) | Tỷ lệ % | Ghi chú |
|---|---:|---:|---|
| Thuế thu nhập cá nhân | 2.500.000 | 10% | Nghĩa vụ thuế |
| Chi phí cố định | 7.000.000 | 28% | Nhà ở, điện, nước, internet |
| Trả nợ tối thiểu | 4.000.000 | 16% | Thanh toán nợ đúng hạn |
| Tiết kiệm cam kết | 4.500.000 | 18% | 20% thu nhập ròng |
| Nhu cầu thiết yếu phát sinh | 3.500.000 | 14% | Ăn uống, đi lại |
| Cá nhân và giải trí | 2.100.000 | 8,4% | Mua sắm, giải trí |
| Quỹ dự phòng | 1.400.000 | 5,6% | Chi phí phát sinh bất ngờ |
| **TỔNG CỘNG** | **25.000.000** | **100%** | **Ngân sách cân đối** |

## 4. Kiểm tra và đánh giá kết quả

- Thu nhập sau thuế: 22.500.000 VNĐ.
- Tiết kiệm cam kết: 4.500.000 VNĐ, đạt đúng 20% thu nhập ròng.
- Các khoản nợ tối thiểu được thanh toán đầy đủ.
- Quỹ dự phòng được trích riêng 1.400.000 VNĐ.
- Tổng ngân sách phân bổ: 25.000.000 VNĐ, tương ứng 100% thu nhập ban đầu.

