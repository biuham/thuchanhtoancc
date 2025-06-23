# Nhập Môn Xử Lý Ảnh Số - Lab 2  

**Sinh viên thực hiện:** [Tên sinh viên] **MSSV:** [Mã số sinh viên]  
**Môn học:** Nhập môn Xử lý ảnh số  
**Giảng viên:** Phan Hồ Viết Trường  

---

## Giới thiệu  
Bài lab này trình bày các phép biến đổi cường độ ảnh cơ bản để tăng cường tương phản và chi tiết hình ảnh[1].

---

## Các phép biến đổi  

### 1. Negative Transformation  
- **Ý chính:** Đảo ngược giá trị pixel, biến vùng sáng thành tối và ngược lại[2].  
- **Công thức:** $$s = L - 1 - r$$[3].  
- **Ví dụ:** Pixel 100 → 155 (255 - 100)[4].

### 2. Log Transformation  
- **Ý chính:** Khuếch đại pixel nhỏ, làm rõ vùng tối[5].  
- **Công thức:** $$s = c \times \log(1 + r)$$[6].  
- **Ví dụ:** Pixel 10 sáng lên nhiều hơn pixel 200.

### 3. Gamma Correction  
- **Ý chính:** Điều chỉnh độ sáng tổng thể bằng tham số γ[7].  
- **Công thức:** $$s = c \times r^\gamma$$[8].  
- **Ví dụ:** γ = 0.5 → ảnh sáng; γ = 2.0 → ảnh tối.

### 4. Histogram Equalization  
- **Ý chính:** Phân phối lại mức xám để tăng độ tương phản sử dụng CDF[9].  
- **Ví dụ:** Dải 50–150 mở rộng thành 0–255.

### 5. Contrast Stretching  
- **Ý chính:** Kéo giãn tuyến tính dải pixel[10].  
- **Công thức:** $$s = \frac{255\,(r - a)}{b - a}$$.

### 6. FFT & Butterworth Filtering  
- **FFT:** Chuyển ảnh sang miền tần số để lọc nhiễu hoặc nâng cao cạnh[11].  
- **Butterworth:** $$H(u,v) = \frac{1}{1 + (D(u,v)/D_0)^{2n}}$$[12].

---
## Hướng dẫn sử dụng  
1. Cài đặt: `pip install pillow numpy matplotlib scipy`[13]  
2. Chạy: Mở Jupyter Notebook và thực thi các cell từng bước[14]  
3. Tùy chỉnh: Thay đổi tham số γ, D₀ để quan sát kết quả[15].

---

## Tài liệu tham khảo  
1. Gonzalez R.C., Woods R.E., Digital Image Processing.  
2. Jain A.K., Fundamentals of Digital Image Processing.  
3. Oppenheim A.V., Schafer R.W., Discrete-Time Signal Processing.  
4. Russ J.C., The Image Processing Handbook.  
5. Slide bài giảng Nhập môn Xử lý ảnh số - Văn Lang University
