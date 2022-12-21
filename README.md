# Weather-forecast-using-RNN-LSTM
Project dự báo thời tiết tại một tỉnh ở miền Bắc Việt Nam bằng cách sử dụng mô hình Recurent Neural Network/ Long Short Term Memory

### Các thư viện và ngôn ngữ được sử dụng:
* `Python 3.10`: toàn bộ project đều sử dụng ngôn ngữ lập trình Python
* `Numpy`: xử lý dữ liệu số, dữ liệu dạng mảng,...
* `Pandas`: làm việc với dữ liệu dạng bảng, cụ thể là `csv` 
* `Matplotlib` và `Seaborn`: trực quan hoá dữ liệu
* `seasonal_decompose` from statsmodels.tsa.seasonal: phân rã dữ liệu dạng `seasonal` thành các yếu tố `mùa vụ`, `xu hướng`, và `phần bất định` (được sử dụng ở Data preprocessing)
* `Medfilt` from scipy.signal: lọc trung vị để giảm độ bất định của dữ liệu (được sử dụng ở Data preprocessing)
* `MinMaxScaler` from sklearn.preprocessing: scale dữ liệu về khoảng nhỏ hơn trước khi bắt đầu huấn luyện
* `Keras` from Tensorflow 2: xây dựng mô hình học máy
* `mean_absolute_error` và `BinaryAccuracy` from keras.metrics để đánh giá kết quả dự đoán của mô hình

### Cách sử dụng:
* Dữ liệu thô được lưu trữ trong folder `raw_data` dưới dạng `.csv`
* Chạy tất cả các ô trong file `Data_Preprocessing.ipynb`, dữ liệu đã xử lý sẽ được lưu vào folder `processed_data`dưới dạng `.csv`
* Sau khi đã xử lý xong dữ liệu, tiến hành huấn luyện mô hình bằng cách thực thi tất cả các ô trong file `RNN.ipynb` và `LSTM.ipynb`. Bạn có thể sửa các tham số ở block `Parameters` như `n_timestep` là số timestep, `n_timepred` là số ngày dự đoán (mô hình chỉ dự đoán 1 ngày, sau đó lấy ngày đấy làm input để dự đoán ngày tiếp theo), `train_val_test_rate` là tỷ lệ để chia tập dữ liệu thành các phần `huấn luyện`, `tối ưu`, `kiểm thử`. Mô hình sau khi huấn luyện sẽ được lưu vào folder `model` dưới dạng `.h5` với `val_loss` thấp nhất.
* Cũng trong file `RNN.ipynb` và `LSTM.ipynb`, tiến hành load mô hình tốt nhất lên và đánh giá nó
* Nhóm đã lưu các đánh giá dưới dạng hình ảnh trong folder `image`

### Thông tin liên lạc:
* Email: anh.nh204511@gmail.com
