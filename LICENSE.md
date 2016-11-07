#計算測站 C0M530 (奮起湖站) 從 2006到2015 年的十年的每日平均氣溫、每日最低溫的平均、每日最高溫的平均、每月平均氣溫、平均每月累積降水
#計算最暖月的每日最高溫平均
#計算最冷月的每日最低溫平均
getwd()
setwd("D:/sourcetree/生態資訊學/聚合作業/raw")
getwd()
library(data.table)
rawdata200601 <- fread("D:\\sourcetree\\生態資訊學\\聚合作業\\raw\\200601_auto_hr.txt",skip = 74,head = TRUE)
rawdata200601
rawdata200602 <- fread("D:\\sourcetree\\生態資訊學\\聚合作業\\raw\\200602_auto_hr.txt",skip = 74,head = TRUE)
rawdata200603 <- fread("D:\\sourcetree\\生態資訊學\\聚合作業\\raw\\200603_auto_hr.txt",skip = 74,head = TRUE)
rawdata200604 <- fread("D:\\sourcetree\\生態資訊學\\聚合作業\\raw\\200604_auto_hr.txt",skip = 74,head = TRUE)
rawdata200605 <- fread("D:\\sourcetree\\生態資訊學\\聚合作業\\raw\\200605_auto_hr.txt",skip = 74,head = TRUE)
list.files()
txtpath = "D:/sourcetree/生態資訊學/聚合作業/raw/"
txtfilesn = list.files()
txtfilesn
gointo = function(rtxt){
  fread(rtxt,skip = 74,stringsAsFactors = FALSE)
}
something = lapply(paste(txtpath,txtfilesn,sep =" "),gointo)
txtfilesn
data1 = something[[1]]
#未完成
