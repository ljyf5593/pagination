# 使用范例

控制器代码

    $pagination = new Pagination(array(
        'total_items' => $model->reset(FALSE)->count_all(), // 指定总共有多少条数据
    ));

    $this->content = View::factory('home/index');
    $this->content->pagination = $pagination

视图层代码

    <?php echo $pagination->render(); ?>