# DEVIZ CRUD SYSTEM

<b>Languages</b> - <i>English</i>

<b>Język</b> - <i>Polski</i>

<i>[english]</i> <b>DEVIZ CRUD SYSTEM - Easy Application Development</b>

The control system is designed to create fast and efficient web applications. It is the basis for building web applications, the developer can quickly and easily create efficient applications. It has the structure of the model->controller->view application, as well as the database model function, thanks to which we can work quickly and efficiently on the data. The addition is an authorization controller that has the function of logging in, registering, activating the account and changing the password. Authorization in the system has been secured with a script that verifies the currently logged in user, it is a proprietary protection of the user's session. The system has an auxiliary function that we can use in our projects. It is important to remember that each of the system functionalities can be adapted to your needs.


The system is constantly being improved, full documentation is in the process of being written. Below are the installation instructions and product details.

<i>[polski]</i> <b>DEVIZ CRUD SYSTEM - Łatwe Tworzenie Aplikacji</b>

System kontroli został stworzony z myślą o tworzeniu szybkich i wydajnych aplikacji internetowych. Jest podstawą w budowaniu aplikacji internetowych, programista w szybki i łatwy sposób może tworzyć wydajne aplikacje. Posiada on strukturę aplikacji model->kontroler->widok, a także funkcję modelu bazy danych, dzięki którym możemy szybko i sprawnie pracować na danych. Dodatkiem jest kontroler autoryzacyjny, który posiada funkcję logowania, rejestracji, aktywacji konta i zmiany hasła. Autoryzacja w systemie została zabezpieczona skryptem weryfikującym aktualnie zalogowanego użytkownika, jest to autorskie zabezpieczenie sesji użytkownika. System posiada funkcję pomocniczne, z których możemy korzystać w swoich projektach. Ważne jest aby pamiętać, że każde z funkcjonalności systemu możemy dostosować do swoich potrzeb.


System cały czas jest udoskonalany, pełna dokumentacja jest w trakcie pisania. Poniżej instrukcja instalacji i szczegóły produktu.


<h2>Dokumentacja (polski)</h2>
<b>Język programowania:</b> PHP
<br>
<b>Framework:</b> CodeIgniter 4
<br>
<b>Nazwa systemu:</b> DEVIZ CRUD SYSTEM
<br>
<b>Wersja:</b> 1.0
<br>
<b>Autor:</b> Dawid Pogoda
<br>
<b>Licencja:</b> MIT


<h3>Instalacja:</h3>
<b>Wymagania - </b>Serwer PHP, wersja php 7.3+. 
<br>
<br>
Folder <b>deviz</b> wrzucamy do głównego folderu serwera www, nazwę folderu można zmienić.
<br>
<b>Apache XAMPP:</b> xampp\htdocs\deviz
<br>
<b>IIS:</b> inetpub\wwwroot\deviz
<br>
<b>Domain:</b> domains\deviz

<h3>Konfiguracja:</h3>
Wszystkich możliwości frameworka CI4 -> https://codeigniter.com/user_guide/intro/index.html
<br>
1. deviz\app\Config\App.php - Wpisujemy swój adres base url <code>public $baseURL = 'URL';</code> 
<br>
2. deviz\app\Config\Database.php - Wpisujemy dane do połączenia z naszą bazą <code>public $default</code>
<br>
3. deviz\app\Config\Email.php - Wpisujemy dane do połączenia adresu email <code>public $userAgent, $protocol, $SMTPHost, $SMTPUser, $SMTPPass, $SMTPPort</code>
<br>
4. deviz\app\Config\Security.php - Wpisujemy własną nazwę tokenu <code>public $tokenName</code> ( Domyślne DEVIZ CRUD SYSTEM ma włączone zabezpieczenia CI4 )
<br>
5. deviz\app\Config\Routes.php - Określamy domyślny folder aplikacji <code>$routes->setDefaultNamespace('App/Controllers');</code>, domyślny plik aplikacji <code>$routes->setDefaultController('Page');</code>, a także poprzez ścieżkę <code>$routes->get('/', 'Core/Page::index');</code>

<h2>Struktura CRUD</h2>
<h3>Controllers:</h3>
- Core (główny rdzeń, operacje wykonywane przed autoryzacją)
<br>
- Admin (kontrolery uprawnienia administracyjne)
<br>
- Site (kontrolery uprawnienia użytkownik)
<br>
<br>
<b>Controllers\Core:</b>
<br>
- BaseController.php (główny kontroler CI4)
<br>
- Page.php (kontroler przed autoryzacyjny)
<br>
- Login.php (kontroler autoryzacyjny)
<br>
- Registration.php (kontroler rejestracyjny)
<br>
- Activation.php (kontroler aktywacyjny)
<br>
- Reset.php (kontroler resetujący)
<br>
<br>
<b>Controllers\Admin:</b>
<br>
- Admin.php (kontroler autoryzacyjny admina)
<br>
- HomeAdmin.php (główny kontroler admina)
<br>
- ProfileAdmin.php (dodatkowy kontroler admina)
<br>
<br>
<b>Controllers\Site:</b>
<br>
- Site.php (kontroler autoryzacyjny użytkownika)
<br>
- Home.php (główny kontroler użytkownika)
<br>
- Profile.php (dodatkowy kontroler użytkownika)
<br>
<br>
<h3>Models:</h3>
- Deviz_model.php (funkcje połączenia z bazą danych)
<br>
- Ext_model.php (dodatkowe funkcje)
<br>
<br>
<h3>Views:</h3>
- core (widoki rdzenia aplikacji)
<br>
- admin (widoki administracyjne)
<br>
- site (widoki użytkownika)
<br>
<br>
<b>Views\core:</b>
<br>
- page.php (główny widok strony)
<br>
- headerPage.php (nagłówek strony)
<br>
- footerPage.php (stopka strony)
<br>
- logowanie.php (widok logowania)
<br>
- reset.php (widok resetu hasła)
<br>
<br>
<b>Views\admin:</b>
<br>
- homeAdmin.php (główny widok admina)
<br>
- headerAdmin.php (nagłówek admina)
<br>
- footerAdmin.php (stopka admina)
<br>
- profileAdmin.php (widok dodatkowego kontrolera)
<br>
<br>
<b>Views\site:</b>
<br>
- home.php (główny widok użytkownika)
<br>
- header.php (nagłówek użytkownika)
<br>
- footer.php (stopka użytkownika)
<br>
- profile.php (widok dodatkowego kontrolera)
<br>
<br>
<h3>Helpers:</h3>
- deviz_alert_helper.php (funkcje komunikatów)
<br>
- deviz_auth_helper.php (funkcje autoryzacyjne)
<br>
- deviz_key_helper.php (funkcje kluczy)
<br>
<br>
<h2>Przykład Tworzenia Aplikacji</h2>

