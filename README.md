# hoctangcuong
Câu 1: 

Hàm init duyệt các phần tử giá trị của range(iteration)
mỗi state , xét từng trạng thái của nó. nếu là đích thì sẽ thoát ra và phần thưởng không có;
Nếu không phải địch thì tính tổng phần thưởng mong đợi.

 q-value  cần 1 cặp action state chúng ta có thể tính toán nên đi action nào bằng các hàm computeQValueFromValues để tính toán trạng thái chuyển đồi, và getTransitionStatesAndProbs(state, action) tính xác suất. bằng 2 hàm này ta tính được tổng phần thưởng mong đợi đối với action sau đó.

 Câu 4: 

 Lấy trạng thái của hành động bằng getLegalActions(), khởi tạo bằng 0 hoặc trả về giá trị tối đa của trạng thái q-value.
 
 Câu 5: 
 Với việc chọn ngẫu nhiên một action epsilon chỉ khi đánh giá được self.epsilon còn không sẽ trả về giá trị hành động của hàm computeActionFromQValues
 Câu 6:
 Ta chọn các giá trị : answerEpsilon = 0.1 answerLearningRate = 0.8 Vì không thể tìm được con đường tối ưu đến 99%, 50 tập là quá nhỏ nên cần thêm để tìm kiếm
