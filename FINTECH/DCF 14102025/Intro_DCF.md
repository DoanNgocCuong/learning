DCF (Discounted Cash Flow - Dòng tiền chiết khấu) là một **phương pháp định giá doanh nghiệp**, không phải là một chỉ tiêu cụ thể trong báo cáo kết quả kinh doanh mà bạn đang xem.[](https://vneconomy.vn/toan-canh-buc-tranh-kinh-doanh-quy-2-2024.htm)​

## 1. Giải thích về DCF

DCF là công cụ phân tích tài chính dùng để ước tính giá trị doanh nghiệp dựa trên dòng tiền tự do trong tương lai được chiết khấu về giá trị hiện tại. Để tính DCF, nhà đầu tư cần:[](https://vneconomy.vn/toan-canh-buc-tranh-kinh-doanh-quy-2-2024.htm)​

- **Báo cáo lưu chuyển tiền tệ** (Cash Flow Statement) - không phải báo cáo kết quả kinh doanh như bạn đang có
    
- Dự báo dòng tiền tự do (Free Cash Flow) cho 5-10 năm tới
    
- Xác định tỷ lệ chiết khấu (WACC - Weighted Average Cost of Capital)
    
- Tính giá trị cuối kỳ (Terminal Value)


---
https://www.prudential.com.vn/vi/blog-nhip-song-khoe/cach-doc-bao-cao-tai-chinh-de-quan-ly-dau-tu-hieu-qua/

Doanh thu, chi phí, hàng tồn kho, khấu hao, dòng tiền thuần từ kết quả kinh doanh, khoản nợ ngắn hạn, nợ dài hạn. 
- **Báo cáo lưu chuyển tiền tệ** (Cash Flow Statement) - không phải báo cáo kết quả kinh doanh như bạn đang có

- Dự báo dòng tiền tự do (Free Cash Flow) cho 5-10 năm tới

- Xác định tỷ lệ chiết khấu (WACC - Weighted Average Cost of Capital)

- Tính giá trị cuối kỳ (Terminal Value)

---

## 🏦 1. Các trang tài chính Việt Nam phổ biến & đáng tin cậy

|Trang|Loại dữ liệu|Cấu trúc HTML / API|Ưu điểm|Nhược điểm|
|---|---|---|---|---|
|**Cafef.vn** (thuộc VCCorp)|Báo cáo tài chính, lịch sử giá, chỉ số PE, EPS, dòng tiền|HTML có cấu trúc tương đối ổn (`div#divTableData`)|Có hầu hết công ty VN|Không có API, cần xử lý AJAX + rate limit|
|**Vietstock.vn**|Báo cáo tài chính chi tiết, phân tích, chỉ số, DCF|HTML và JS dynamic|Dữ liệu đầy đủ, cập nhật nhanh|JS render (phải dùng Selenium/Playwright)|
|**SSI iBoard / FiinTrade / FiinPro**|Real-time quotes, phân tích cơ bản|Có API riêng (cần key hoặc mua gói)|Ổn định, chuyên nghiệp|Trả phí, hạn chế request|
|**HNX / HOSE / UPCoM websites**|Báo cáo gốc (PDF, Excel)|File link cố định theo năm|Chính thức, nguồn xác thực|Khó parse, PDF thường là scan|
|**Company IR websites** (ví dụ: QTP.com.vn, POW.vn)|Báo cáo gốc (PDF)|Tên file có pattern|Đảm bảo chính xác|Cần crawl từng công ty riêng|
|**Investing.com / TradingView / Yahoo Finance (VN)**|Giá cổ phiếu, chỉ số, lịch sử|Có API ẩn / JSON endpoint|Dễ crawl, nhẹ|Không có dữ liệu dòng tiền chi tiết|

# 3. Các chỉ số nhỏ ảnh hưởng đến DCF 

|Nhóm chỉ số|Chỉ số con|Ảnh hưởng đến DCF|Nguồn trích xuất|
|---|---|---|---|
|1. Tăng trưởng Doanh thu|Revenue growth rate|Tăng dòng tiền tương lai|Mở nhà máy, sản phẩm mới, mở rộng thị trường|
||Market expansion|Tăng quy mô kinh doanh|Khai trương chi nhánh, xuất khẩu|
||M&A (Acquire)|Tăng doanh thu hợp nhất|Thông báo mua lại công ty|
||Product Launch|Đóng góp từ sản phẩm mới|Ra mắt sản phẩm/dịch vụ|
||Price adjustment|Ảnh hưởng giá bán|Thay đổi chính sách giá|
||Capacity increase|Tăng công suất sản xuất|Mở rộng nhà máy, thiết bị mới|
|2. Biên lợi nhuận & Chi phí|EBITDA margin delta|Ảnh hưởng lợi nhuận hoạt động|Tái cấu trúc, tối ưu chi phí|
||Operating margin change|Thay đổi hiệu quả hoạt động|Tự động hóa, nâng cấp công nghệ|
||OPEX ratio delta|Thay đổi chi phí vận hành|Cắt giảm nhân sự, tối ưu quy trình|
||Raw material cost impact|Ảnh hưởng giá nguyên liệu|Biến động giá thép, sữa, dầu|
||Energy & logistics cost|Chi phí năng lượng/vận chuyển|Giá xăng dầu, điện, logistics|
|3. Đầu tư vốn (CAPEX)|CAPEX delta|Ảnh hưởng dòng tiền đầu tư|Xây nhà máy, mua thiết bị|
||Asset disposal|Thu tiền từ thanh lý tài sản|Bán nhà máy, thiết bị cũ|
||Maintenance CAPEX|Vốn duy trì hoạt động|Bảo trì định kỳ|
||Growth CAPEX|Vốn mở rộng|Dự án mới, mở rộng công suất|
||Depreciation|Khấu hao tài sản|Hạch toán kế toán|
|4. Vốn lưu động|Working capital ratio delta|Hiệu quả quản lý vốn|Thay đổi chính sách thu hồi nợ|
||Days Sales Outstanding (DSO)|Kỳ thu tiền|Quản lý công nợ khách hàng|
||Days Inventory Outstanding (DIO)|Kỳ tồn kho|Quản lý hàng tồn kho|
||Days Payable Outstanding (DPO)|Kỳ trả tiền nhà cung cấp|Điều khoản thanh toán|
|5. Chi phí vốn (WACC)|WACC delta|Ảnh hưởng tỷ lệ chiết khấu|Thay đổi cấu trúc vốn|
||Risk premium delta (bps)|Thay đổi phần bù rủi ro|Kiện tụng, scandal, thay CEO|
||Debt-to-Equity ratio|Cơ cấu nợ/vốn|Phát hành trái phiếu/cổ phiếu|
||Interest expense delta|Chi phí lãi vay|Vay mới, tái cơ cấu nợ|
||Credit rating change|Xếp hạng tín dụng|Nâng/hạ hạng tín nhiệm|
|6. Thuế & Chính sách|Effective tax rate delta|Suất thuế hiệu dụng|Thay đổi luật thuế, ưu đãi|
||Tax incentive benefit|Lợi ích ưu đãi thuế|Chính sách hỗ trợ doanh nghiệp|
||Regulatory compliance cost|Chi phí tuân thủ|Quy định mới về môi trường|
||Tariff impact|Ảnh hưởng thuế quan|Chính sách thuế nhập khẩu|
|7. Rủi ro & Phi hoạt động|Litigation exposure|Kiện tụng, phạt|Thông báo kiện tụng, vi phạm|
||Non-operating cash outflow|Dòng tiền ngoài hoạt động|Chi phí phạt, bồi thường|
||One-time charges/gains|Chi phí/lợi ích một lần|Thanh lý tài sản, tái cơ cấu|
||Probability-weighted scenarios|Kịch bản có xác suất|Phân tích Monte Carlo|
|8. Quản trị & ESG|Leadership change|Thay đổi ban lãnh đạo|Thay CEO/CFO/Chủ tịch|
||ESG rating change|Xếp hạng ESG|Đầu tư bền vững, môi trường|
||Governance quality|Chất lượng quản trị|Scandal, gian lận, minh bạch|
||Strategic shift|Thay đổi chiến lược|Chuyển đổi mô hình kinh doanh|
|9. Đổi mới & Tài sản vô hình|R&D investment|Đầu tư nghiên cứu phát triển|Chi tiêu R&D, đổi mới công nghệ|
||Patent/IP acquisition|Mua bản quyền/sáng chế|Thương vụ mua IP, cấp phép|
||Brand investment|Đầu tư thương hiệu|Chi phí marketing, PR|
||Technology adoption|Áp dụng công nghệ mới|AI, tự động hóa, chuyển đổi số|
|10. Dòng tiền tự do (Output)|Free Cash Flow to Firm (FCFF)|Dòng tiền tự do công ty|Tổng hợp từ các nhóm trên|
||Free Cash Flow to Equity (FCFE)|Dòng tiền tự do cổ đông|FCFF trừ đi nghĩa vụ nợ|
||Terminal Value|Giá trị cuối kỳ|Perpetuity growth method|
||Enterprise Value (EV)|Giá trị doanh nghiệp|NPV của FCFF + Terminal Value|
||Equity Value|Giá trị vốn cổ phần|EV trừ nợ ròng|

---
# 1. Giải thích công thức DCF đơn giản

**Công thức DCF** giúp chúng ta biết một công ty đáng giá bao nhiêu tiền nếu ta biết nó sẽ kiếm được bao nhiêu tiền trong tương lai.

## Công thức DCF là gì?

DCF là viết tắt của "Discounted Cash Flow". Nó giống như việc bạn tính xem số tiền bạn sẽ nhận được trong tương lai thì hôm nay có giá trị bao nhiêu.

## Ví dụ dễ hiểu

Giả sử bạn sẽ nhận được 100.000 đồng từ bố mẹ sau 1 năm. Nhưng nếu bạn muốn biết số tiền đó hôm nay có giá trị bao nhiêu, bạn phải trừ đi một chút vì phải chờ đợi (giống như "chiết khấu").

## Công thức đơn giản:

![[image/Pasted image 20251014233806.png]]

- **Tiền năm 1, năm 2...** là số tiền công ty sẽ kiếm được mỗi năm.
    
- **Tỉ lệ chiết khấu** là phần trăm bạn trừ đi vì phải chờ đợi (giống như "lãi suất ngân hàng").
    

## Ý nghĩa

- Nếu bạn nhận tiền sớm thì giá trị lớn hơn.
    
- Nếu phải chờ lâu, giá trị hôm nay sẽ nhỏ hơn.
    

**Tóm lại:**

- DCF giúp bạn biết số tiền trong tương lai hôm nay có giá trị bao nhiêu.
    
- Càng phải chờ lâu, giá trị càng nhỏ.
    

Nếu em muốn thử tính với số tiền cụ thể, hãy nói cho thầy biết nhé!

---
### **Tỉ lệ chiết khấu** (thường là WACC - Weighted Average Cost of Capital) được tính để phản ánh rủi ro và chi phí sử dụng vốn của doanh nghiệp. Nó dùng làm “lãi suất chiết khấu” để quy đổi giá trị dòng tiền tương lai về hiện tại.

Công thức phổ biến nhất để tính WACC là:

$\mathrm{WACC} = \frac{E}{V} r_e + \frac{D}{V} r_d (1 - T)$


Trong đó:

- EEE: Giá trị vốn cổ phần (Equity)
    
- DDD: Giá trị nợ (Debt)
    
- V=E+DV = E + DV=E+D: Tổng giá trị vốn
    
- rer_ere: Chi phí vốn cổ phần (thường dựa trên kỳ vọng lợi suất cổ đông, ví dụ bằng mô hình CAPM)
    
- rdr_drd: Chi phí nợ (lãi suất vay ngân hàng)
    
- TTT: Thuế suất doanh nghiệp
    

**Các bước tổng quát:**

1. Xác định cấu trúc vốn (tỷ lệ nợ/vốn chủ sở hữu).
    
2. Tính chi phí cho từng loại vốn:
    
    - Chi phí nợ: lãi suất thực trả cho ngân hàng/trái phiếu, đã trừ thuế.
        
    - Chi phí vốn cổ phần: thường dùng mô hình CAPM.
        
3. Ghép tỷ lệ từng loại vốn và cộng lại theo trọng số.
    

**Ý nghĩa:** Tỉ lệ chiết khấu càng cao thì kỳ vọng lợi nhuận/rủi ro của nhà đầu tư càng lớn, giá trị hiện tại của dòng tiền tương lai sẽ càng thấp.

Tóm lại: **WACC** là chỉ số tổng hợp chi phí vốn, dùng để chiết khấu các dòng tiền dự báo trong mô hình DCF về hiện tại. Bạn sẽ cần số liệu về vốn cổ phần, nợ, lãi suất vay, lãi suất kỳ vọng cổ đông, thuế...[perplexity](https://www.perplexity.ai/search/mece-cac-nhom-chi-so-can-tinh-HUgedURhQiq0gNW_lh_ygw)​

1. [https://www.perplexity.ai/search/mece-cac-nhom-chi-so-can-tinh-HUgedURhQiq0gNW_lh_ygw](https://www.perplexity.ai/search/mece-cac-nhom-chi-so-can-tinh-HUgedURhQiq0gNW_lh_ygw)