## Как работает?
- В проекте настроена проверка на `conventional commits`.
- Нельзя коммитить в ветку `master`. Для этого требуется создать PR.
- Чтобы сделать merge в ветку `master` должны пройти тесты.
- При пуше нового релизного тега или в релизную ветку создается/обновляется запись в реестре релизов и запускаются тесты.
- Если все тесты пройдены, то запускается деплой на GitHub Pages.

## Как проверить?
1. Отправляешь запрос на добавление в качестве collaborator.
2. Клонируешь репозиторий.
 - Локально запускаешь команду `npm ci`.
 - Локально запускаешь команду `npx husky install`.
3. Локально создаешь новую ветку, в которую добавляешь какие-то коммиты.
4. Делаешь push ветки и создаешь PR.
5. При необходимости вносишь hot-fixes, чтобы проверки проходили.
6. Делаешь merge в `master` ветку.
7. Делаешь pull изменений в локальную ветку `master` и создаешь локально новый релизный тег и пушишь его в `master`. 
8. Впоследствии должен появиться issue со всеми деталями о релизе, в котором можно отслеживать статус проверок и деплоя.
9.  При необходимости можно зайти в панель `Actions` и детально просмотреть как отрабатывает workflow (ссылка на который также есть в issue).
10. В конце концов можно будет кликнуть на ссылку и зайти на сам сайт, однако [изменения могут появитьтся спустя некоторое время](https://github.com/actions/deploy-pages/issues/86#issuecomment-1357970178).
