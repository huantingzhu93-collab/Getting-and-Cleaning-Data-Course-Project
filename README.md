# Getting and Cleaning Data Course Project

本项目是 Coursera《Getting and Cleaning Data》课程的 Peer-graded Assignment。

## 项目目标
清洗 UCI HAR（Human Activity Recognition Using Smartphones）数据集，生成可用于分析的 tidy data set。

## 文件说明

- `run_analysis.R`：主分析脚本，完成数据合并、提取、重命名和汇总
- `CodeBook.md`：详细说明数据处理过程和变量含义
- `FinalData.txt`：最终生成的 tidy data set（运行脚本后产生）
- `README.md`：本说明文件

## 如何运行

1. 下载原始数据：  
   https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  
   解压后得到 `UCI HAR Dataset` 文件夹。

2. 将 `UCI HAR Dataset` 文件夹与 `run_analysis.R` 放在同一目录下。

3. 在 R 中运行：
   ```r
   source("run_analysis.R")
