> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

本系统分为了管理员、教练角色

球员信息管理页面，此页面提供给管理员的功能有：球员信息的查询管理，可以删除球员信息、修改球员信息、新增球员信息，

教练信息管理页面，此页面提供给管理员的功能有：查看已发布的教练信息数据，修改教练信息，教练信息作废，即可删除，还进行了对教练信息名称的模糊查询

给管理员的功能有：根据公告类型进行条件查询，还可以对公告类型进行新增、修改、查询操作等等。



# 环境要求



1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。 

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA; 

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可 

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS; 

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目 

6.数据库：MySql5.7/8.0等版本均可；





# 技术栈



运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：SpringBoot + MyBatis + Vue + Bootstrap + jQuery





# 使用说明





1.使用Navicat或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件； 

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目； 

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；





# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq 

源码地址：[http://www.codegym.top](http://www.codegym.top/)





# 运行截图

![img](https://img-blog.csdnimg.cn/img_convert/3f35fca1d895958c9a2f419dc4ce340a.png)





![springboot212球队训练信息管理系统11](https://img-blog.csdnimg.cn/img_convert/15e51d5b02a043aa77c6ef214c979b69.png)

![springboot212球队训练信息管理系统12](https://img-blog.csdnimg.cn/img_convert/307e754caab99b22ca08acc846b10fdf.png)

![springboot212球队训练信息管理系统13](https://img-blog.csdnimg.cn/img_convert/dd338ad760cc585eca7be291a16690d7.png)

![springboot212球队训练信息管理系统14](https://img-blog.csdnimg.cn/img_convert/e82980eb72eb3ea88030cd9336618922.png)
### 代码

```java
	public PageUtils queryPage(Map<String, Object> params, Wrapper<DingdanxinxiEntity> wrapper) {
		  Page<DingdanxinxiView> page =new Query<DingdanxinxiView>(params).getPage();
	        page.setRecords(baseMapper.selectListView(page,wrapper));
	    	PageUtils pageUtil = new PageUtils(page);
	    	return pageUtil;
 	}
    
```






