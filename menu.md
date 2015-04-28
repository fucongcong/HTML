# 后台重整

1.[改进后的优势](#_2)

2.[如何配置菜单](#_3)

## 改进后的优势
####1.可扩展性

####2.界面布局统一

## 如何配置菜单


####1.菜单配置文件放在各个Bundles/Resources/config/

    目前支持配置的菜单有：顶部导航，侧边导航，右侧tab和右侧button按钮

    (1)后台菜单配置文件为 menus_admin.yml

    下面是其中一部分:
    --------
    admin_category_create:
        name: 添加分类
        parent: admin_course_category
        router_params: {'groupId': 'group.id'}
        router_params_context: 1
        group: 2
        mode: modal
        blank: 1
        class: "demo"
        before: admin_course
--------

    1.admin_category_create  是这个菜单的code，唯一标识
    2.参数
        -name   菜单名称
        -parent   上一级菜单的code
        -router_name   菜单链接地址,可以不填，默认读取code作为router
        -router_params   router所需参数,可以不填，具体传一个数组如：router_params: {'groupId': 'group.id'},前面为key，后面为value
        -router_params_context 是否需要上下文数据，可以不填。【0(默认),1】。如果填了值为1会取上下文参数
        (如router_params: {'groupId': 'group.id'},那么group将会是你所在页面中的一个数组，group.id 取的这个数组的id的值)
        -group  所在菜单的分组,可以不填。【1(默认),2】
        -mode  页面展示形式，可以不填。【page(默认),modal(模态框)】
        -blank  是否新开窗口。【0(默认),1】
        -class  此菜单的类名
        -before  在哪个菜单之前，填对应菜单的code
        -after  在哪个菜单之后，填对应菜单的code  (与before共存时优先取before)

    3.下面给个例子:
    admin_course:
        name: 课程顶部导航
        parent: admin

    admin_course_manage
        name: 课程管理侧边导航
        parent: admin_course
        router_name: admin_course

    admin_course_manage_tab:
        name: 课程管理tab
        parent: admin_course_manage
        router_name: admin_course_manage

    admin_course_add:
        name: 创建课程button按钮
        parent: admin_course_manage_tab
        router_name: course_create
        group: 2-------------------------->button 取2
        blank: 1--------------------------->新开窗口
    

    页面中的调用,后台请继承TopxiaAdminBundle::layout.html.twig，必须统一！

    {% extends 'TopxiaAdminBundle::layout.html.twig' %}

    {% set menu = 'admin_course_manage_tab' %}

    menu这个值取当前tab的code。如果没有tab，请取侧边导航code
