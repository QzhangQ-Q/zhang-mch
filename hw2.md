(1)PERT/CPM 圖

## PERT 圖

```mermaid
graph TD;
    A1["研擬計畫 (1天)"] --> A2["任務分配 (4天)"];
    A1 --> A3["取得硬體 (17天)"];
    
    A2 --> A4["程式開發 (70天)"];
    A3 --> A5["安裝硬體 (10天)"];
    
    A4 --> A6["程式測試 (30天)"];
    A5 --> A7["撰寫使用手冊 (25天)"];
    A5 --> A8["轉換檔案 (20天)"];
    
    A6 --> A9["系統測試 (25天)"];
    A7 --> A10["使用者訓練 (20天)"];
    A8 --> A10;
    
    A9 --> A11["使用者測試 (25天)"];
    A10 --> A11;
```
![image](https://github.com/user-attachments/assets/f894572a-1e4e-4e87-b7aa-db2c3f331f43)



(2)甘特圖
```mermaid
gantt
    title A Gantt Diagram

    section Section
    研擬計畫           :a1, 2024-01-01, 1d
    任務分配     :a2,after a1  , 4d
    取得硬體      :a3,after a1  , 17d
    程式開發      : a4,after a2,70d
    安裝硬體      : a5,after a3,10d
    程式測試      : a6,after a4,30d
    撰寫使用手冊      : a7,after a5,25d
    轉換檔案      : a8,after a5,20d
    系統測試      : a9,after a6,25d
    使用者訓練      : a10,after a7 a8,20d
    使用者測試      : after a9 a10,25d
```
![image](https://github.com/user-attachments/assets/fe8b3d19-0657-4a9e-9420-dcb8c8674008)


### 專案關鍵路徑

1. **研擬計畫** (1 天)
2. **任務分配** (4 天)
3. **程式開發** (70 天)
4. **程式測試** (30 天)
5. **系統測試** (25 天)
6. **使用者測試** (25 天)

**總工期：155 天**

```graphviz
   digraph {
    node[shape=record];
    rankdir="LR";

    no1 [label = "研擬計畫 | 編號:1 | 開始:第1天 | 結束:第1天 | 需時:1天"]
    no2 [label = "任務分配 | 編號:2 | 開始:第2天 | 結束:第5天 | 需時:4天"]
    no3 [label = "取得硬體 | 編號:3 | 開始:第2天 | 結束:第18天 | 需時:17天"]
    
    no1 -> no2
    no1 -> no3

    no4 [label = "程式開發 | 編號:4 | 開始:第6天 | 結束:第75天 | 需時:70天"]
    no5 [label = "安裝軟體 | 編號:5 | 開始:第19天 | 結束:第28天 | 需時:10天"]
    
    no2 -> no4
    no3 -> no5

    no6 [label = "程式測試 | 編號:6 | 開始:第76天 | 結束:第105天 | 需時:30天"]
    no7 [label = "撰寫使用手冊 | 編號:7 | 開始:第29天 | 結束:第53天 | 需時:25天"]
    no8 [label = "轉換檔案 | 編號:8 | 開始:第29天 | 結束:第48天 | 需時:20天"]

    no4 -> no6
    no5 -> no7
    no5 -> no8

    no9 [label = "系統測試 | 編號:9 | 開始:第106天 | 結束:第130天 | 需時:25天"]
    no10 [label = "使用者訓練 | 編號:10 | 開始:第54天 | 結束:第73天 | 需時:20天"]
    
    no6 -> no9
    no7 -> no10

    no11 [label = "使用者測試 | 編號:11 | 開始:第131天 | 結束:第155天 | 需時:25天"]
    no9 -> no11
}
```

![image](https://github.com/user-attachments/assets/23099623-ff98-4297-8bd0-3392ecff10fb)


![image](https://github.com/user-attachments/assets/8d493603-3036-47b2-8133-80d1bf322be3)

(1) 顯示任務及任務模式

![image](https://github.com/user-attachments/assets/f0ad785b-e3c0-468a-b124-cfa4c6fd83a4)

(2) 輸入開始及結束時間。

![image](https://github.com/user-attachments/assets/4bdbb2b0-7b1a-4f55-b54b-c0edc2f1db73)




