# jd_ql_assistant

京东青龙抢购助手

## 主要功能

- 商品预约
- 定时提交（加购，预售，抢购）
- 有货提交（加购，预售）
- 查询订单

## 运行环境

- [qinglong](https://github.com/whyour/qinglong)

## 使用教程

- 配置环境变量
```
JD_COOKIE
```
- 安装依赖
```
requests
pycryptodome
```
- 创建定时任务
```
task jd.py -a <地区> -s <商品:数量> -b <时间> -m <模式> -i <账号序号>
```
```
a (area) <地区> # 【不填=默认地址】 地区id or 省份名称
s (sku_ids) <商品:数量> # 【必填】 商品id1:数量1,商品id2:数量2
b (buy_time) <时间> # 【必填】 抢购时间 00:00:00.00
m (mode) <模式> # 【必填】 加购<1> 预售<2> 抢购<3> 库存监控<4> 查询订单<5>
i (index) <账号序号> # 【不填=默认全部】 账号序号1,账号序号2
```

## 注意事项

- 核心算法编译成库，确保环境版本相同
- 定时任务时间需要小于抢购时间
- 设置发票信息`电子普通发票-个人`
- 设置取消使用`红包` `京豆`

## 待完成的功能

- [ ] 判断下单模式
- [ ] 抢优惠券

## 不考虑的功能

- ✖ 支付功能

## 支持

- 考研失败开发，欢迎合作支持
- ![image](https://github.com/SSJACK8582/jd_ql_assistant/blob/main/files/alipay.jpg)