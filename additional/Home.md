# Изпит

Изпита ще бъде под формата на тест или практическа задача (за който има желание) и ще се провде присъствено на 31.03.2023

Goggle Classroom: ???

# Въведение в web програмирането с Java и JavaScript.

Практически курс насочен към изучаване на инструменти и технологии необходими за изграждане на съвремени Java и JavaScript базирани web приложения. По време на курса стъпка по стъпка се изгражда работещо web приложение със [Spring Boot](https://spring.io/projects/spring-boot), [Spring MVC](https://docs.spring.io/spring/docs/5.1.6.RELEASE/spring-framework-reference/web.html#spring-web) и [ReactJS](https://reactjs.org/). Курса е предназначен за студентите изучавали Java.

## Конспект

1. [[Maven|maven]] – базови концепции, насочени основно към това как да си компилират и стартират примерите със разбиране какво се прави.
    1. [Стандартни стъпки](https://github.com/hrabur/web-programming-course/wiki/Maven#%D0%A1%D1%82%D0%B0%D0%BD%D0%B4%D0%B0%D1%80%D1%82%D0%BD%D0%B8-%D1%81%D1%82%D1%8A%D0%BF%D0%BA%D0%B8-build-lifecycle)
    2. [Зависимости (Dependencies)](https://github.com/hrabur/web-programming-course/wiki/Maven#%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BD%D0%B0-%D0%B7%D0%B0%D0%B2%D0%B8%D1%81%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D0%B8)
    3. [Хранилища (Maven repository)](https://github.com/hrabur/web-programming-course/wiki/Maven#%D0%A5%D1%80%D0%B0%D0%BD%D0%B8%D0%BB%D0%B8%D1%89%D0%B0-%D0%B7%D0%B0-%D0%B0%D1%80%D1%82%D0%B5%D1%84%D0%B0%D0%BA%D1%82%D0%B8-repositories)
    4. [Стандартна структура](https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html)
2. [[HTTP|HTTP]] и REST – базови концепции за да може да се осмисли как работи едно Web приложение и Servlet API-то
    1. [URL](https://github.com/hrabur/web-programming-course/wiki/HTTP#url-aka-uri)
    2. [Request/Response и техният формат](https://github.com/hrabur/web-programming-course/wiki/HTTP#http-1)
    3. [HTTP методи – GET/POST/...](https://github.com/hrabur/web-programming-course/wiki/HTTP#http-1)
    4. [REST](https://github.com/hrabur/web-programming-course/wiki/HTTP/#rest)
3. Spring Boot
    1. Шаблони използвани в Spring Framework
        1. Dependency Injection (DI) и Inversion of Control (IoC)
        2. Proxy (Посредник)
    2. Spring Been и неговият жизнен цикъл
    3. Java конфигурация и търсене в пътя с класовете (classpath scanning)
4. Spting MVC – основи на съвременото web програмиране
    1. Защо не Servlet API + JSP? (няма да е в теста)
    2. Анотации и основни концепции
    3. Работа с форми – свързване и валидация (няма да е в теста)
    4. Spring tag library (няма да е в теста)
5. Spring Data, JPA and Hibernate
6. ReactJS - основи на съврененият потребителски интерфейс
    1. [Защо ReactJS](https://hrabur.github.io/reactjs-for-java-devs/#/subject)? (няма да е в теста)
    2. Основни концепции и инструменти за работа
    3. Въведение в ES6 и JSX синтакса (няма да е в теста)
    4. [Компоненти - обектно ориентирани и функционални](https://facebook.github.io/react/docs/components-and-props.html)
    5. Свойства (properties) на компонента
    6. Състояние (state) на компонента
    6. [Условно рендиране](https://facebook.github.io/react/docs/conditional-rendering.html)
    7. [Работа с форми](https://facebook.github.io/react/docs/forms.html) - [контролирани](https://facebook.github.io/react/docs/forms.html) и [неконтролитани](https://facebook.github.io/react/docs/uncontrolled-components.html) компоненти (няма да е в теста)
    8. [Пример - Ticker](https://jsbin.com/yijawir/5/edit?js,output) (няма да е в теста)

Материали с които може да бъде надграден курса (не са необходими за изпита :-)
* [Presentational and Container Components, article by Dan Abramov](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0)
* [You Might Not Need Redux, article by Dan Abramov](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)
* [Flux vs MVC (Design patterns)](https://medium.com/hacking-and-gonzo/flux-vs-mvc-design-patterns-57b28c0f71b7)
* [Getting Started with Redux, web course by Dan Abramov](https://egghead.io/courses/getting-started-with-redux)
* [Building React Applications with Idiomatic Redux, web course by Dan Abramov](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)