# Code Book - Getting and Cleaning Data Course Project

## 数据来源
原始数据来自 UCI Machine Learning Repository：  
Human Activity Recognition Using Smartphones Dataset  
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

下载地址：  
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## 数据处理步骤（run_analysis.R 执行的操作）

1. **合并训练集和测试集**  
   将 train 和 test 的 subject、X、y 数据分别合并，形成一个完整的数据集。

2. **提取均值和标准差测量**  
   只保留变量名中包含 `mean` 或 `std` 的特征列。

3. **使用描述性活动名称**  
   将活动代码（1-6）替换为：
   - WALKING
   - WALKING_UPSTAIRS
   - WALKING_DOWNSTAIRS
   - SITTING
   - STANDING
   - LAYING

4. **重命名变量为描述性名称**  
   主要替换规则：
   - `t` → `Time`
   - `f` → `Frequency`
   - `Acc` → `Accelerometer`
   - `Gyro` → `Gyroscope`
   - `Mag` → `Magnitude`
   - `mean()` → `Mean`
   - `std()` → `STD`
   - 等

5. **创建最终 tidy data set**  
   按 `subject` 和 `activity` 分组，计算每个变量的平均值。

## 最终数据集（FinalData.txt）说明

- **行数**：180 行（30 个受试者 × 6 种活动）
- **列数**：88 列
  - 第1列：`subject`（受试者编号，1-30）
  - 第2列：`activity`（活动名称）
  - 其余86列：各测量变量的平均值

## 变量说明（主要类型）

- **Time 域特征**：以 `Time` 开头
- **Frequency 域特征**：以 `Frequency` 开头
- **Accelerometer**：加速度计相关
- **Gyroscope**：陀螺仪相关
- **Mean**：均值
- **STD**：标准差
- **Magnitude**：幅值

完整变量列表可在运行脚本后通过 `names(FinalData)` 查看。
