# Antonio Course - Canva 🚀
Technologie: Tailwind | React.js | PostgreSQL | Drizzle | Next.js | Hono | Next Auth
## Setup
Instalacja Managera Pakietów BUN
```
curl -fsSL https://bun.sh/install | bash
```
Tworzenie projektu:
```
bunx create-next-app@latest image-ai
```
Konfiguracja instalacji:
* Would you like to use TypeScript? … No / <u>Yes</u>
* Would you like to use ESLint? … No / <u>Yes</u>
* Would you like to use Tailwind CSS? … No / <u>Yes</u>
* Would you like to use src/ directory? … No / <u>Yes</u>
* Would you like to use App Router? (recommended) … No / <u>Yes</u>
* Would you like to customize the default import alias (@/*)? › <u>No</u> / Yes

Instalacja paczki UI https://ui.shadcn.com/
```
bunx --bun shadcn-ui@latest init
```
Konfiguracja instalacji:
* Which style would you like to use? › Default
* Which color would you like to use as base color? › Slate
* Would you like to use CSS variables for colors? … no / yes

Uruchomienie projektu:
```
bun run dev
```
Instalacja kompnentów z shadcn np Button:
```
bunx --bun shadcn-ui@latest add button
```
## Basic of Next.js
Zaczerpnięte z dokumentacji:

Struktura Projektu Next.js

Struktura projektu w Next.js jest uporządkowana w sposób, który ułatwia organizację kodu i zasobów statycznych.
Główne foldery

Główne foldery są używane do organizowania kodu aplikacji i zasobów statycznych.

* app: Router aplikacji.
* pages: Router stron.
* public: Zasoby statyczne, które będą serwowane.
* src: Opcjonalny folder źródłowy aplikacji.

Pliki na najwyższym poziomie

Pliki na najwyższym poziomie są używane do konfiguracji aplikacji, zarządzania zależnościami, uruchamiania middleware, integracji narzędzi monitorujących oraz definiowania zmiennych środowiskowych.

* next.config.js: Plik konfiguracyjny dla Next.js.
* package.json: Zależności projektu i skrypty.
* instrumentation.ts: Plik OpenTelemetry i Instrumentation.
* middleware.ts: Middleware dla zapytań Next.js.
* .env: Zmienne środowiskowe.
* .env.local: Lokalne zmienne środowiskowe.
* .env.production: Zmienne środowiskowe dla produkcji.
* .env.development: Zmienne środowiskowe dla środowiska developerskiego.
* .eslintrc.json: Plik konfiguracyjny dla ESLint.
* .gitignore: Plik określający, które pliki i foldery mają być ignorowane przez Git.
* next-env.d.ts: Plik deklaracji TypeScript dla Next.js.
* tsconfig.json: Plik konfiguracyjny dla TypeScript.
* jsconfig.json: Plik konfiguracyjny dla JavaScript.

Konwencje routingu w folderze app

Konwencje te określają, jak definiować trasy i obsługiwać metadane w routerze aplikacji.

* layout.js/.jsx/.tsx: Layout strony.
* page.js/.jsx/.tsx: Strona.
* loading.js/.jsx/.tsx: Interfejs ładowania.
* not-found.js/.jsx/.tsx: Interfejs strony nieznalezionej.
*  error.js/.jsx/.tsx: Interfejs błędu.
* global-error.js/.jsx/.tsx: Globalny interfejs błędu.
* route.js/.ts: Punkt końcowy API.
* template.js/.jsx/.tsx: Ponownie renderowany layout.
* default.js/.jsx/.tsx: Strona zastępcza dla równoległych tras.

Zagnieżdżone trasy

* folder: Segment trasy.
* folder/folder: Zagnieżdżony segment trasy.

Dynamiczne trasy

* [folder]: Dynamiczny segment trasy. <- możemy podłóżyć dowolony slug
* [...folder]: Segment trasy obejmujący wszystkie dopasowania.
* [[...folder]]: Opcjonalny segment trasy obejmujący wszystkie dopasowania.

Grupy tras i prywatne foldery

* (folder): Grupowanie tras bez wpływu na routing. <- np grupujemy w folderze auth a trasy są bezpośrednio po głownej domenie.
* _folder: Folder i wszystkie jego segmenty są wyłączone z routingu.

Równoległe i przechwycone trasy

* @folder: Nazwany slot.
* (.)folder: Przechwytywanie na tym samym poziomie.
* (..)folder: Przechwytywanie poziom wyżej.
* (..)(..)folder: Przechwytywanie dwa poziomy wyżej.
* (...)folder: Przechwytywanie od root.

Konwencje plików metadanych
Ikony aplikacji

* favicon.ico: Plik favicon.
* icon.ico/jpg/jpeg/png/svg: Plik ikony aplikacji.
* icon.js/ts/tsx: Generowana ikona aplikacji.
* apple-icon.jpg/jpeg/png: Plik ikony Apple App.
* apple-icon.js/ts/tsx: Generowana ikona Apple App.

Obrazy Open Graph i Twitter

* opengraph-image.jpg/jpeg/png/gif: Plik obrazu Open Graph.
*  opengraph-image.js/ts/tsx: Generowany obraz Open Graph.
* twitter-image.jpg/jpeg/png/gif: Plik obrazu Twitter.
* twitter-image.js/ts/tsx: Generowany obraz Twitter.

SEO

* sitemap.xml: Plik mapy strony.
* sitemap.js/ts: Generowana mapa strony.
* robots.txt: Plik robots.
* robots.js/ts: Generowany plik robots.

Konwencje routingu w folderze pages

Konwencje te określają, jak definiować trasy w routerze stron.
Pliki specjalne:

* _app.js/.jsx/.tsx: Niestandardowa aplikacja.
*  _document.js/.jsx/.tsx: Niestandardowy dokument.
*  _error.js/.jsx/.tsx: Niestandardowa strona błędu.
* 404.js/.jsx/.tsx: Strona błędu 404.
* 500.js/.jsx/.tsx: Strona błędu 500.

Trasy
Konwencja folderów

* index.js/.jsx/.tsx: Strona główna.
* folder/index.js/.jsx/.tsx: Zagnieżdżona strona.

Konwencja plików

* index.js/.jsx/.tsx: Strona główna.
* file.js/.jsx/.tsx: Zagnieżdżona strona.

Dynamiczne trasy
Konwencja folderów

* [folder]/index.js/.jsx/.tsx: Dynamiczny segment trasy.
* [...folder]/index.js/.jsx/.tsx: Segment trasy obejmujący wszystkie dopasowania.
* [[...folder]]/index.js/.jsx/.tsx: Opcjonalny segment trasy obejmujący wszystkie dopasowania.

Konwencja plików

* [file].js/.jsx/.tsx: Dynamiczny segment trasy.
* [...file].js/.jsx/.tsx: Segment trasy obejmujący wszystkie dopasowania.
* [[...file]].js/.jsx/.tsx: Opcjonalny segment trasy obejmujący wszystkie dopasowania.
