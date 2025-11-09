# Tensile-Data-Analysis
# Dự án 1: Phân tích Dữ liệu Thí nghiệm Kéo Nén

Đây là một dự án Python đơn giản để minh họa các kỹ năng giao thoa giữa Khoa học Vật liệu và Khoa học Dữ liệu.

Dự án này tự động đọc các file dữ liệu (`.csv`) thô từ máy thí nghiệm kéo nén, sau đó:
1.  Làm sạch và xử lý dữ liệu.
2.  Tính toán các đặc tính cơ học quan trọng (Modulus Young, Độ bền kéo, Độ dãn dài).
3.  Trực quan hóa và so sánh đường cong ứng suất-biến dạng của các mẫu.

## 🛠️ Công nghệ sử dụng
* **Python**
* **Pandas:** Để tải, làm sạch và quản lý dữ liệu.
* **NumPy:** Để thực hiện các phép tính khoa học (đặc biệt là `polyfit` để tìm Modulus).
* **Matplotlib:** Để trực quan hóa kết quả.

## 🏃 Cách chạy dự án

1.  **Cài đặt thư viện:**
    ```bash
    pip install pandas numpy matplotlib
    ```

2.  **Chuẩn bị dữ liệu:**
    Tạo các file `sample_A.csv` và `sample_B.csv` (hoặc bất kỳ file `.csv` nào có 2 cột `Displacement(mm)` và `Force(N)`) trong cùng thư mục.

3.  **Chạy script:**
    ```bash
    python analyze_tensile_data.py
    ```

## 📊 Kết quả

Script sẽ tự động tạo ra một biểu đồ so sánh các mẫu và lưu lại dưới dạng `output_stress_strain_curves.png`.

#### Biểu đồ Ứng suất - Biến dạng
![Biểu đồ Stress-Strain](output_stress_strain_curves.png)

#### Bảng Tổng hợp Đặc tính
Script cũng sẽ in ra một bảng so sánh các đặc tính đã tính toán (ở định dạng Markdown):

| Sample Name | Young's Modulus (GPa) | UTS (MPa) | Fracture Strain (%) |
|:------------|:------------------------|:----------|:----------------------|
| sample_A | 25.07 | 680.00 | 4.40 |
| sample_B | 33.32 | 792.00 | 4.00 |

*(Lưu ý: Các con số này có thể thay đổi một chút dựa trên dữ liệu)*

## 🔬 Ý nghĩa (Context)
Dự án này mô phỏng một tác vụ cơ bản nhưng quan trọng trong R&D vật liệu. Việc tự động hóa quy trình này giúp các nhà nghiên cứu tiết kiệm thời gian, giảm lỗi do tính toán thủ công và dễ dàng so sánh hàng chục mẫu thử một cách trực quan.
