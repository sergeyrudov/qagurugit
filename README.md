# qagurugit
для выполения задания qaguru по git в группе

тест для добавления через pull request

    @Test
    @DisplayName("Поиск страницы selenide на Yandex.ru")
    public void searchSelenideInYandex() {
        parameter("Строка поиска","selenide");
        step("Открытие страницы yandex.ru", () -> {
            open("https://yandex.ru");
        });
        step("Поиск selenide в google", () -> {
            $("#text").val("selenide").pressEnter();});
        step("Проверка результатов поиска", () -> {
            $$(".serp-item").shouldHave(sizeGreaterThan(1));
            $("#search-result").shouldBe(visible).shouldHave(
                    text("Selenide: лаконичные и стабильные UI тесты на Java"),
                    text("selenide.org"));
        });
    }
