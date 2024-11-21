# service-pushData
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Service dùng để nạp dữ liệu và chuyển hóa dữ liệu từ dạng văn bản thành dạng vector và lưu trữ trong Pinecone Vector Store

Nền tảng công nghệ LCDP sử dụng: **N8N**

## Changelog

### v1.0
- **Node Google Drive**:  
  - Tích hợp dịch vụ Google Drive để lấy dữ liệu văn bản từ các tệp trên Google Drive.

- **Node Pinecone Vector Store**:  
  - Phân tích nội dung sau khi tải về từ Google Drive.  
  - Tạo embedding và lưu trữ tài liệu dưới dạng vector trong Pinecone.

- **Node Embedding OpenAI**:  
  - Sử dụng mô hình OpenAI để tạo embedding từ văn bản, chuyển đổi nội dung sang dạng vector mà máy tính có thể hiểu và xử lý.  

- **Node Default Data Loader**:  
  - Xử lý và nạp dữ liệu từ các tệp tải về từ Google Drive.  
  - Trích xuất và chuẩn bị văn bản để xử lý ở các bước tiếp theo.  

- **Node Recursive Character Text Splitter**:  
  - Chia nhỏ tài liệu thành các đoạn văn bản để xử lý tuần tự.  
  - Các đoạn văn bản nhỏ hơn sẽ được sử dụng để tạo embedding hiệu quả hơn.

## Hướng dẫn cài đặt
### 1. Yêu cầu hệ thống
- **Tài khoản Google API**: Để truy cập Google Drive.  
- **Tài khoản OpenAI**: Để sử dụng mô hình tạo embedding.  
- **Tài khoản Pinecone**: Để lưu trữ và truy vấn vector.
- **N8N**: Phiên bản >=1.66.0

### 2. Cài đặt dữ án
#### Bước 1: Tải mã nguồn từ bản phát hành
1. Truy cập trang phát hành chính thức tại: [Releases](https://github.com/trungthanhcva2206/service-pushData/releases).
2. Chọn phiên bản phù hợp với nhu cầu của bạn.
3. Trong phần **Assets**, tải tệp:
   - `Source code (zip)` hoặc
   - `Source code (tar.gz)`.

#### Bước 2: Giải nén và truy cập thư mục
```bash
# Giải nén file đã tải
unzip service-pushPDF.zip
cd service-pushPDF
```
#### Bước 3: Import vô N8N 
1. Tạo 1 workflow trong N8N
2. Import file PushPDF.json, file này lấy được ở trong thư mục service-pushPDF

#### Bước 4: Chỉnh sửa các tài khoản dịch vụ
Ở trong các node Google Drive, OpenAI, Pinecone sẽ có phần **Credential to connect with**, có thể chỉnh sửa các tài khoản dịch vụ của mình ở đây. 

## Tác giả
- Nguyễn Lê Trung Thành
- Trần Tuấn Anh
- Lê Văn Quang

# License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
