# tp5-category
这是一个基于ThinkPHP5框架的无限分类库

## 案例展示
> 基于ThinkPHP5开发呈现分页的效果  
![Image text](http://images.22058.com/github/tp5-category/category_1.jpg)

## 安装
> composer require zhujinkui/tp5-page

## 代码举例使用
> 建立Node控制器,读取节点列表
```
<?php
namespace app\common\controller;
use think\Controller;

class Node extends Controller
{
    /**
     * [index 节点管理]
     * @return array [节点树]
     */
    public function index()
    {
        $cat = new \think\Category('authRule', ['id', 'pid', 'title', 'fullname']);
        $temp = $cat->getList();
    }
 }
 
```
