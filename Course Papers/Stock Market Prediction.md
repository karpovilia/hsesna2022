# Stock market prediction

Утверждение: анализировать имеет смысл только иностранный рынок. Наш рынок полностью инсайдерский.

## Прочитать:
* Посмотреть [подборку на google scholar](https://scholar.google.ru/scholar?start=20&q=stock+price&hl=en&as_sdt=2005&sciodt=0,5&cites=4768437242681188965&scipsc=1)
* "**[A survey of the application of graph-based approaches in stock market analysis** and prediction](https://link.springer.com/article/10.1007/s41060-021-00306-9)"
* "[FactorVAE: A Probabilistic Dynamic Factor Model Based on Variational Autoencoder for Predicting Cross-sectional Stock Returns](https://www.aaai.org/AAAI22Papers/AAAI-12027.DuanY.pdf)"
* "[Forecasting Stock Prices Using Stock Correlation Graph: A Graph Convolutional Network Approach](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9533510)" AAAI 2022
## Возможно, прочитать
* Китайцы пытаются решить задачу регрессии без GAT [sciencedirect](https://pdf.sciencedirectassets.com/280179/1-s2.0-S1877750318X00052/1-s2.0-S1877750317306361/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEEgaCXVzLWVhc3QtMSJHMEUCIDzt7y0CgWtGtc3dfF8xkSkFeGb6MFoeMqOJCm%2FAtURdAiEA2Bzyox4H4HzXQVtA6Z1VWSnU2w0rsG%2F7QfAb9MrEpsIqgwQI8f%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAEGgwwNTkwMDM1NDY4NjUiDJ2Cbi61tAu8yjJ21irXA3b2T0Lr6Z4HvyR99xXb8A3kjjAg0ybop7GwII8vuNvUC01qAE3Ry9rCG9dd5v0Jaogd6cur0FCuzFhimKLtuhfl5R9HSs8jdw5NSZV0%2B95Ku7sESqqXNXBQiftNoPSA7Yi9vjqdiPKTC53tmM6KBxfNeebM3Y1EiaZM95u%2FjWq0JapR675tbONS%2BL5dPULQcyjU813g%2Fg%2BJ0HT6w%2Bfkn5Xv5ilirY6VsuRBe6pRsXGAiPHXvDiCiXVhCUwmCETfWJmvigkKfXpMbPIVj9bPGYuSO0Z0j7n82bpHePs21tTPtadOF938IXl91nyPGa6U2ckV9m%2F5WjHgrQxv%2B02BivpsHf%2FcFa5RYRPK4CGG7MVJUXt1PW%2BKTKozHWcrwbKoi7lfgssp9s1%2FA7tJXJ29G%2FhSD0dcmTFE8kUcMDFufwbrFP11d1Lad11mWKoPEQtSHClPMaSzanchj8SDIdiUWDkqixBDAFyUzycJSAZIPrXAUnw7e%2F8w14ZlMK19ZGXL42ynYEhxCqwDd%2B5thIMwRLWkHZDrVtUZ%2FDCT%2FVraKO%2FPdgx9f7gG33tVvTZKhvRzQSLq%2FZRVMpB1Tnkehp7DcwyI0MPaHv%2BU%2BFHc9lq3D4NkOThMFQgqvjD6ufuSBjqlAeZFpxSatXxFdsIwmsr7eSjAmIttf%2FTZt%2BQvRWbdkwWqvSBVAE399gzT1isojydSrrfArV6tvqAwp8z3HPnM5YGKI2QVPiTFEXtU%2FCvSv%2Ft8BqKYHyWGEER%2BscdxJc9myEYDe%2B6nwcL6DBchM0UmZ%2BW%2B5rL3cQQkbmSzSpDgO60uzCvgIRDnz0KZPI9mmUbThDHzQ7sv7pQTnXGvCmbKglSfwWv6zg%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20220419T170746Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYYGR6UXCZ%2F20220419%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=e8d1ea80f299618c1ab97f2a0e041dcdc652dfffd9be1e4874fdf2b55ff3c010&hash=d92fd2d1897998a9a8cb1fe6fbdf06854b53e6719c9897925aabc29e00ef97b3&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S1877750317306361&tid=spdf-b72d0a80-93dd-4768-b27e-6f26663f9d43&sid=0a540f5629f12849831af9097fbf9408b51egxrqb&type=client)
* "[FinGAT: Financial Graph Attention Networks for Recommending Top-K Profitable Stocks](https://arxiv.org/abs/2106.10159)"

Источник данных:
* twitter
* tinkoff 
* ???

Возможные идеи:
1. Прогнозирование того, как твиты ключевых пользователей влияют на стоимость - важно смотреть кто написал, а не сколько раз. 
    * В этом как раз могут помочь центральности (много подписчиков, значит ерунды не скажет) или GAT эмбеддинги
    * Вариант с центральностями плох тем, что пользователей очень много и получается задача с $\infty$ коррелирующими переменными.
    * В случае с GAT непонятно как поставить задачу градиентной оптимизации.

2. Акции соседних компании сильно коррелируют. Если видим что падает одно, можем спрогнозировать и падение второго. Для этого можно посмотреть корреляцию трендов и оценить меру близости между компаниями, дальше сплошной GAT. Более подробнее см. "[Forecasting Stock Prices Using Stock Correlation Graph: A Graph Convolutional Network Approach](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9533510)"

