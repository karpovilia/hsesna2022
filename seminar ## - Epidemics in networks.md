https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology
https://publications.hse.ru/en/chapters/210598897
https://www.researchgate.net/publication/223990697_Competition_among_memes_in_a_world_with_limited_attention


* Epidemics on networks with NetworkX and EoN [github](https://github.com/Mercurialll/tutors_and_projs/blob/master/jupyter_english/tutorials/Epidemics_on_networks_with_NetworkX_and_EoN_Syrovatskiy_Ilya.ipynb)



# Information propagation

Inf2Vec model

Авторы предлагают модель для эмбеддинга social influence. 

Эмбеддинг происходит следующим образом:

1. Для каждого юзера определяются два influence context: локальный и глобальный. Локальный контекст, это набор пользователей, полученный с помощью random-walk по propagation network, глобальный - набор юзеров, похожих по совершаемым действиям.
2. Эмбеддинг состоит из двух частей (два вектора): -
    1. Source Embedding - отвечающий за способность юзера влиять на других (S)
    2. Target Embedding - отвечающий за то насколько пользователь подвержен влиянию (T)
    3. байасы - influenceability и conformity
3. По контекстам и цепочкам экшонов для пар юзеров считаются вероятности влияния одного юзера на другого, вероятность считается через комбинацию S, T, biases, таким образом вектора фиттятся.

[feng2018.pdf](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/65ba9b1f-cf93-438e-9fa4-cc7bb7a87103/feng2018.pdf)

Inf2Vec model improvement + Influence Maximization task

Применение модели из прошлой статьи к задаче максимизации влияния.

Принципиально авторы не вносят в модель изменения, только обнаруживают, что для их задачи достаточно смотреть только на юзеров, которые в основном начинают активности, также они упрощают вычисления (насколько я понял делают облегченную модель, в которой эмбединги не вычисляются)

[7319-Article Text-10549-1-10-20200601.pdf](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a8e0649e-4ca4-4d63-b7fe-645ed4849fc3/7319-Article_Text-10549-1-10-20200601.pdf)

Deep Collaborative Embedding (DCE)

Автоэнкодер каскадов распространения информации. Пока не очень вник, но выглядит достаточно громоздко. Сначала там собираются cascading contexts, которые для каждого каскада делают матрицу N*N (N - количество нодов), где значения на [i, j] это потенциальное влияние юзера i на юзера j в рамках данного каскада.

Затем для каждого нода собираются вектора их влияния на другие ноды в рамках разных каскадов, и это все подается на вход автоанкодеру, из которого достается эмбеддинг для нода.

[10.1016@j.knosys.2020.105502.pdf](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/edca08d7-81a8-40b2-82a2-5d01083516aa/10.1016j.knosys.2020.105502.pdf)

[https://github.com/geopanag/awesome-influence-maximization-papers/blob/master/readme.md](https://github.com/geopanag/awesome-influence-maximization-papers/blob/master/readme.md)


## References
* CitationIE: Leveraging the Citation Graph for Scientific Information Extraction [pdf](https://arxiv.org/pdf/2106.01560.pdf)
* [VigDet: Knowledge Informed Neural Temporal Point Process for Coordination Detection on Social Media](https://arxiv.org/abs/2110.15454)
* 
