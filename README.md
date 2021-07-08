# !!! TODO !!!
# 说明

PHP [bc库](https://www.php.net/manual/zh/ref.bc.php) 是用于精确计算的库但是用起来就比较麻烦，尤其是公式特别长的时候，函数一层裹一层

举例
```php
//普通公式
$val = $a * $b * ($c + $d) / ($e - $f)
//bc库
$val = bcmul(bcmul($a, $b), bcdiv(bcadd($c + $d), bcsub($e, $f)));
```

想要的效果
```php
$val = bc_parse("{a} * {b} * ({c} + {d})/({e} - {f}), [
    'a' => $a,
    'b' => $b,
    'c' => $c,
    'd' => $c,
    'e' => $e,
    'f' => $f
]);
```


# API
!!! TODO !!!

```php
string bc_parse(string query, array $params);
//使用方法
$val = bc_parse("{a} * {b} * ({c} + {d})/({e} - {f}), [
    'a' => $a,
    'b' => $b,
    'c' => $c,
    'd' => $c,
    'e' => $e,
    'f' => $f
]);
```
## 进度

- [ ] 基础加减乘除
- [ ] 函数支持




