## **Thông tin từ bài báo này**: 
- **Tên bài báo:** _An Elementary Proof of Dodgson's Condensation Method for Calculating Determinants_
- **Tác giả:** Mitch Main, Micah Donor, và R. Corban Harwood
- **Năm xuất bản:** 2016 (Được nộp lên hệ thống vào ngày 18 tháng 7 năm 2016)
- **Nguồn:** Kho lưu trữ tài liệu khoa học trực tuyến **arXiv** (Mã định danh: `arXiv:1607.05352`, thuộc lĩnh vực Toán học - Lịch sử và Tổng quan / `math.HO`)
- **DOI:** [https://doi.org/10.48550/arXiv.1607.05352](https://doi.org/10.48550/arXiv.1607.05352)

## **Tóm tắt bài báo**: 
+ Trình bày cách tính (thuật toán) (how), chứng minh (why), và ví dụ về cách tính định thức của Lewis Carroll hay đươc gọi là phương pháp ngưng tụ Dodgson (Dodgson condensation). 
+ Ý tưởng mà Lewis Carroll sử dụng cho phương pháp tính định thức của mình dựa trên định lý Jacobi (Jacobi’s Theorem). 
+ Vấn đề lớn nhất của phương pháp này nằm ở chỗ các số 0 xuất hiện bên trong ma trận. Câu hỏi là vì sao số 0 xuất hiện trong ma trận lại là vấn đề lớn nhất trong pp tính định thức này của Lewis Carroll ? Chúng ta sẽ khắc phục những vấn đề như thế nào ? 

## **Câu hỏi thêm của mình với bài báo này**:
+ Nên sử dụng pp tính định thức này của Carroll khi nào (when) ? 
+ Dấu hiệu nhận biết số 0 (?) làm ảnh hưởng đến pp của Carroll ? 
+ So sánh độ hiểu quả của phương pháp của Carroll với các phương pháp tính định thức khác ? (dựa vào đâu mà ta so sánh ?) 

## Phân tích phần toán học 

###  Như thế nào ? 

Qua một ví dụ sau đây:  

Cho một ma trận $A$ thực vuông cấp 4 sau:

$$
A = \begin{bmatrix}
    4 & 2 & 0 & -3 \\
    1 & 1 & 2 & 2 \\ 
    0 & -1 & 3 & -1 \\
    1 & 2 & 5 & 1
\end{bmatrix}
$$
Tiếp đến ta nhóm các ma trận $2 \times 2$ , lúc này ma trận vuông cấp 4 sẽ trở thành ma trận vuông cấp 3: 
$$
\begin{bmatrix}
    \begin{vmatrix}
        4 & 2 \\
        1 & 1 
    \end{vmatrix} & \begin{vmatrix}
        2 & 0 \\
        1 & 2 
    \end{vmatrix} & 
    \begin{vmatrix}
        0 & -3 \\
        2 & 2 
    \end{vmatrix} \\
    
    \begin{vmatrix}
        1 & 1 \\
        0 & -1 
    \end{vmatrix} & 
    
    \begin{vmatrix}
        1 & 2 \\
        -1 & 3 
    \end{vmatrix} & 
    \begin{vmatrix}
        2 & 2 \\ 
        3 & -1
    \end{vmatrix} \\
    \begin{vmatrix}
        0 & -1 \\ 
        1 & 2
    \end{vmatrix} & 
    \begin{vmatrix}
        -1 & 3 \\
        2 & 5
    \end{vmatrix} & 
    \begin{vmatrix}
        3 & -1 \\
        5 & 1
    \end{vmatrix}
\end{bmatrix}

= \begin{bmatrix}
    2 & 4 & 6  \\
    -1 & 5 & -8  \\ 
   1 & -11 & 8 \\
\end{bmatrix}


$$

Tương tự như vậy, lúc này ma trận vuông cấp 3 sẽ trở thành ma trận vuông cấp 2:
$$
\begin{bmatrix}
    \begin{vmatrix}
        2 & 4 \\
        -1 & 5 
    \end{vmatrix} & \begin{vmatrix}
        4 & 6 \\
        5 & -8 
    \end{vmatrix} \\
    
    \begin{vmatrix}
        -1 & 5 \\
        1 & -11 
    \end{vmatrix} & 
    \begin{vmatrix}
        5 & -8 \\
        -11 & 8 
    \end{vmatrix}
\end{bmatrix} 

= \begin{bmatrix}
    14 & -62  \\
    6 & -48 \\ 
\end{bmatrix}


$$
Các phần tử trung tâm (?) của ma trận $A$ ta đặt $A'$ lúc này có là: 
$$
A' = \begin{bmatrix}
    1 & 2  \\
   -1 & 3 \\ 
\end{bmatrix}
$$
. . . (chưa biết viết sao)

$$
\begin{bmatrix}
    \frac{14}{1} & \frac{-62}{2}  \\
   \frac{6}{-1} & \frac{-48}{3} \\ 
\end{bmatrix} 

= 

\begin{bmatrix}
    14 & -31  \\
   -6 & -16 \\ 
\end{bmatrix}
$$
Phần tử trung tâm (?) của ma trận  $\begin{bmatrix} 2 & 4 & 6  \\    -1 & 5 & -8  \\ 1 & -11 & 8 \\\end{bmatrix}$ là bằng 5. 

Định thức của ma trận $A$ lúc là: 

$$
det(A) = \frac{14 \cdot (-16) - (-31) \cdot (-6)}{5} = -82
$$

### Vì sao ? 