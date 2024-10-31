# Nguồn gốc dữ liệu
Hiện nay, dịch vụ cho thuê xe đạp được giới thiệu ở nhiều thành phố đô thị nhằm nâng cao sự thoải mái khi di chuyển. Điều quan trọng là phải cung cấp xe đạp cho thuê và công chúng có thể tiếp cận vào đúng thời điểm vì nó giúp giảm thời gian chờ đợi. Cuối cùng, việc cung cấp cho thành phố nguồn cung cấp xe đạp cho thuê ổn định trở thành mối quan tâm lớn. Phần quan trọng là dự đoán số lượng xe đạp cần thiết mỗi giờ để cung cấp xe đạp cho thuê ổn định. Bộ dữ liệu chứa thông tin thời tiết (Nhiệt độ, Độ ẩm, Tốc độ gió, Tầm nhìn, Điểm sương, Bức xạ mặt trời, Lượng tuyết rơi, Lượng mưa), số lượng xe đạp được thuê mỗi giờ và thông tin ngày. Dữ liệu *Seoul* trong giai đoạn 01/12/2017 tới 30/11/2018, với các biến được quan sát sau:



  <ul>
   <li>Date: ngày thu thập dữ liệu: year-month-day</li>  
   <li>Rented Bike count: lượng xe đạp được thuê mỗi giờ</li>  
   <li>Hour: giờ trong ngày</li>  
   <li>Temperature: nhiệt độ ( &#870; C)</li>  
   <li>Humidity: độ ẩm (%)</li>  
   <li>Windspeed: tốc độ gió (m/s)</li>  
   <li>Visibility: tầm nhìn (10m)</li>  
   <li>Dew point temperature: nhiệt độ ngưỡng tạo sương mù ( &#870; C)</li>  
   <li>Solar radiation: bức xạ năng lượng mặt trời (MJ/m&#178;	)</li>  
   <li>Rainfall: lượng mưa trong ngày (mm)</li>  
   <li>Snowfall: lượng tuyết rơi trong ngày (cm)</li>  
   <li>Seasons: mùa (Winter, Spring, Summer, Autumn)</li>  
   <li>Holiday: ngày nghỉ hoặc không (Holiday/ No holiday)</li>  
   <li>Functional Day: ngày làm NoFunc(Non Functional Hours), Fun(Functional hours)</li>
 </ul>  

# Các mục tiêu phân tích cần đạt được
<ul>
  <li>
    Xây dựng mô hình dự đoán số lượng xe đạp được thuê trong ngày dựa trên thông
    tin của một ngày (thời tiết, tính chất ngày nghỉ/làm việc), đưa ra mô hình
    khác nhau, tìm ra mô hình tốt nhất.
  </li>
  <li>
    Sử dụng mô hình tốt nhất, thu được trong phần trên, hãy dự đoán số lượng
    thuê xe trong ngày ở Seoul. So sánh với thực tế
  </li>
</ul>

# Các phương pháp phân tích và chiến lược cho mỗi mục tiêu đề ra
<ul>
  <li>
    Trước mắt sẽ tập trung xây dựng mô hình hồi quy Poisson, nếu mô hình không
    phù hợp thì sẽ chuyển sang lựa chọn khác thay thế (mô hình Quasi-Poisson)
  </li>
  <li>
    Thực hiện dự đoán lượng xe được thuê trong một ngày từ dữ liệu đã cho và so
    sánh giá trị dự đoán với dữ liệu.
  </li>
</ul>
