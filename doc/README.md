

### 1. 实现一个日志库

> 需求分析

1. 支持往不同的地方输出日志（文件、控制台）
2. 日志分级别
   - debug、trace、info、warning、error、fatal
3. 日志要支持开关控制，比如说开发的时候什么级别都能输出，但是上线之后，只有INFO级别以下的才能输出
4. 完整的日志记录要包含有时间、行号、文件名、日志级别、日志信息
5. 日志文件要切割（按照时间切割、按照大小切割）
   - 按日期切割：在结构体中设置一个字段记录上一次切割的小时数
   - 按文件大小切割：每次记录日志之前判断当前这个文件的大小


**切割效果**：

![61452205069](assets/1614522050699.png) 

> 实现代码：[src/github.com/demo_utils/mylogger](src/github.com/demo_utils/mylogger) 

