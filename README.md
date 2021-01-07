# hoctangcuong
Câu 1: 
 Hàm init  duyệt các giá trị của range(iterations), ta xét từng giá trị của từng state, mỗi state ta lại xét từng trạng thái nếu trạng thái là đích thì ta sẽ thoái ra và không có phần thưởng, còn nếu đây không phải đích thì ta sẽ tìm tổng phần thưởng đợi lớn nhất của các hành động khác nhau.

Với computeQValueFromValues, ta có một hàm ở đây để có thể tính toán trạng thái chuyển đổi và xác suất là getTransitionStatesAndProbs(state, action). Đối với mỗi lần chuyển đổi được tính bằng tổng phần thưởng của việc chuyển đổi và trạng thái chuyển tiếp sau đó. Và chính giá trị này cung cấp cho q-value một cặp hành động và trạng thái (action,state) mà từ đó ta có thể tính được giá trị cần tìm.

Với computeActionFromValues, ta đơn giản là chỉ khai báo một bộ đém stateAction để lưu q-value. Với mỗi cặp (Action,state) thì policy hoặc action chính là cho ta biết được tổng phần thưởng mong đợi tốt nhất.
 Câu 4: 
 Ta lấy tât các trạng thái của hành động bằng hàm getLegalActions() với và khởi tạo giá trị bằng 0 còn với các trạng thái khác thì trả về giá trị tối đa của q-value trạng thái.
 Câu 5: 
 Với việc chọn ngẫu nhiên một action epsilon chỉ khi đánh giá được self.epsilon còn không sẽ trả về giá trị hành động của hàm computeActionFromQValues
 Câu 6:
 Ta chọn các giá trị : answerEpsilon = 0.1 answerLearningRate = 0.8 Vì không thể tìm được con đường tối ưu đến 99%, 50 tập là quá nhỏ nên cần thêm để tìm kiếm
