# JAVA-2
JAVA试验
##实验目的
初步了解分析系统需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法；
掌握面向对象的类设计方法（属性、方法）；
掌握类的继承用法，通过构造方法实例化对象；
学会使用super()，用于实例化子类；
掌握使用Object根类的toString（）方法,应用在相关对象的信息输出中。
##实验过程
1 创建系统，学生信息 老师信息 课程信息
2 创建类，利用private函数创建人名，年龄，学号等。
3 创建课程，学生，老师类，利用public函数进行编程。
4 改错并运行。
##核心方法
方法1
```
System.out.println("******************学生信息*********************");
		        Student hjh = new Student();
		        hjh.setName("何佳航");
		        hjh.setAge(19);
		        hjh.setNumber(2019310866);
		        hjh.setSex("男");
		        System.out.println("学生姓名:" + hjh.getName());
		        System.out.println("学生年龄:" + hjh.getAge());
		        System.out.println("学生编号:" + hjh.getNumber());
		        System.out.println("学生性别:" + hjh.getSex());
```
方法2	
```
class People{
		    public People(){

		    }
		    public People(String name,int age,int number,String sex){
		        this.name = name;
		        this.age = age;
		        this.number = number;
		        this.sex = sex;
		    }

		    private String name;
		    private int age;
		    private int number;
		    private String sex;

		    public String getName() {
		        return name;
		    }
		    public int getAge() {
		        return age;
		    }
		    public String getSex() {
		        return sex;
		    }
		    public int getNumber() {
		        return number;
		    }
		    public void setName(String name) {
		        this.name = name;
		    }
		    public void setAge(int age) {
		            this.age = age;
		    }
		    public void setNumber(int number) {
		        this.number = number;
		    }
		    public void setSex(String sex) {
		        this.sex = sex;
		    }

		}
```
方法3	
```
class Student extends People{
		    public Student(){

		    }
		    public Student(String name,int age,int number,String sex){
		        super(name, age, number, sex);
		    }
		}

		class Teacher extends People{
		    public Teacher(){

		    }
		    public Teacher(String name,int age,int number,String sex){
		        super(name, age, number, sex);
		    }
		    String lesson_1;
		    public String getLesson_1() {
		        return lesson_1;
		    }
		    public void setLesson_1(String lesson_1) {
		        this.lesson_1 = lesson_1;
		    }


		}
方法4
```
		class Lesson{
		    public Lesson(){

		    }
		    public Lesson(String name,String time,int number,String place){
		        this.name = name;
		        this.time = time;
		        this.number = number;
		        this.place = place;
		    }

		    private String name;
		    private String time;
		    private int number;
		    private String place;


		    public String getName() {
		        return name;
		    }
		    public String getTime() {
		        return time;
		    }

		    public String getPlace() {
		        return place;
		    }
		    public int getNumber() {
		        return number;
		    }
		    public void setName(String name) {
		        this.name = name;
		    }
		    public void setTime(String time) {
		        this.time = time;
		    }
		    public void setNumber(int number) {
		        this.number = number;
		    }
		    public void setPlace(String place) {
		        this.place = place;
		    }

		}
```
方法5
```	
  class Lesson_1 extends Lesson{
		    public Lesson_1(){

		    }
		    public Lesson_1(String name,String time,int number,String place){
		        super(name, time, number, place);
		    }
		    public String toString() {
		        return "课程名称：" + getName()+ "\n" + "上课时间：" + getTime() + "\n" + "课程编号：" + getNumber()+ "\n" + "授课地点：" + getPlace()+ "\n";
		    }

	}
 ```
 ##实验结果
 ******************学生信息*********************
学生姓名:何佳航
学生年龄:19
学生编号:2019310866
学生性别:男
******************教师信息*********************
授课教师:张世博
教师年龄:30
教师编号:10101010
教师性别:男
******************课程信息*********************
课程名称：Java
上课时间：每周五 下午4:05-5.30
课程编号：101001
授课地点：教306

******************课程详情*********************
选课成功，
##实验感想
该系统主要实现了学生选课的功能，这个系统是我独立完成在这次的课程设计中，层次化，模块化，也是我学到的一个重要的经验，参考一些资料后发现模块化能使程序设计更加简单，设计代码时目标更加明确，效率更高，以前虽然也知道这些道理，但自己真正实施起来却感到无从下手。开始有些听不懂，很害怕编程，但是从这次做完java编程之后我意识到只有用心去做没有什么困难的
