# Báo cáo Phân tích Gene Kháng kháng sinh và Độc lực (*B. siamensis* B01)

## 1. Phương pháp phân tích (Methodology)

Phân tích gene kháng kháng sinh (AMR) và gene độc lực (VF) trên bộ gene của chủng B01 (*Bacillus siamensis*) được thực hiện bằng các công cụ sau:

- **Abricate (v1.2.0):** Tra cứu gene kháng kháng sinh dựa trên các cơ sở dữ liệu: **CARD**, **NCBI**, **ARG-ANNOT**, **ResFinder**, **MEGARes**, **VFDB**.
- **AMRFinderPlus (v4.0.19):** Sử dụng phương pháp BLAST và HMM để xác định các gene kháng thuốc dựa trên cơ sở dữ liệu cập nhật từ NCBI.
- **VFanalyzer:** Sử dụng phương pháp BLAST để xác định các gene độc lực dựa vào cơ sở dữ liệu **VFDB** với tham số tìm kiếm dựa vào độ tương đồng là 50%

## 2. Kết quả phân tích (Results)

### 2.1. Gene kháng kháng sinh (Antimicrobial Resistance Genes)

Dựa trên kết quả từ các cơ sở dữ liệu khác nhau, các gene kháng kháng sinh sau đây đã được xác định trong chủng B01:

| Gene | Loại kháng sinh (Resistance) | Độ tương đồng (%) | Công cụ/Cơ sở dữ liệu |
| :--- | :--- | :--- | :--- |
| **tet(L)** / **TETL** | Tetracycline | 86.42% - 87.75% | NCBI, ResFinder, MEGARes, AMRFinderPlus |
| **satA** / **SAT** | Streptothricin | 80.98% - 85.82% | NCBI, ARG-ANNOT, MEGARes, AMRFinderPlus |
| **rphC** | Rifamycin | 80.19% | NCBI |
| **fosM** | Fosfomycin | 75.36% | AMRFinderPlus |
| **bla** (class A) | Beta-lactam | 63.19% | AMRFinderPlus |
| **bla** (subclass B1) | Beta-lactam | 51.09% | AMRFinderPlus |

**Nhận xét:** 
- Chủng B01 mang các gene kháng kháng sinh thuộc nhiều nhóm khác nhau như Tetracycline, Streptothricin, Rifamycin, Fosfomycin và Beta-lactam.
- Gene **tet(L)** và **satA** được tìm thấy bởi hầu hết các cơ sở dữ liệu với độ tương đồng khá cao (>80%).
- Các gene **bla** (beta-lactamase) được tìm thấy bởi AMRFinderPlus với độ tương đồng thấp (51.09% - 63.19%), có thể là các biến thể chưa được định danh đầy đủ.

### 2.2. Gene độc lực (Virulence Factors)

Kết quả phân tích gene độc lực được lưu trong **B01_VFanalyzer.xlsx**

## 3. Kết luận (Conclusion)

Chủng vi khuẩn B01 (*Bacillus siamensis*) mang các gene kháng kháng sinh thuộc nhóm tetracycline, streptothricin, rifamycin, fosfomycin, beta-lactam và có thể mang một số gene độc lực theo cơ sở dữ liệu **VFDB**.
