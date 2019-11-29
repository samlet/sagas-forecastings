# procs-time-series-forecastings.md
⊕ [利用Python进行时间序列分析和预测的端到端项目](https://towardsdatascience.com/an-end-to-end-project-on-time-series-analysis-and-forecasting-with-python-4835e6bf050b)
⊕ [Prophet: forecasting at scale – Facebook Research](https://research.fb.com/prophet-forecasting-at-scale/)
⊕ [facebook/prophet: Tool for producing high quality forecasts for time series data that has multiple seasonality with linear or non-linear growth.](https://github.com/facebook/prophet)

+ workspace/data-science/workspace/time-series-forecastings.ipynb
    * 预告工具Prophet于2017年由Facebook发布，旨在分析在不同时间尺度上显示模式的时间序列，例如年度，每周和每日。它还具有高级功能，可以对假期对时间序列的影响进行建模并实现自定义变更点。因此，我们正在使用Prophet来建立和运行模型。
+ google: python sales forecasting

## install
```sh
conda create --name ds python=3.6
using ds
# pip install fbprophet

# set up gcc
conda install gcc
# The easiest way to install Prophet is through conda-forge
# (安装失败, 必须要在vpn环境下)
conda install -c conda-forge fbprophet

## 直接使用pip: ⊕ [Detailed Installation Instructions — PyStan 2.18.0.0 documentation](https://pystan.readthedocs.io/en/latest/installation_beginner.html)

conda install numpy
pip install pystan
pip install fbprophet  # 编译失败
## issue: Failed building wheel for fbprophet

## 在macos上, 必须使用conda with vpn环境安装, 以下是全步骤:
conda install gcc
conda install numpy
conda install -c conda-forge fbprophet
```

+ 其它问题: 
    ⊕ [pip install error, Failed building wheel for fbprophet · Issue #722 · facebook/prophet](https://github.com/facebook/prophet/issues/722)

## start
```python
# cols = ['行ID'，'订单ID'，'发货日期'，'发货模式'，'客户ID'，'客户名称'，'细分'，'国家'，'城市'，'州'，'邮政编码'，'地区'，'产品ID'，'类别'，'子类别'，'产品名称'，'数量'，'折扣'，'利润'] 
cols = ['Row ID', 'Order ID', 'Ship Date', 'Ship Mode', 'Customer ID', 'Customer Name', 'Segment', 'Country', 'City', 'State', 'Postal Code', 'Region', 'Product ID', 'Category', 'Sub-Category', 'Product Name', 'Quantity', 'Discount', 'Profit']
furniture.drop(cols, axis=1, inplace=True)
furniture = furniture.sort_values('Order Date')
```


