# Работа IO_bound в одном потоке
![изображение](https://user-images.githubusercontent.com/73441333/144722768-26d79c1f-785e-423c-9195-0385d31c52ef.png)

![изображение](https://user-images.githubusercontent.com/73441333/144757687-b0d2030b-b76b-4ab3-b7de-2d325d6091cf.png)
![изображение](https://user-images.githubusercontent.com/73441333/144757712-4c7870ca-78e6-451c-99ed-cddc0c0beef6.png)
Работало минут 40

## Работа в нескольких потоках:
**5:**
![изображение](https://user-images.githubusercontent.com/73441333/144758024-617d07e2-bc3f-4c56-b748-6ed98ca4b718.png)
![изображение](https://user-images.githubusercontent.com/73441333/144758202-2040d3e9-1855-49e7-bfd3-0d8ac948ec57.png)
![изображение](https://user-images.githubusercontent.com/73441333/144758212-b6236f8f-aa65-4068-889b-287fb341bdbc.png)


**10:**
![изображение](https://user-images.githubusercontent.com/73441333/144758123-e4547762-15cf-46a3-93e7-ff01c56788c6.png)
![изображение](https://user-images.githubusercontent.com/73441333/144758249-8578ba20-b83a-4ab5-8eae-fd89af684d66.png)
![изображение](https://user-images.githubusercontent.com/73441333/144758259-82fe77d7-9850-47d6-acc5-32667c6de3a5.png)


**100:**
![изображение](https://user-images.githubusercontent.com/73441333/144758148-7f79c13c-555e-433e-9781-ae1f594ed120.png)
![изображение](https://user-images.githubusercontent.com/73441333/144758299-f61c5f9d-4966-43cd-8c73-544cf2d08bb2.png)
![изображение](https://user-images.githubusercontent.com/73441333/144758311-58695b01-92d8-4959-bede-229eb10dbe55.png)


**Вывод:** чем больше воркеров, тем больше используется ресурсов (память, процессор, сеть...) и теб быстрее выполняется задача


# Задача CPU_bound
**Генерируем 5 монет на 1 ядре**
![изображение](https://user-images.githubusercontent.com/73441333/144759367-18dd6f5b-5ccb-4181-ac42-467d6d3916da.png)
**Разбиение на 2 процесса**
Затраченное время на 5 момент:
![изображение](https://user-images.githubusercontent.com/73441333/144759526-bcbe194b-e096-454f-8f32-18be2d375e65.png)

Нагрузка:
![изображение](https://user-images.githubusercontent.com/73441333/144759495-0ed367ac-c232-42ca-b817-3cefc99cd594.png)

**Разбиение на 4 процесса**
Затраченное время на 5 момент:
![изображение](https://user-images.githubusercontent.com/73441333/144759588-f783a250-36b8-4651-b807-f8f3841b2fcf.png)

Нагрузка:
![изображение](https://user-images.githubusercontent.com/73441333/144759605-d7d13897-d877-4c16-be86-27af161e4d46.png)

**Разбиение на 5 процессов**
Затраченное время на 5 момент:
![изображение](https://user-images.githubusercontent.com/73441333/144759626-bc39cebc-8874-45c8-a749-4988a6d51c39.png)

Нагрузка:
![изображение](https://user-images.githubusercontent.com/73441333/144759647-37627fcc-f9f6-40fc-b85c-f0e82c0585b4.png)
**Вывод:**
Дальше разбивать бесполезно, так как процессор на моём компьютере 4 ядерный. С увеличением количества задействованных ядер растёт загрузка процессора и памяти, а время работы в среднем уменьшается. Однако такое происходит пока не дошли до 5.
