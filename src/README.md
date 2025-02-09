<div class="lesson-question"><div class="lesson-description"><h3><strong>Условие:&nbsp;</strong></h3>

<p><br>
Склонируйте&nbsp;заготовку проекта по <a href="https://github.com/KataAcademy/PP_2_1_4_spring-types-of-wiring" target="_blank">ссылке</a>.<br>
<em>«На море на океане есть остров, на том острове дуб стоит, под дубом сундук зарыт, в сундуке — заяц, в зайце — утка, в утке — яйцо, в яйце — игла, — смерть Кощея»</em><br>
Зависимости остались прежние. В упражнении появился компонент Кощей Бессмертный (<code>KoscheiTheDeathless</code>), который расскажет, где находится его смерть, если вызвать метод <code>getRulesByDeth()</code>.<br>
Для описания поиска смерти использованы классы в пакете <code>models</code>. Для вашего удобства они были пронумерованы: <code>Ocean1, Island2, Wood3</code> и так далее.<br>
Чтобы Спринг видел все бины, в классе <code>AppConfig</code> была добавлена аннотация <code>@ComponentScan</code>.<br>
В Спринге связать бины можно различными способами, рассмотрим их на примере:<br>
1) <code>KoscheiTheDeathless</code> связывается с <code>Ocean1</code> через сеттер <code>setOcean</code> и аннотации <code>@Autowired</code> над ней.<br>
2) <code>Ocean1</code> связан с <code>Island2</code> через поле и аннотацию, которая подтянет бин <code>Island2</code> через метод <code>getIsland()</code> в классе <code>AppConfig</code>. Обратите внимание, что данный метод обозначен аннотацией <code>@Bean</code>, что автоматически подтягивает аргументы в метод. В качестве аргумента выступает бин <code>Wood3</code>.<br>
3) Бин <code>Wood3</code> помечен как компонент, который конструируется через связывание по <code>@Autowired</code> с помощью конструктора.</p>

<p>&nbsp;</p>

<h3><strong>Задание:&nbsp;</strong></h3>

<p><br>
Собрать цепочку до 8го элемента, использовав все вышеперечисленные методы связывания. После выполнения вы должны получить полную фразу. Проверьте своё решение тестом из заготовки.</p>
