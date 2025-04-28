# 电商数据探索性分析与预处理作业
## 1、数据集
原始数据以Parquet格式存储，包含id、last_login、user_name、fullname、email、age、income、gender、country、address、purchase_history、is_active、registration_date、phone_number、
login_history 等字段
## 2、解决方案
### 2.1 数据预处理
采用了基于SQL的查询方式从Parquet文件中提取关键特征。数据预处理阶段主要包括从JSON格式的purchase_history中提取avg_price、item_count 等关键信息，计算days_since_last_purchase 时间差值，
以及创建income_spend_ratio 等衍生特征。同时过滤了与消费行为分析无关的字段，如user_name、email、phone_number 等，保留了 age、income、purchase_history 等核心特征。
### 2.2 探索性分析
主要进行了各年龄段平均商品价格分析、用户年龄分布与购买价格分布分析、特征相关性分析、聚类特征对比等

