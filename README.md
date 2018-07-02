# jersey-rest

**注解说明**
```
Annotation	作用	说明
@GET	查询请求	相当于数据库的查询数据操作
@POST	插入请求	相当于数据库的插入数据操作
@PUT	更新请求	相当于数据库的更新数据操作
@DELETE	删除请求	相当于数据的删除数据操作
@Path	uri路径	定义资源的访问路径，client通过这个路径访问资源。比如：@Path("user")
@Produces	指定返回MIME格式	资源按照那种数据格式返回，可取的值有：MediaType.APPLICATION_XXX。比如：@Produces(MediaType.APPLICATION_XML)
@Consumes	接受指定的MIME格式	只有符合这个参数设置的请求再能访问到这个资源。比如@Consumes("application/x-www-form-urlencoded")
@PathParam	uri路径参数	写在方法的参数中，获得请求路径参数。比如：@PathParam("username") String userName
@QueryParam	uri路径请求参数	写在方法的参数中，获得请求路径附带的参数。比如：@QueryParam("desc") String desc
@DefaultValue	设置@QueryParam参数的默认值	如果@QueryParam没有接收到值，就使用默认值。比如：@DefaultValue("description") @QueryParam("desc") String desc
@FormParam	form传递的参数	接受form传递过来的参数。比如：@FormParam("name") String userName
@BeanParam	通过Bena的形式传递参数	接受client传递的bean类型的参数，同时这个bean可以在属性上配置@FormParam用以解决client的属性名称和bean的属性名称不一致的问题。比如：@BeanParam User user
@Context	获得一些系统环境信息	通过@Context可以获得以下信息：UriInfo、ServletConfig、ServletContext、HttpServletRequest、HttpServletResponse和HttpHeaders等
@XmlRootElement	将bean转换为xml	如果要讲bean以xml或json的格式返回，必须要这个注解。比如：
@XmlRootElement
public class User{...}
```