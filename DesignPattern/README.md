> 作者：Caesar1014

# 学习并理解23种设计模式
> 设计模式（Design Pattern）是一套被反复使用、多数人知晓的、经过分类编目的、代码设计经验的总结，使用设计模式是为了可重用代码、让代码更容易被他人理解并且保证代码可靠性。


## 一、UML类图
每个模式都有相应的对象结构图，同时为了展示对象间的交互细节， 有些时候会用到 UML 图来介绍其如何运行。这里不会将 UML 的各种元素都提到，只想讲讲类图中各个类之间的关系， 能看懂类图中各个类之间的线条、箭头代表什么意思后，也就足够应对日常的工作和交流。同时，我们应该能将类图所表达的含义和最终的代码对应起来。有了这些知识，看后面章节的设计模式结构图就没有什么问题了。

### 1.1 关联
关联关系是用一条直线表示的，它描述不同类的对象之间的结构关系，它是一种静态关系，通常与运行状态无关，一般由常识等因素决定的。它一般用来定义对象之间静态的、天然的结构，所以，关联关系是一种“强关联”的关系。
比如，乘车人和车票之间就是一种关联关系，学生和学校就是一种关联关系，关联关系默认不强调方向，表示对象间相互知道。  
![avatar](https://github.com/Caesar1014/MarkDown/blob/master/DesignPattern/src/%E5%85%B3%E8%81%94.png?raw=true)

### 2.2 聚合
聚合关系用于表示实体对象之间的关系，表示整体由部分构成的语义，例如一个部门由多个员工组成。与组合关系不同的是，整体和部分不是强依赖的，即使整体不存在了，部分仍然存在。例如，部门撤销了，人员不会消失，他们依然存在。
```java
public class Team
{
    private Employee employee;
    public Team(Employee employee) {
        this.employee = employee;
    }

    public void setEmployee(Employee employee) {
        this.employee = employee;
    }
    ...
}

public class Employee
{
    ...
} 
```

### 2.3 组合
与聚合关系一样，组合关系同样表示整体由部分构成的语义。比如公司由多个部门组成，但组合关系是一种强依赖的特殊聚合关系，如果整体不存在了，则部分也不存在了。例如，公司不存在了，部门也将不存在了。
```java
public class Company
{
    private Department department;
    public Company() {
        department = new Department();
    }
}

publci class Department
{
    ...
}
```

### 2.4 继承
继承用一条带空心箭头的直接表示。

### 2.5 实现
实现关系用一条带空心箭头的虚线表示。


## 二、六大原则


## 三、模式分类