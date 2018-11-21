# odoo-reportbro
odoo集成reportbro实现单据套打、批量打印、条码及图片打印等
# 11.0

安装：1、下载后修改模块名称为inspur_print；2、初始数据中account_china改为account；
# 服务端：
1、虚拟机Ubuntu16.04.4

2、sftp上传文件状态错误（权限）：sudo chmod 777 reportbro/

3、sudo apt install python-pip

4、$ pip install reportbro-lib

5、$ pip install SQLAlchemy tornado

6、$ python reportbro_server.py

这样测试服务是没啥问题，但是还需要处理中文问题！

显示已安装模块：pydoc modules

安装成功！！！一直出问题原因是因为安装的reportbro-lib版本问题！！！

Postman服务测试文件：

{
"report":{
"docElements": [{"borderColor": "#000000", "borderTop": false, "cs_borderColor": "#000000", "cs_fontSize": 12, "elementType": "text", "x": 210, "cs_borderTop": false, "cs_paddingBottom": 2, "height": 20, "cs_paddingLeft": 2, "paddingTop": 2, "alwaysPrintOnSamePage": true, "paddingBottom": 2, "borderLeft": false, "paddingRight": 2, "cs_paddingRight": 2, "cs_bold": false, "cs_condition": "", "cs_underline": false, "cs_borderLeft": false, "cs_verticalAlignment": "top", "cs_horizontalAlignment": "left", "printIf": "", "pattern": "", "italic": false, "cs_borderRight": false, "cs_borderAll": false, "eval": false, "borderWidth": 1, "cs_paddingTop": 2, "cs_lineSpacing": 1, "spreadsheet_addEmptyRow": false, "paddingLeft": 2, "borderAll": false, "width": 100, "cs_font": "helvetica", "backgroundColor": "", "underline": false, "fontSize": 12, "id": 230, "cs_borderBottom": false, "spreadsheet_column": "", "cs_italic": false, "bold": false, "borderBottom": false, "lineSpacing": 1, "cs_borderWidth": "1", "font": "firefly", "containerId": "0_content", "content": "\u4e2d\u6587\u4e2d\u6587\u4e2d\u6587", "cs_styleId": "", "styleId": "", "cs_textColor": "#000000", "verticalAlignment": "top", "horizontalAlignment": "left", "spreadsheet_hide": false, "cs_backgroundColor": "", "textColor": "#000000", "y": 50, "borderRight": false, "removeEmptyElement": false
}], 
"styles": [], 
"parameters": [], 
"version": 2,
"documentProperties":{"contentHeight": "", "footer": true, "unit": "mm", "pageWidth": "", "marginTop": "20", "headerSize": "60", "patternLocale": "de", "header": true, "footerSize": "60", "footerDisplay": "always", "orientation": "portrait", "marginBottom": "10", "headerDisplay": "always", "marginLeft": "20", "pageHeight": "", "pageFormat": "A4", "marginRight": "20", "patternCurrencySymbol": 1}
},
"outputFormat": "pdf",
"data":{},
"isTestData": false
}

![image](https://github.com/inspurodoo/odoo-reportbro/blob/master/static/description/design.png)
![image](https://github.com/inspurodoo/odoo-reportbro/blob/master/static/description/preview.png)

# 服务端代码
reportbro_server.py

# 中文字体文件
fireflysung.ttf

