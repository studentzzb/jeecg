JEECG 智能开发平台
===============
简介
-----------------------------------
    JEECG（J2EE Code Generation）是一款基于代码生成器的智能开发平台。引领新的开发模式(Online Coding模式->代码生成器模式->手工MERGE智能开发)，
    可以帮助解决Java项目60%的重复工作，让开发更多关注业务逻辑。既能快速提高开发效率，帮助公司节省人力成本，同时又不失灵活性。 
    
    JEECG宗旨是: 简单功能由代Online Coding配置出功能;复杂功能由代码生成器生成进行手工Merge; 复杂流程业务采用表单自定义，
    业务流程使用工作流来实现、扩展出任务接口，供开发编写业务逻辑。实现了流程任务节点和任务接口的灵活配置，既保证了公司流程的保密行，又减少了开发人员的工作量。

架构说明
-----------------------------------
* 	JEECG V3.0版本采用SpringMVC+Hibernate+UI快速开发库+Spring jdbc+ freemarker+ Highcharts+ bootstrap+Ehcache 的基础架构</br>
* 	采用面向声明的开发模式， 基于泛型编写极少代码即可实现复杂的数据展示、数据编辑、
表单处理等功能，再配合Online Coding在线开发与代码生成器的使用,将J2EE的开发效率提高6倍以上，可以将代码减少80%以上。</br>

* 	JEECG V3.0版本六大技术点: 1.Online Coding (通过在线配置实现一个表模型的增删改查功能，无需一行代码，支持用户自定义表单布局)2.代码生成器 3.UI快速开发库 4.在线流程设计 5.系统日志记录 6.Web GIS支持 7.移动平台支持Bootstrap(兼容Html5) 8.动态报表9.查询过滤器</br>

* 	<b>技术点一：</b>Online Coding开发模式（通过配置实现单表模型和一对多数据模型的增删改查功能,No 代码） </br>
* 	<b>技术点二：</b>代码生成器，支持多种数据模型,根据表生成对应的Entity,Service,Dao,Action,JSP等,增删改查功能生成直接使用</br>
* 	<b>技术点三：</b>UI快速开发库，针对WEB UI进行标准封装，页面统一采用UI标签实现功能：数据datagrid,表单校验,Popup,Tab等，实现JSP页面零JS，开发维护非常高效</br>
* 	<b>技术点四：</b>在线流程定义，采用开源Activiti流程引擎，实现在线画流程,自定义表单,表单挂接,业务流转，流程监控，流程跟踪，流程委托等</br>
* 	<b>技术点五：</b>系统日志记录 (详细记录操作日志)</br>
* 	<b>技术点六：</b>Web GIS支持 （基础技术GIS的支持）</br>
* 	
* 	<b>技术点七：</b>移动平台支持，对Bootstrap(兼容Html5)进行标准封装 </br>
* 	<b>技术点八：</b>动态报表功能（用户输入一个sql，系统自动解析生成报表）</br>
	
* 	JEECG V3.0,经过了专业压力测试,性能测试，保证后台数据的准确性和页面访问速度</br>
* 	支持多种浏览器: IE, 火狐, Google 等</br>
* 	支持数据库: Mysql,Oracle10g,Postgre,SqlServer等</br>
* 	基础权限: 用户，角色，菜单权限，按钮权限，数据权限</br>
* 	智能报表集成: 简易的图像报表工具和Excel导入导出</br>
* 	Web容器测试通过的有Jetty和Tomcat6,Weblogic</br>
* 	即将推出功能：分布式部署，云平台，移动平台开发，规则引擎</br>
* 	要求JDK1.6+</br>


系统演示
-----------------------------------
![github](http://www.jeecg.org/data/attachment/forum/201303/02/123311mf9fa22tv69b228f.jpg "jeecg")
![github](http://www.jeecg.org/data/attachment/forum/201303/02/123412x003euegeg7nb68z.jpg "jeecg")
![github](http://www.jeecg.org/data/attachment/forum/201303/02/124748gyhrgvr45vshyc82.jpg "jeecg")
![github](http://www.jeecg.org/data/attachment/forum/201303/02/123428ubcjjnuwjbkjrnrw.jpg "jeecg")
![github](http://www.jeecg.org/data/attachment/forum/201303/02/124749up2j5id7gj9kppp8.jpg "jeecg")


代码示例
-----------------------------------
    这是一个有多行的文本框  
    <%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
    <%@include file="/context/mytags.jsp"%>
    <div class="easyui-layout" fit="true">
    <div region="center" style="padding:1px;">
    <t:dategrid name="jeecgDemoList" title="开发DEMO列表" actionUrl="jeecgDemoController.do?datagrid" idField="id" fit="true">
    <t:dgCol title="编号" field="id" hidden="false"></t:dgCol>
    <t:dgCol title="用户名" field="userName" query="true"></t:dgCol>
    <t:dgCol title="电话号码" sortable="false" field="mobilePhone" width="20" query="true"></t:dgCol>
    <t:dgCol title="办公电话" field="officePhone"></t:dgCol>
    <t:dgCol title="邮箱" field="email"></t:dgCol>
    <t:dgCol title="年龄" sortable="true" field="age"></t:dgCol>
    <t:dgCol title="工资"  field="sex"></t:dgCol>
    <t:dgCol title="性别"  field="salary"></t:dgCol>
    <t:dgCol title="生日" field="birthday" formatter="yyyy/MM/dd"></t:dgCol>
    <t:dgCol title="创建日期" field="createTime" formatter="yyyy-MM-dd hh:mm:ss"></t:dgCol>
    <t:dgCol title="操作" field="opt" width="100"></t:dgCol>
    <t:dgFunOpt funname="szqm(id)" title="审核" />
    <t:dgDelOpt title="删除" url="jeecgDemoController.do?del&id={id}" />
    <t:dgToolBar title="录入" icon="icon-add"></t:dgToolBar>
    <t:dgToolBar title="编辑" icon="icon-edit"></t:dgToolBar>
    </t:dategrid>
    </div>
    </div>
    
    
技术交流
-----------------------------------
* 	作者：张代浩</br>
* 	邮箱：zhangdaiscott@163.com
* 	论坛：[www.jeecg.org](http://www.jeecg.org)
* 	交流群:106259349, 106838471, 289782002</br>
* 	在线演示: [JEECG演示DEMO](http://demo.jeecg.org:8080/)
