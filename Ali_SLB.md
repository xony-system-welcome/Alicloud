![image](https://user-images.githubusercontent.com/44719723/133032486-96d3a511-9d41-444d-bf42-d18d7152f901.png)
Instel:便宜
Extenl:
Server Load Balancer instances:
Listeners:PROTOCOL(http so on), halcheck
Backend Server: 接LOG

![image](https://user-images.githubusercontent.com/44719723/133032799-561ab872-66bb-4af9-8959-4fcf32a7e121.png)
Public Network: hr/$

![image](https://user-images.githubusercontent.com/44719723/133032830-ca6d3e24-aae0-47a6-bceb-a7f7427acfc5.png)
![image](https://user-images.githubusercontent.com/44719723/133032850-7f63a327-9334-4115-a741-615fdcb9b3e7.png)
![image](https://user-images.githubusercontent.com/44719723/133032871-a1702b26-5f2f-47b7-b0ad-f38d60437baa.png)
Listeners:
-Routing rules:
-Session stickiness:
-Health check configurations:
Peak banwdihk:

![image](https://user-images.githubusercontent.com/44719723/133032987-94bcb743-f2c5-4ba6-b1cc-016e09e38720.png)
Round Rbin :123 123 123 順序排；平均分配
Weighted round robin（WRR）：3部電腦 根據 round高的優先；當如果收到大量的用量時，會自動生成小型的 machine（小型的配置與大型的一樣，but）
Weighted least connections（WLC）：

![image](https://user-images.githubusercontent.com/44719723/133033528-4388f0c0-5182-4777-b3c3-ff1635d74513.png)
最高可以有50 但只能睇住一個application

![image](https://user-images.githubusercontent.com/44719723/133033603-922426f3-ccd7-40ca-bd17-b1dc9c291a32.png)
Alicloud 如果要進行全球 backend servers 的話 需要透過GTM setting

![image](https://user-images.githubusercontent.com/44719723/133033806-54a593b1-5d3f-4ecf-8f53-b1b55008f348.png)
Backend server gp

![image](https://user-images.githubusercontent.com/44719723/133033853-f42d3d6c-4699-4d17-9a61-439342b11af9.png)
Health Checks 的重要性：加入有一台電腦下線，會檢查到是否有server down（HTTP：,TCP：）

![image](https://user-images.githubusercontent.com/44719723/133034048-7df17eca-3844-40d0-bde4-4223a6b3c305.png)
Health Checks 不會無限期等待，能setting 連續34/5次 and 10/20/30S 秒數的嘗試連線，如果連線失敗就會進行 自動由 SLB server to Backend ECS。

![image](https://user-images.githubusercontent.com/44719723/133034272-99637dd6-026f-4e8c-98c0-0f3b0fc86a07.png)
SLB 可以 create 出兩個簡單的zone。IF zoneA 30s 無法鏈接 就會 pass 去zoneB，Master and Slave 並沒有任何IP（原本的IP by Node） 

![image](https://user-images.githubusercontent.com/44719723/133034524-accd2bc2-31f6-420d-b32e-bc8406b1ed44.png)
For customer 的 securety

![image](https://user-images.githubusercontent.com/44719723/133034725-2961ba0a-4287-4ef4-9725-3af5cf8fe70f.png)
可以由1部機 變10部機，可以自由選擇。

![image](https://user-images.githubusercontent.com/44719723/133034800-f3e2f7f7-59c5-46fe-a392-0e6112bc25ff.png)
Security 等級

![image](https://user-images.githubusercontent.com/44719723/133034887-da660cb3-f825-49d5-9954-89fb068ee458.png)
![image](https://user-images.githubusercontent.com/44719723/133034907-24548f4f-3e8a-4ad7-85dc-4bde5324299a.png)
Support：HTTPS HTTPS（會多了一些settting）
