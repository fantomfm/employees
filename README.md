<h1> Описание проекта </h1>

<h3> 1.	Структура базы данных </h3>

<p> Employees – сотрудники. </p>
<p> Positions – должности. </p>
<p> RefStatuses – статусы должностей. </p>
<p> Placement – промежуточная таблица со связью many to many. </p>

<h3> 2. Файловая структура приложения </h3>

<p> •	app – каталог с файлами приложения. После разворачивания необходимо прописать адрес подключения к MySQL в файле /app/common/config/main-local.php. </p>
<p> •	docker-compose: </p>
<p> - mysql – каталог со скриптом загрузки таблиц и тестовых данных. </p>
<p> - nginx – каталог с конфигурационным фалом Nginx. </p>
<p> •	.env – файл с настройками подключения к MySQL для docker-compose. </p>
<p> •	Dockerfile* - файлы конфигураций docker-контейнеров. </p>
<p> •	docker-compose.yml – файл для разворачивания приложения. </p>

<h3> 3. В приложении реализованы действия </h3>

<p> •	Просмотр списка всех сотрудников с поиском по ФИО. </p>
<p> •	Создание нового сотрудника с указанием должности и сохранением фото в файловой системе, и пути к нему в БД. Изменение всех атрибутов существующего сотрудника. </p>
<p> •	Просмотр карточки сотрудника на отдельной странице. Увольнение сотрудника (переключение статуса в Уволен). Удаление сотрудника из БД. Удаление фото из файловой системы с очисткой записи из БД. </p>
<p> •	Просмотр на отдельной странице статистики с поиском по должности и дате на момент создания должности у сотрудника или перевода в статус Активный. Дата выбирается из диапазона. </p>

<h3> 4. Используемые модули и расширения </h3>

<p> •	Формирование моделей и CRUD с помощью модуля GII. </p>
<p> •	Формирование действий для работы со связью many-to-many с помощью расширения yii2-save-relations-behavior. </p>
<p> •	Работа со стилями с помощью Bootstrap 5.1.3. </p>
<p> •	Формирования выборки должностей в форме с помощью стороннего виджета Chosen::widget. </p>