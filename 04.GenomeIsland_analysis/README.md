# Phân tích Genomic Island (GI) và Pathogenicity Island (PAI) - Mẫu B01

## 1. Tổng quan về Genomic Island (GI)
- **Định nghĩa:** GI là các vùng DNA kích thước lớn (10-200 kb) được thu nhận thông qua chuyển gen ngang (HGT).
- **Đặc điểm nhận diện:**
    - Thành phần trình tự (%GC, Codon usage bias) khác biệt so với hệ gen gốc.
    - Chứa các gen di động (Integrase, Transposase, Recombinase).
    - Thường chèn gần các gen tRNA.
    - Mang các gen chức năng quan trọng (độc lực, kháng kháng sinh, trao đổi chất).

## 2. Phương pháp phân tích
- **Công cụ chính:** Tích hợp 3 thuật toán từ **IslandViewer 4**: IslandPick, SIGI-HMM và IslandPath-DIMOB.
- **Tiêu chí sàng lọc GI tiềm năng:**
    - **Kích thước:** Ưu tiên vùng từ 10-200 kb.
    - **Thành phần %GC:** Lệch ≥ 2–5% so với trung bình hệ gen (46.25%).
    - **Gen di động:** Kiểm tra qua **mobileOG-db** (yêu cầu coverage & identity ≥ 80%).
    - **Công cụ xác minh:** **AlienHunter** (HGT score) và **PHASTEST** (Prophage).

## 3. Kết quả phân tích GI
Sơ bộ phát hiện 11 vùng GI (kích thước 4.0 - 79.3 kb). Dưới đây là 3 vùng tiêu biểu được phân tích chi tiết:

| ID | Contig | Vị trí (Start-End) | Độ dài (bp) | %GC | Gen di động | Gắn tRNA | AlienHunter (Score) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **GI1** | 3 | 48,135 - 90,091 | 41,956 | 37.64% | Integrase/Excision | Có | 0.611 |
| **GI2** | 1 | 1,031,224 - 1,055,600 | 24,376 | 38.65% | Transfer (dut) | Không | - |
| **GI3** | 2 | 784,682 - 797,298 | 12,616 | 38.83% | Transposase (tnp_2) | Không | 0.605 |

**Đánh giá:**

- **GI1 & GI3:** Là các **GI tiềm năng cao** do thỏa mãn tiêu chí về %GC, gen di động và điểm AlienHunter (Score > 0.6). Riêng GI1 nằm cạnh tRNA, là dấu hiệu HGT điển hình.
- **GI2:** Độ tin cậy thấp do không liên kết tRNA và điểm AlienHunter không cao.
- **Prophage:** Không phát hiện vùng prophage nào trong cả 3 GI (theo PHASTEST).

## 4. Phân tích Pathogenicity Island (PAI)
- **Mục tiêu:** Xác định xem các GI tiềm năng có chứa cụm gen độc lực hay không.
- **Kết quả:** Sử dụng **VFAnalyzer (VFDB)** để kiểm tra, không phát hiện các gen độc lực đặc trưng (hệ thống bài tiết, độc tố, bám dính, xâm nhiễm) trong các vùng GI đã xác định.
- **Kết luận:** Mẫu B01 **không chứa Pathogenicity Island (PAI)**.
