За да свикваш сложи си направо Google Code Format в Eclipse-а:


1. Инсталирате Google Java Format Eclipse Plugin
    1. [Свали](https://github.com/google/google-java-format#eclipse)
    2. Копирате в */<eclipse_folder>/dropins
    3. Разирхивирате
    4. Рестартирате Eclipse
    5. Отивате в настройките на Eclipse (Windows -> Preferences -> "Formatter") и избирате “Formatter Implementation”: “google-java-format”
2. Конфигуриране на “active Profile”
    1. Сваляте локално [import](https://raw.githubusercontent.com/google/styleguide/gh-pages/eclipse-java-google-style.xml)
    2. Импортвате файла (стъпка 5)
    3. Избирате "Active Profile": GoogleStyle
3. Конфигуриране на Organize Imports
    1. Windows -> Preferences -> "Organize"
    2. only "* - all unmatched type imports"
4. Конфигуриране на Save Actions
    1. "Perform the selected actions on save"
    2. "Format the source code"
    3. "Format all lines"
    4. "Organize imports"
    5. "Additional actions"
5. За да сработи с Java 15+ Google Eclipse Plugin-а трябва да си добавиш в eclipse.ini-то:
    1. --add-modules=ALL-SYSTEM
    2. --add-exports=jdk.compiler/com.sun.tools.javac.api=ALL-UNNAMED
    3. --add-exports=jdk.compiler/com.sun.tools.javac.file=ALL-UNNAMED
    4. --add-exports=jdk.compiler/com.sun.tools.javac.parser=ALL-UNNAMED
    5. --add-exports=jdk.compiler/com.sun.tools.javac.tree=ALL-UNNAMED
    6. --add-exports=jdk.compiler/com.sun.tools.javac.util=ALL-UNNAMED
    7. --add-opens=java.base/java.lang=ALL-UNNAMED

    8. -javaagent:C:\dev\eclipse\lombok-1.18.24.jar

Последното е за Lombok-а (Трябва да бъде изтеглен и локацията в кода да се смени) 