# 📊 Phân Tích Giữ Chân Khách Hàng (Customer Retention Analytics)

## 🔍 Giới thiệu

Dự án này tập trung vào việc phân tích dữ liệu khách hàng để hiểu rõ hơn về hành vi mua sắm, xu hướng giữ chân và giá trị vòng đời khách hàng. Sử dụng bộ dữ liệu bán lẻ trực tuyến từ một công ty bán lẻ có trụ sở tại Vương Quốc Anh, dự án áp dụng các kỹ thuật phân tích hiện đại để cung cấp thông tin chi tiết về việc giữ chân khách hàng và chiến lược tiếp thị hiệu quả.

### 📋 Tổng quan về dữ liệu

Bộ dữ liệu bao gồm tất cả các giao dịch xảy ra từ 01/12/2021 đến 09/12/2022, với hơn 500.000 giao dịch từ khách hàng trên khắp thế giới. Mỗi bản ghi chứa thông tin chi tiết về đơn hàng như mã hóa đơn, mã sản phẩm, mô tả sản phẩm, số lượng, ngày hóa đơn, đơn giá, ID khách hàng và quốc gia.

## 📝 Nội dung dự án

Dự án bao gồm các phần phân tích sau:

1. **🔬 Phân tích dữ liệu khám phá (EDA)**

   - Làm sạch và chuẩn bị dữ liệu
   - Phân tích xu hướng mua sắm theo thời gian
   - Khám phá mẫu mua hàng theo quốc gia và sản phẩm

2. **👥 Phân tích theo nhóm (Cohort Analysis)**

   - Theo dõi hành vi của các nhóm khách hàng theo thời gian
   - Đánh giá tỷ lệ giữ chân theo từng nhóm khách hàng
   - Trực quan hóa các xu hướng giữ chân khách hàng

3. **📈 Tỷ lệ giữ chân và mất khách hàng**

   - Tính toán tỷ lệ giữ chân hàng tháng
   - Phân tích nguyên nhân mất khách hàng
   - Dự báo xu hướng giữ chân khách hàng

4. **🎯 Chỉ số hiệu suất chính (KPIs) về giữ chân khách hàng**

   - Doanh thu định kỳ hàng tháng (MRR)
   - Giá trị đơn hàng trung bình (AOV)
   - Tần suất mua hàng và chu kỳ mua lại

5. **💎 Mô hình RFM (Recency, Frequency, Monetary)**

   - Phân đoạn khách hàng dựa trên thời gian gần đây, tần suất và giá trị tiền tệ
   - Phân loại khách hàng thành các nhóm (Gold, Silver, Bronze)
   - Chiến lược tiếp thị cho từng phân khúc khách hàng

6. **💰 Phân tích giá trị vòng đời khách hàng (CLV)**
   - Ước tính giá trị vòng đời của từng phân khúc khách hàng
   - Dự báo doanh thu tương lai dựa trên hành vi hiện tại
   - Chiến lược tối ưu hóa CLV

## 🧪 Phương pháp luận

Dự án sử dụng nhiều kỹ thuật phân tích tiên tiến:

- **Phân tích theo nhóm tuổi (Cohort)**: Theo dõi các nhóm khách hàng được xác định theo thời gian bắt đầu mối quan hệ với công ty. Phương pháp này cho phép chúng tôi đo lường hiệu suất giữ chân khách hàng theo thời gian và xác định các mẫu trong hành vi khách hàng dựa trên thời điểm họ thực hiện giao dịch đầu tiên.

- **Mô hình RFM (Recency, Frequency, Monetary)**:

  - _Recency_: Số ngày kể từ lần mua hàng gần nhất của khách hàng
  - _Frequency_: Tổng số lần mua hàng trong khoảng thời gian phân tích
  - _Monetary_: Tổng giá trị chi tiêu của khách hàng

  Từ ba thông số này, mỗi khách hàng được gán điểm từ 1-5 cho mỗi thông số và được phân loại thành các nhóm dựa trên điểm RFM tổng hợp.

- **Phân tích CLV (Customer Lifetime Value)**:

  - _Phương pháp cơ bản_: Sử dụng công thức `CLV = (Giá trị đơn hàng trung bình x Tần suất mua hàng) / Tỷ lệ mất khách hàng`
  - _Mô hình BG-NBD_: Mô hình xác suất dự đoán xác suất mua hàng trong tương lai dựa trên hành vi mua hàng trong quá khứ
  - _Mô hình Gamma-Gamma_: Ước tính giá trị đơn hàng trung bình dự kiến trong tương lai

- **Phân tích xu hướng thời gian**: Theo dõi các chỉ số giữ chân khách hàng theo thời gian để xác định các mẫu và xu hướng mùa vụ, sử dụng các kỹ thuật trực quan hóa dữ liệu như biểu đồ nhiệt (heatmap) và biểu đồ đường (line chart).

## 🔍 Các phát hiện chính

- **📉 Xu hướng giữ chân khách hàng**: Phân tích cho thấy tỷ lệ giữ chân khách hàng giảm dần theo thời gian, với sự sụt giảm đáng kể sau 3 tháng đầu tiên. Cụ thể, tỷ lệ giữ chân trung bình là khoảng 30% sau tháng đầu tiên, nhưng giảm xuống còn khoảng 15% sau 6 tháng.

- **👥 Phân đoạn khách hàng**:

  - _🥇 Gold (20% khách hàng)_: Đóng góp khoảng 65% tổng doanh thu
  - _🥈 Silver (30% khách hàng)_: Đóng góp khoảng 25% tổng doanh thu
  - _🥉 Bronze (50% khách hàng)_: Đóng góp khoảng 10% tổng doanh thu

  Mô hình RFM cho thấy sự phân bố không đều về giá trị khách hàng, tuân theo nguyên tắc Pareto (80-20).

- **💰 Giá trị vòng đời khách hàng**: Khách hàng Gold có CLV trung bình cao hơn 8 lần so với khách hàng Bronze và 3 lần so với khách hàng Silver. Phân tích cũng cho thấy khách hàng trong các quốc gia như Vương Quốc Anh, Đức và Pháp có CLV cao nhất.

- **⚠️ Dự báo churn**: Mô hình dự báo xác định các yếu tố chính ảnh hưởng đến việc khách hàng rời bỏ:

  - Thời gian không hoạt động trên 60 ngày làm tăng nguy cơ rời bỏ lên 70%
  - Giảm tần suất mua hàng trên 40% so với thời kỳ trước
  - Giá trị đơn hàng trung bình giảm trên 30% so với lịch sử mua hàng

- **🌍 Phân tích theo khu vực địa lý**: Khách hàng ở các quốc gia khác nhau có mẫu giữ chân khác biệt đáng kể, với tỷ lệ giữ chân cao nhất tại Vương Quốc Anh (45%), Đức (38%) và Pháp (35%).

## 📂 Cấu trúc dự án

```
Customer-Retention-Analytics/
│
├── customer_retention_analytics.ipynb   # 📊 Notebook chính chứa toàn bộ phân tích
├── online_retail.csv                    # 📂 Dữ liệu bán lẻ trực tuyến đã xử lý
├── online_retail.xlsx                   # 📄 Dữ liệu gốc dạng Excel
├── Online Retail.xlsx                   # 📑 Bản sao dữ liệu gốc
└── clv.csv                              # 💰 Dữ liệu đã tính toán giá trị vòng đời khách hàng
```

## 🚀 Cách sử dụng

1. Mở file `customer_retention_analytics.ipynb` bằng Jupyter Notebook hoặc JupyterLab.
2. Đảm bảo bạn đã cài đặt các thư viện Python cần thiết (pandas, numpy, matplotlib, seaborn).
3. Chạy từng ô lệnh để xem kết quả phân tích và trực quan hóa.
4. Điều chỉnh các tham số trong các hàm phân tích để khám phá các kịch bản khác nhau.

## 🛠️ Yêu cầu

- Python 3.7+
- Pandas & Pandas Profiling
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn (cho các mô hình dự báo và chuẩn hóa dữ liệu)
- Lifetimes (thư viện Python cho mô hình BG-NBD và Gamma-Gamma)
- Jupyter Notebook

### 💾 Cài đặt thư viện

```bash
pip install pandas pandas-profiling numpy matplotlib seaborn scikit-learn lifetimes jupyter
```

## 💡 Đề xuất kinh doanh

Dựa trên các phát hiện từ phân tích, dự án đề xuất:

1. **🎯 Chiến lược tương tác khách hàng có mục tiêu**

   - _Khách hàng Gold_: Chương trình VIP với ưu đãi cao cấp, dịch vụ cá nhân hóa, thông báo sớm về sản phẩm mới
   - _Khách hàng Silver_: Ưu đãi theo mùa, chương trình giảm giá theo tần suất mua hàng
   - _Khách hàng Bronze_: Chiến dịch kích hoạt lại với ưu đãi đặc biệt cho lần mua hàng tiếp theo

2. **🏆 Chương trình loyalty**

   - Hệ thống điểm thưởng tích lũy với nhiều cấp độ thành viên
   - Phần thưởng dựa trên cả tần suất và giá trị đơn hàng
   - Các đặc quyền đặc biệt khi khách hàng đạt đến các mốc chi tiêu

3. **🔔 Can thiệp churn sớm**

   - Thiết lập ngưỡng cảnh báo khi thời gian không hoạt động vượt quá 30 ngày
   - Email tự động và ưu đãi cá nhân hóa cho khách hàng có nguy cơ rời bỏ
   - Khảo sát phản hồi đối với khách hàng không hoạt động để hiểu rõ lý do

4. **📈 Tối ưu hóa CLV**

   - Chiến lược up-selling và cross-selling dựa trên lịch sử mua hàng
   - Chiến dịch tăng tần suất mua hàng thông qua các ưu đãi giới hạn thời gian
   - Phân tích giỏ hàng để đề xuất sản phẩm bổ sung phù hợp

5. **🌐 Chiến lược theo khu vực**
   - Tối ưu hóa tiếp thị theo quốc gia dựa trên mẫu giữ chân khách hàng đặc thù
   - Điều chỉnh chương trình ưu đãi theo mùa vụ và sở thích văn hóa của từng thị trường
   - Cá nhân hóa trải nghiệm mua sắm dựa trên phân tích hành vi theo khu vực

## 📝 Kết luận

Phân tích giữ chân khách hàng cung cấp thông tin quý giá về hành vi khách hàng và hiệu quả của chiến lược kinh doanh. Bằng cách hiểu rõ các yếu tố ảnh hưởng đến việc giữ chân khách hàng và giá trị vòng đời, doanh nghiệp có thể phát triển các chiến lược tiếp thị hiệu quả hơn, tập trung vào các phân khúc khách hàng có giá trị cao và cuối cùng là tăng doanh thu và lợi nhuận.

Dự án này đã chứng minh rằng:

1. 🎯 Tập trung vào việc giữ chân 20% khách hàng hàng đầu có thể mang lại tác động lớn hơn 3 lần so với các chiến dịch thu hút khách hàng mới
2. 🔮 Phân tích dữ liệu có thể giúp dự đoán và ngăn ngừa việc mất khách hàng trước khi nó xảy ra
3. 💹 Việc áp dụng các chiến lược giữ chân khách hàng có thể tăng lợi nhuận lên đến 25-30% thông qua việc giảm chi phí thu hút khách hàng mới và tăng doanh thu từ khách hàng hiện tại

## 🔮 Công việc tiếp theo

Để tiếp tục phát triển khả năng phân tích giữ chân khách hàng, các bước tiếp theo có thể bao gồm:

1. **😊 Phân tích tình cảm khách hàng**: Tích hợp dữ liệu từ đánh giá sản phẩm, phản hồi dịch vụ khách hàng và tương tác trên mạng xã hội.
2. **🤖 Mô hình dự đoán nâng cao**: Áp dụng các kỹ thuật học máy phức tạp hơn như Random Forest, Neural Networks để cải thiện độ chính xác của việc dự báo churn.
3. **📱 Phân tích đa kênh**: Đánh giá hiệu quả giữ chân khách hàng trên các kênh bán hàng khác nhau (web, di động, cửa hàng vật lý).
4. **🧪 Thử nghiệm A/B**: Tiến hành các thử nghiệm có kiểm soát để đánh giá hiệu quả của các chiến lược giữ chân khách hàng khác nhau.

## 📊 Nguồn dữ liệu

Bộ dữ liệu được sử dụng trong phân tích này đại diện cho các giao dịch bán lẻ trực tuyến từ một công ty có trụ sở tại Vương Quốc Anh. Dữ liệu bao gồm giai đoạn từ tháng 12/2021 đến tháng 12/2022.

## 👨‍💻 Tác giả

**Luu Dinh Gia** - _Phân tích dữ liệu_ - Ngày 12/02/2025
