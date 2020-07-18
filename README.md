# Java Gradle TestNG Selenium ChromeDriver Mac

1) Устаналиваем Selenium Java отсюда https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java <br>
Ищем в проекте build.gradle и в разделе dependencies добавляем:
```
compile group: 'org.seleniumhq.selenium', name: 'selenium-java', version: '3.141.59'
```
2) Создаем в корне проекта папку drivers и скачиваем туда драйвер браузера. Chrome Driver: https://chromedriver.chromium.org/downloads
3) Добавляем в проет TestNG отсюда https://mvnrepository.com/artifact/org.testng/testng
Ищем в проекте build.gradle и в разделе dependencies добавляем:
```
testCompile group: 'org.testng', name: 'testng', version: '7.1.0'
```
В build.gradle добавляем добаляем после dependencies раздел test: 
```
test {
    useTestNG()
}
```
4) В src-test-java создаем новый Java class в котором будет находиться первый тест. Пример теста для ChromeDriver можно взять тут: https://chromedriver.chromium.org/getting-started