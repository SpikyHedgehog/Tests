Высылаю ответы на вопросы.

 Вопрос №1
 Читали ли вы чужой код? Если да, то что это был за код? Опишите свои впечатления от него.

Да, читал. Попадался разный - был и тот, который читать приятно, а был и такой, который только в самых страшных кошмарах присниться может.
На предыдущих местах работы обычно попадался красивый код.


 Вопрос №2
 Опишите известные вам языки программирования и их предназначение.

C, C++, C#, Паскаль, ассемблер, java, js, python. Предназначение любого языка программирования - написать что-нибудь, чтоб работало. А вот области применения различны. А некоторые из перечисленных (например паскаль) можно считать умершими. Ассемблер - язык низкого уровня, потому его логично применять, когда нужно написать что-то, близкое к железу (драйвера, компиляторы, ОС, прошивки). Очевидно тут надо понимать, что ассемблер скорее всего будет использоваться в паре с другим языком. С и С++ - где-то видел хохму, что их можно считать как фреймворк над ассемблером. Это языки более высокого уровня, однако они не перекладывают на программиста значительное число задач (например по управлению памяти). В частности, вместо того, чтоб регулярно запускать сборщик мусора, освобождением памяти должен заниматься разработчик. Что обычно даёт существенный прирост в производительности. Потому, обычно применяют их там, где нужна высокая производительность, зачастую в паре с ассемблером. js - скриптовый язык для браузеров.Потому, очевидно, фронтэнд в вебе. Питон - у меня не сложилось мнение о нём, и не так много с ним работал. Такое чувство, что хотели создать универсальный язык, удобный для разработки.


 Вопрос №3
 Что такое "компилятор", зачем он нужен и почему некоторые языки обходятся без него?

В любом случае, выполнять какие-то действия (программу) будет процессор. А у него свой язык, потому программу требуется перевести во что-то близкое к нему (в объектный код, в машинный код, иногда в ассемблер). Собственно, компилятор этим и занимается - на вход получает исходный код, на выход даёт тоже самое, но на машинно-ориентированном языке, обычно объектный код.
Некоторые языки используют интерпретатор - выполняют команды построчно. 
Существуют языки, которые используют и компилятор и интерпретатор.


 Вопрос №4
 Что такое "фреймворк" и для чего он нужен? Приведите примеры известных вам фреймворков.

Условно можно считать за библиотеку. Но отличается от библиотек тем, что накладывает ограничения на структуру программы и архитектуру.
Известные мне фреймворки - vue.js, ef. Слышал и о других, например angular, react, django.


 Вопрос №5
 Что за приставка "http://" перед адресами сайтов и почему она всё чаще теперь становится "https://"?

Это указание для браузера, что нужно использовать протокол http (ну или https, в зависимости от написанного). https - расширение для протокола http,
куда добавили шифрование данных. Обычно передаются поверх ssl или tls.


 Вопрос №6
 Самая популярная библиотека для разработки фронтенд-приложений, ReactJS, моделирует логику в виде компонентов.
 Если бы вам нужно было на ReactJS разработать страницу профиля ВКонтакте (например, https://vk.com/id1), на какие компоненты вы бы её разбили? Почему именно так?

Так получилось, что и вконтакте прошел мимо меня, и с реактом я не работал. Разбивал бы я на компоненты по функциональности. 
т.е. выделил бы такие:
верхняя панель с поиском, левая панель с входом и регистрацией, (по всей видимости ещё одна левая панель со списком настроек). Если реакт поддерживает вложенные компоненты, то всё остальное объеденил бы в одну компоненту, и разбил бы её на такие: левый блок (который с фотографией и не скроллится и панелькой ниже), и правый блок (который разбил бы на личные данные, галерею, и стену).


 Вопрос №7
 SqlServer, PostgreSQL, SQLLite, MySQL, Oracle, Microsoft Access - разные базы данных с разным функционалом, которые разрабатываются, в основном, разными компаниями с разным видением своего продукта.
 Однако все эти базы используют один и тот же язык запросов - SQL, и не планируют от него отказываться. Как так получается? Что такого в SQL, что он подходит всем этим базам?
А если он такой чудесный, то почему многие другие базы данных, вроде MongoDB или Cassandra, его не используют?

Так исторически сложилось. В итоге имеем, что скрипты, использующиеся в одной базе, можно с минимальными доработками использовать в другой. Итого его плюсы - стандартизация, независимость от субд. 
В SQL есть существенный минус - сложность работы с иерархическими структурами. Полагаю, этот существенный минус и повлиял на развитие альтернативных субд.


 Вопрос №8
 Пришлите ссылку на пример вашего кода на C#, за который вам не стыдно. Если кода нет, выполните задание ниже. Оно также поможет, если код есть.
 Пожалуйста, не пишите код внутри форм ответов, разместите его на Github и приложите ссылку. Если в задании что-то непонятно, опишите возникшие вопросы и сделанные предположения. Например, в комментариях в коде.
 Задание:
 Напишите библиотеку для поставки внешним клиентам, которая умеет вычислять площадь круга по радиусу и треугольника по трем сторонам. Дополнительно к работоспособности оценим:
 Юнит-тесты
 Легкость добавления других фигур
 Вычисление площади фигуры без знания типа фигуры
 Проверку на то, является ли треугольник прямоугольным
 Вопрос №9
 В базе данных MS SQL Server есть продукты и категории. Одному продукту может соответствовать много категорий, в одной категории может быть много продуктов. Напишите SQL запрос для выбора всех пар «Имя продукта – Имя категории». Если у продукта нет категорий, то его имя все равно должно выводиться.


восьмое тут: https://github.com/SpikyHedgehog/FiguresAndTests
девятое тут: https://github.com/SpikyHedgehog/FiguresAndTests/blob/master/Task9.sql
Дополнительный код залил сюда: https://github.com/SpikyHedgehog/FileSearcher



