# excel_w
对excel_BOM表 分四个层级：1.包装2.组装，3插件 4贴纸，根据不同需求不同逻辑 修改excel单元格数据

'''*
0821
根据的新需求实现BOM物料表自动化操作单元格：
需求：操作表sheet2，自动完成单元格修改需求，sheet1为原表，sheet2为操作需求表，（需求表逐行从第二行按顺序执行，第一行是标题），new sheet是新表

逻辑细节：级别满足1234，sheet2物料表编码和sheet1（原表）一致，判断操作是否为ADD、DEL，分别执行ADD或DEL操作，.ADD：1转字符串2.split切割3.循环判断，not append,4join拼接；5.len读位号个数，.DEL：1转字符串2.split切割3.循环判断，4join拼接；5.len读位号个数，not move,4join拼接

实现版本：打包成EXE，和excel在同级目录下，将EXE拖到同级目录下的终端 ，回车执行
'''

*
0822
excel_BOM[update]
1.运行提示输出到excel{温馨提示}sheet；更改表名：sheet1-->原表；sheet2-->操作提示表；sheet3-->新bom表；
2openyxl官方文档和环境配置
3..每次运行不新增一个新表单，表单存在就覆盖，不存在则新增；
