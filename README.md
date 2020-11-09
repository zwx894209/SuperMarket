<html lang="zh">
<body>
<h1>网上商城</h1>
<h2>截图展示</h2>
<img src="./img/index.png" alt="首页" /><br />
<img src="./img/product.png" alt="商品页面" /><br />
<img src="./img/regist.png" alt="注册页面" /><br />
<img src="./img/login.png" alt="登录页面" /><br />
<img src="./img/logout.PNG" alt="注销页面" /><br />
<img src="./img/error.png" alt="错误页面" /><br />
<h2>声明</h2>
<ul>
    <li>本项目静态资源由网络收集得来，并加以大范围修改</li>
    <li>未经许可不得将本项目商用，如需商用请联系作者<a href="mailto:zxr@tju.edu.cn">zxr@tju.edu.cn</a></li>
</ul>
<h2>关键技术</h2>
<p>基于SSM框架开发的商城系统，代码严格遵循MVC分层思想，可部署到服务器上，设计精良，不断完善</p>
<h3>前端</h3>
<ul>
    <li>前端对应View层</li>
    <li>前端使用jsp页面展示，并通过EL表达式接收服务器打给浏览器的数据</li>
    <li>使用js实现网页动态效果，通过jQuery简化操作，并配合html5实现前端的数据校验</li>
    <li>使用Ajax技术完成前端用户名可用性校验、退出登录功能</li>
</ul>
<h3>过滤器</h3>
<ul>
    <li>com.supermarket.filter包用于存放过滤器</li>
    <li>CharacterEncodingFilter类实现全局乱码处理，包括POST请求、GET请求、响应</li>
    <li>AutoLogin类实现用户自动登录功能</li>
</ul>
<h3>Controller层</h3>
<ul>
    <li>com.supermarket.web包对应Controller层，通过SpringMVC实现</li>
    <li>UserController类实现用户登录、注销、注册、检查用户名等功能</li>
    <li>com.supermarket.interceptor包为SpringMVC拦截器，通过Logging类实现用户请求信息的日志记录</li>
</ul>
<h3>Service层</h3>
<ul>
    <li>com.supermarket.service包属于Model层</li>
    <li>使用com.supermarket.service.UserService实现登录、注册、检查可用性等功能</li>
    <li>使用com.supermarket.service.ValistrService完成验证码生成和比对相关功能</li>
    <li>com.supermarket.aspect存放切面类，其中Logging实现异常日志记录、执行时间统计等功能</li>
</ul>
<h3>DAO层</h3>
<ul>
    <li>com.supermarket.dao包属于Model层，通过MyBatis实现</li>
    <li>UserDao为接口，配合UserMapper使用</li>
    <li>com.supermarket.mapper为MyBatis的mapper文件存放位置，配合UserDao实现对用户的增删改查</li>
</ul>
<h2>版本迭代</h2>
<table>
    <tr>
        <th>版本号</th>
        <th>更新内容</th>
        <th>上传时间</th>
    </tr>
    <tr>
        <td>0.1</td>
        <td>
            <ul>
                <li>初步完成项目方案确定</li>
                <li>完成主页及注册页面的静态资源编写(包括js,css)</li>
                <li>完成主页及注册页面的动态资源编写(包括jsp,servlet)</li>
                <li>通过jdbc链接MySQL数据库</li>
                <li>使用c3p0连接池</li>
            </ul>
        </td>
        <td>2020年8月3日</td>
    </tr>
    <tr>
        <td>0.1.1</td>
        <td>
            <ul>
                <li>可以选择使用哪个连接池，并且在web.xml中指定，现在可以使用DBCP连接池</li>
                <li>通过反射机制设置如果指定连接池调用失败，再调用哪个连接池</li>
                <li>使用Ajax技术完成前端用户名校验</li>
                <li>更改img标签的src属性，使浏览器异步发送GET请求，刷新验证码</li>
            </ul>
        </td>
        <td>2020年8月7日</td>
    </tr>
    <tr>
        <td>0.1.2</td>
        <td>
            <ul>
                <li>使用JDBC.properties进行全局JDBC配置</li>
                <li>去掉JDBC的反射调用</li>
                <li>使用cookie完成记住用户名功能</li>
                <li>新增登录功能：使用session完成会话级别的数据传递</li>
                <li>新增注销功能：通过ajax请求销毁session</li>
                <li>修改静态页面，使其实现对logo.png的单独依赖</li>
            </ul>
        </td>
        <td>2020年8月9日</td>
    </tr>
    <tr>
        <td>0.2</td>
        <td>
            <ul>
                <li>使用EL表达式替换jsp页面中的脚本表达式</li>
                <li>修改静态资源，主页增加右下角浮动项以及向上返回功能</li>
                <li>新增错误页面提示</li>
                <li>重构为JavaEE三层经典架构</li>
            </ul>
        </td>
        <td>2020年8月20日</td>
    </tr>
    <tr>
        <td>0.2.1</td>
        <td>
            <ul>
                <li>使用过滤器完成全局请求参数拦截处理，包括全局中文乱码处理、全局password请求参数加密</li>
                <li>通过过滤器实现全局连接池选定</li>
                <li>通过过滤器实现自动登录功能</li>
                <li>通过装饰者模式扩展request对象</li>
            </ul>
        </td>
        <td>2020年8月22日</td>
    </tr>
    <tr>
        <td>0.2.2</td>
        <td>
            <ul>
                <li>使用log4j框架进行日志记录</li>
                <li>修复重启服务器自动登录失效的bug</li>
                <li>加入网页标题图标</li>
            </ul>
        </td>
        <td>2020年8月24日</td>
    </tr>
    <tr>
        <td>0.2.3</td>
        <td>
            <ul>
                <li>将JDBC初始化功能交由监听器实现，并移除对应的过滤器</li>
                <li>使用过滤器实现JDBC反注册，避免内存泄漏</li>
                <li>使用注解替代web.xml完成servlet和监听器的注册</li>
                <li>重写前端校验，对于支持html5的浏览器使用其自带校验</li>
            </ul>
        </td>
        <td>2020年8月25日</td>
    </tr>
    <tr>
        <td>0.3</td>
        <td>
            <ul>
                <li>使用Spring、SpringMVC、MyBatis重构该web应用</li>
                <li>使用User类的装饰者模式完成密码的md5加密功能</li>
                <li>使用SpringMVC拦截器记录用户的访问请求</li>
                <li>使用切面记录错误日志，并统计响应时间</li>
                <li>升级log4j为log4j2</li>
                <li>使用html5及jQuery相结合的方式进行前端表单校验</li>
            </ul>
        </td>
        <td>2020年9月25日</td>
    </tr>
    <tr>
        <td>0.3.1</td>
        <td>
            <ul>
                <li>新增UserDao的SpringJDBC模板类实现</li>
                <li>注册用户功能开启事务，修复多个用户同时注册时可能造成用户名重复的bug</li>
            </ul>
        </td>
        <td>2020年9月29日</td>
    </tr>
    <tr>
        <td>0.3.2</td>
        <td>
            <ul>
                <li>新增备选的DBCP连接池配置</li>
            </ul>
        </td>
        <td>2020年10月1日</td>
    </tr>
    <tr>
        <td>0.4</td>
        <td>
            <ul>
                <li>使用Maven重构依赖</li>
                <li>使用SpringCloud重构项目</li>
                <li>重构数据库</li>
                <li>增加common微服务: 存放共享资源(如JavaBean, 工具类, ViewObject)</li>
                <li>增加商品微服务：新增、修改、查询功能</li>
                <li>增加用户微服务：用户名校验、注册</li>
                <li>增加图片微服务：图片上传</li>
                <li>增加nginx：负载均衡、动态静态资源分离</li>
            </ul>
        </td>
        <td>2020年11月10日</td>
    </tr>
</table>
<h2>配置情况</h2>
<ul>
    <li>JDK版本：OpenJDK11</li>
    <li>nginx：1.19.1</li>
    <li>maven: 3.6.3</li>
    <li>MySql: 5.5.27</li>
    <li>开发环境：IntelliJ Idea 2020.1.4</li>
    <li>框架：Springboot 2.2.5.RELEASE, SpringCloud Hoxton.SR3</li>
    <li>hosts配置: 127.0.0.1 www.supermarket.com</li>
</ul>
<h2>遇到的bug锦集(作为记录，博君一笑)</h2>
<ul>
    <li>HttpServletRequest的装饰者类HttpServletRequestDecorator中的getParameterMap重写方法中，不能在原地进行参数字符集修改，否则如果调用两次及以上该方法时会编码多次，造成乱码</li>
    <li>对请求参数的拦截处理，如果用到装饰者模式，最好在一处完成。如果在多处完成会造成请求参数的重复处理，从而导致乱码或者拿到非预期的参数值</li>
    <li>用户的登录信息最好保存到session域中，在0.2.1中的自动登录成功后误把user对象塞入到了request域，造成了重启服务器自动登录失效的bug。</li>
    <li>使用过滤器将密码加密，不仅要将参数为password的值加密，还要将参数为password2的值加密，否则永远确认密码不一致</li>
    <li>使用SpringMVC处理请求参数，如果自动封bean作为方法参数传入，那么该bean所携带的请求参数是不经过过滤器的！原因未知</li>
    <li>自动登录最好使用过滤器实现，因为SpringMVC拦截器无法拦截index.jsp。而因为使用过滤器的时候Spring容器还未初始化，所以过滤器的属性需要手工注入</li>
    <li>即便上一次响应设置了cookie的path，下一次请求携带的cookie的path也会是null。因此如果要修改或删除cookie，一定要严格满足name, path都设置，否则可能会无效</li>
    <li>如果间接依赖了spring-cloud-starter-netflix-eureka-server，一定要把jackson-dataformat-xml排除掉，因为如果不排除掉会导致返回给浏览器的对象是xml格式而非json格式</li>
    <li>MyBatis如果使用bean传参，不要使用&lt;if&gt;标签内的test属性名应该对应bean属性名而非表的列名。否则会报There is no getter for property named 'xx' in 'class xxx</li>
    <li>在Springboot项目中，如果要在application.properties中写自定义配置项，若该配置项为路径字符串，一定要写全路径，从盘符写起，否则会自动在前面拼接tomcat的临时路径</li>
</ul>
</body>
</html>
