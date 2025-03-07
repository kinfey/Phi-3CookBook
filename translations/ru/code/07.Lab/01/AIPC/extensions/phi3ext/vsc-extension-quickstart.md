# Добро пожаловать в ваше расширение для VS Code

## Что находится в папке

* Эта папка содержит все файлы, необходимые для вашего расширения.
* `package.json` - это файл манифеста, в котором вы объявляете ваше расширение и команду.
  * Пример плагина регистрирует команду и определяет её название и имя команды. С этой информацией VS Code может отображать команду в палитре команд. На данном этапе плагин ещё не нужно загружать.
* `src/extension.ts` - это основной файл, где вы реализуете вашу команду.
  * Файл экспортирует одну функцию, `activate`, которая вызывается в первый раз, когда ваше расширение активируется (в данном случае при выполнении команды). Внутри функции `activate` мы вызываем `registerCommand`.
  * Мы передаем функцию, содержащую реализацию команды, как второй параметр в `registerCommand`.

## Настройка

* Установите рекомендуемые расширения (amodio.tsl-problem-matcher, ms-vscode.extension-test-runner и dbaeumer.vscode-eslint).

## Быстрый старт

* Нажмите `F5`, чтобы открыть новое окно с загруженным вашим расширением.
* Выполните вашу команду из палитры команд, нажав (`Ctrl+Shift+P` или `Cmd+Shift+P` на Mac) и введя `Hello World`.
* Установите точки останова в вашем коде внутри `src/extension.ts`, чтобы отладить ваше расширение.
* Найдите вывод вашего расширения в консоли отладки.

## Внесение изменений

* Вы можете перезапустить расширение из панели инструментов отладки после внесения изменений в `src/extension.ts`.
* Вы также можете перезагрузить (`Ctrl+R` или `Cmd+R` на Mac) окно VS Code с вашим расширением, чтобы загрузить изменения.

## Изучение API

* Вы можете открыть полный набор нашего API, открыв файл `node_modules/@types/vscode/index.d.ts`.

## Запуск тестов

* Установите [Extension Test Runner](https://marketplace.visualstudio.com/items?itemName=ms-vscode.extension-test-runner).
* Запустите задачу "watch" через команду **Tasks: Run Task**. Убедитесь, что она работает, иначе тесты могут не обнаружиться.
* Откройте представление Testing на панели активностей и нажмите кнопку "Run Test", или используйте горячую клавишу `Ctrl/Cmd + ; A`.
* Посмотрите результаты тестов в представлении Test Results.
* Вносите изменения в `src/test/extension.test.ts` или создавайте новые тестовые файлы в папке `test`.
  * Предоставленный тестовый раннер будет учитывать только файлы, соответствующие шаблону имени `**.test.ts`.
  * Вы можете создавать папки внутри папки `test`, чтобы структурировать ваши тесты так, как вам удобно.

## Дальнейшие шаги

* Уменьшите размер расширения и улучшите время запуска, [упаковав ваше расширение](https://code.visualstudio.com/api/working-with-extensions/bundling-extension?WT.mc_id=aiml-137032-kinfeylo).
* [Опубликуйте ваше расширение](https://code.visualstudio.com/api/working-with-extensions/publishing-extension?WT.mc_id=aiml-137032-kinfeylo) на маркетплейсе расширений VS Code.
* Автоматизируйте сборки, настроив [непрерывную интеграцию](https://code.visualstudio.com/api/working-with-extensions/continuous-integration?WT.mc_id=aiml-137032-kinfeylo).

**Отказ от ответственности**:  
Этот документ был переведен с использованием машинных услуг перевода на основе ИИ. Хотя мы стремимся к точности, пожалуйста, имейте в виду, что автоматические переводы могут содержать ошибки или неточности. Оригинальный документ на его исходном языке следует считать авторитетным источником. Для получения критически важной информации рекомендуется профессиональный перевод человеком. Мы не несем ответственности за любые недоразумения или неправильные интерпретации, возникшие в результате использования данного перевода.