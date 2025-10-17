# 🧭 HỆ THỐNG ĐỊNH GIÁ & BACKTEST - SƠ ĐỒ KIẾN TRÚC

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         🧭 ORCHESTRATOR (LLM FINE-TUNE)                     │
├─────────────────────────────────────────────────────────────────────────────┤
│  📋 Lập kế hoạch          🧩 Điều phối tác vụ        🔁 Vòng lặp refine      │
│  → lịch chạy T1..Tn       → gọi Agent/Tool           đọc diagnostics &       │
│                                                      metrics                 │
└─────────────────────┬───────────────────────────────────────┬───────────────┘
                      │                                       │
                      ▼                                       ▼
┌─────────────────────────────────────┐    ┌─────────────────────────────────┐
│        📚 DATA LAYER (PIT)          │    │        🤖 MULTI-AGENT           │
├─────────────────────────────────────┤    ├─────────────────────────────────┤
│ 🗂️ BCTC PIT                        │    │ 🧪 Data Agent                  │
│ (as-reported, filed_date ≤ T)       │    │ PIT fetch & QC                  │
│                                     │    │                                 │
│ 💹 Giá & Cổ tức PIT                │◄───┤ 🧮 Preprocess Agent             │
│ (đã điều chỉnh corporate actions)   │    │ Chuẩn hoá & FCFF features       │
│                                     │    │ + Priors/Bands                  │
│ 🏦 Lãi suất, Beta, FX,             │    │                                 │
│ Sector stats (T)                    │    │ 📊 Metrics & Compare Agent      │
└─────────────────────────────────────┘    │ So sánh Market & tính           │
                      │                    │ MAPE/RMSE/IC                    │
                      │                    │                                 │
                      ▼                    │ 🔍 Audit Agent                 │
┌─────────────────────────────────────┐    │ Rule + LLM giải thích           │
│       🧰 VALUATION MODULE           │◄───┤ sai số, drift                  │
├─────────────────────────────────────┤    └─────────────────────────────────┘
│ 📈 DCF Engine                      │                      │
│ EV, Equity/Share                    │                      │
│                                     │                      ▼
│ 🧷 Sensitivity                     │    ┌─────────────────────────────────┐
│ WACC × g∞, Margin                  │    │      🗃️ LƯU TRỮ & BACKTEST      │
│                                     │    ├─────────────────────────────────┤
│ 🎲 Monte Carlo (tuỳ chọn)          │───►│ 📀 financial_snapshot_pit       │
│                                     │    │                                 │
│ 🧭 Scenario Base/Bull/Bear         │    │ 💾 valuation_run @T             │
│                                     │    │                                 │
│ 📐 Comps/FCFE kiểm định chéo       │    │ 📊 market_reference             │
└─────────────────────────────────────┘    │                                 │
                      │                    │ 🧮 backtest_metrics             │
                      │                    └─────────────────┬───────────────┘
                      ▼                                      │
┌─────────────────────────────────────┐                      ▼
│       🖥️ DASHBOARD & BÁO CÁO        │    ┌─────────────────────────────────┐
├─────────────────────────────────────┤    │    🗓️ WALK-FORWARD BACKTEST     │
│ 📉 Trend lỗi theo thời gian        │    │           3-5 năm               │
│                                     │    ├─────────────────────────────────┤
│ 📈 Calibration / Hit-rate          │    │  T1 ──► T2 ──► T3 ──► ... ──► Tn │
│                                     │    │ Snapshot Snapshot Snapshot     │
│ 🧩 Value Bridge / Reverse DCF      │    │                                 │
└─────────────────────────────────────┘    └─────────────────────────────────┘
```

## 🔄 LUỒNG DỮ LIỆU CHÍNH

### 1. **Khởi tạo & Lập kế hoạch**
```
Orchestrator → Lịch chạy T1..Tn → Data Agent
```

### 2. **Thu thập dữ liệu Point-in-Time**
```
Data Agent → BCTC PIT + Giá cổ phiếu + Market data → Snapshot PIT
```

### 3. **Xử lý & Chuẩn bị**
```
Preprocess Agent → FCFF, WACC, g∞, Priors → Valuation Module
```

### 4. **Định giá**
```
Valuation Module → {DCF, Sensitivity, Monte Carlo, Scenarios, Comps} → Results
```

### 5. **So sánh & Đánh giá**
```
Metrics Agent → So sánh với Market → MAPE/RMSE/IC → Backtest Metrics
```

### 6. **Kiểm toán & Cải thiện**
```
Audit Agent → Phân tích sai số → Đề xuất cải thiện → Orchestrator
```

## 📊 CẤU TRÚC DỮ LIỆU

### **Point-in-Time Data Layer**
- **BCTC PIT**: Báo cáo tài chính theo thời điểm thực
- **Price PIT**: Giá cổ phiếu đã điều chỉnh corporate actions  
- **Market PIT**: Lãi suất, Beta, FX, thống kê ngành

### **Valuation Results Storage**
- **Snapshot**: Dữ liệu tại từng thời điểm T
- **Valuation Run**: Kết quả định giá chi tiết
- **Backtest Metrics**: Độ chính xác theo thời gian

## 🎯 TÍNH NĂNG CHÍNH

### **Multi-Agent Architecture**
- **Data Agent**: Thu thập & kiểm tra chất lượng dữ liệu
- **Preprocess Agent**: Chuẩn hóa & tính toán features
- **Metrics Agent**: So sánh với thị trường, tính độ chính xác
- **Audit Agent**: Phân tích lỗi & đề xuất cải thiện

### **Valuation Engine**
- **DCF Core**: Tính EV, Equity value, giá/cổ phiếu
- **Sensitivity Analysis**: Phân tích độ nhạy WACC × tăng trưởng vĩnh viễn
- **Monte Carlo**: Mô phỏng phân phối giá trị (tùy chọn)
- **Scenario Analysis**: Base/Bull/Bear scenarios
- **Cross-validation**: Kiểm tra chéo với Comps/FCFE

### **Continuous Improvement Loop**
```
Results → Audit → Diagnostics → Refinement → Improved Assumptions
```

## 🚀 TRIỂN KHAI WALK-FORWARD

1. **Timeline**: Backtest 3-5 năm với snapshots định kỳ
2. **Point-in-Time**: Đảm bảo không có look-ahead bias
3. **Progressive Learning**: Cải thiện model qua từng chu kỳ
4. **Performance Tracking**: Theo dõi độ chính xác theo thời gian
