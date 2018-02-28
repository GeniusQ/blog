### job不支持Autowired注入的处理方法
  使用 BeanFactory factory = new ClassPathXmlApplicationContext("classpath:/applicationContext*.xml"); 手工注入对象
  
### tomcat关闭时无法杀掉quartz线程的处理
  - 添加一个ServletContextListener的实现，在contextDestroyed中拿到Scheduler对象，调用shutdown
  - 在web.xml中加入ServletContextListener的实现
