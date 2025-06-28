### tp5-captcha
基于 https://github.com/top-think/think-captcha/tree/v2.0.2

### 安装
~~~
composer require ibibicloud/tp5-captcha
~~~

### 路由规则
~~~
Route::get('/captcha', function(){
    return captcha('', config('captcha'));
});
~~~
~~~
Route::get('/captcha','\\think\\captcha\\CaptchaController@index');
~~~

### 模板输出
~~~
<div>{:captcha_img()}</div>
~~~
~~~
<div><img src="{:captcha_src()}"></div>
~~~

### 手动验证
~~~
if ( !captcha_check($captcha) ) {
	// 验证失败
};
~~~