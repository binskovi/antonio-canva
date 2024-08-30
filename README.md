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

## Setting up Fabric.js

https://github.com/fabricjs/fabric.js

instalacja, nie wszystkie nowe wersje współpracują prawidłowo stąd konkretna isntalacja.
```
bun add fabric@5.3.0-browser
bun add -D @types/fabric@5.3.0
```
### 1. page.tsx
```
import { Editor } from "@/features/editor/components/editor";

const EditorProjectIdPage = () => {
  return (
    <Editor />
  );
};

export default EditorProjectIdPage;
```
Opis:
* EditorProjectIdPage: Jest to komponent strony, która w Next.js pełni rolę strony dla danego URL. W tym przypadku, komponent ten renderuje jedynie komponent Editor, co sugeruje, że ta strona jest dedykowana do pracy z edytorem Canvas.

### 2. use-editors.ts
```
import { fabric } from "fabric";
import { useCallback } from "react";

export const useEditor = () => {
  const init = useCallback(
    ({
      initialCanvas,
      initialContainer,
    }: {
      initialCanvas: fabric.Canvas;
      initialContainer: HTMLDivElement;
    }) => {
      fabric.Object.prototype.set({
        cornerColor: "#FFF",
        cornerStyle: "circle",
        borderColor: "#3b82f6",
        borderScaleFactor: 1.5,
        transparentCorners: false,
        borderOpacityWhenMoving: 1,
        cornerStrokeColor: "#3b82f6",
      });

      const initialWorkspace = new fabric.Rect({
        width: 900,
        height: 1200,
        name: "clip",
        fill: "white",
        selectable: false,
        hasControls: false,
        shadow: new fabric.Shadow({
          color: "rgba(0,0,0,0.8)",
          blur: 5,
        }),
      });

      initialCanvas.setWidth(initialContainer.offsetWidth);
      initialCanvas.setHeight(initialContainer.offsetHeight);

      initialCanvas.add(initialWorkspace);
      initialCanvas.centerObject(initialWorkspace);
      initialCanvas.clipPath = initialWorkspace;

      const test = new fabric.Rect({
        width: 100,
        height: 100,
        fill: "black",
      });

      initialCanvas.add(test);
      initialCanvas.centerObject(test);
    },
    []
  );

  return { init };
};

```
Opis:

* useEditor: Jest to customowy hook Reacta, który dostarcza funkcję init, odpowiedzialną za inicjalizację Canvas i ustawienia początkowe.
* useCallback: Używane, aby zapewnić, że funkcja init nie zostanie ponownie zdefiniowana przy każdym renderowaniu, co jest istotne z punktu widzenia wydajności. Zwraca ona funkcję inicjalizującą init, która przyjmuje dwa parametry: initialCanvas (obiekt fabric.Canvas) oraz initialContainer (kontener HTML dla Canvas).

Wewnątrz funkcji init:
* Konfiguracja obiektów Fabric.js: Modyfikuje domyślne ustawienia wszystkich obiektów na Canvas (np. styl narożników, kolory obramowania).
* Tworzenie initialWorkspace: Tworzy nowy prostokąt, który pełni rolę głównego obszaru roboczego na Canvas, z cieniowaniem i innymi ustawieniami wizualnymi.
* Inicjalizacja rozmiaru Canvas: Ustawia rozmiar Canvas na podstawie rozmiaru kontenera, w którym jest osadzony.
* Dodanie initialWorkspace do Canvas: Dodaje initialWorkspace do Canvas i centrowanie go.
* Ustawienie ClipPath: Ustawia obszar roboczy jako ClipPath, co oznacza, że inne elementy będą widoczne tylko wewnątrz tego prostokąta.
* Dodanie test: Dodaje przykładowy czarny prostokąt jako element testowy do Canvas.

Funkcjonalność:
Hook useEditor zapewnia funkcję inicjalizującą, która przygotowuje Canvas do użytku, ustawiając odpowiednie wymiary, stylizacje oraz dodając początkowe elementy. Jest to kluczowe do dynamicznego renderowania i manipulowania obiektami na Canvas.

### 3. editor.tsx
```
"use client";

import { fabric } from "fabric";
import { useEffect, useRef } from "react";
import { useEditor } from "@/features/editor/hooks/use-editor";

export const Editor = () => {
  const { init } = useEditor();

  const canvasRef = useRef(null);
  const containerRef = useRef<HTMLDivElement>(null);

  useEffect(() => {
    const canvas = new fabric.Canvas(canvasRef.current, {
      controlsAboveOverlay: true,
      preserveObjectStacking: true,
    });

    init({
      initialCanvas: canvas,
      initialContainer: containerRef.current!,
    });
  }, [init]);

  return (
    <div className="h-full flex flex-col">
      <div className="flex-1 h-full bg-muted" ref={containerRef}>
        <canvas ref={canvasRef} />
      </div>
    </div>
  );
};

```
Opis:

* "use client": Jest to dyrektywa w Next.js, która oznacza, że ten plik działa po stronie klienta (czyli w przeglądarce). Jest to konieczne, ponieważ Fabric.js działa tylko w przeglądarce.
* useRef: Używane do referencji do elementów DOM (tu: <canvas> i jego kontener), co jest niezbędne do pracy z Fabric.js, ponieważ musimy przekazać rzeczywiste elementy DOM do inicjalizacji Canvas.
* useEffect: Używane do inicjalizacji Canvas, gdy komponent jest montowany.
  - Tworzy nowy obiekt fabric.Canvas i przekazuje referencję do elementu Canvas.
  - Wywołuje funkcję init z hooka useEditor, przekazując nowo utworzony obiekt Canvas oraz referencję do kontenera.
* JSX: Struktura JSX definiuje wygląd komponentu Editor. Mamy kontener <div>, który zajmuje całą dostępną wysokość (h-full), a w nim umieszczone jest <canvas>, które jest miejscem pracy Fabric.js.

Funkcjonalność:

Komponent Editor odpowiada za montowanie Canvas w DOM i jego inicjalizację za pomocą hooka useEditor. Cała logika inicjalizacji i ustawienia jest osadzona w useEffect, który jest uruchamiany przy montowaniu komponentu. To tutaj tworzony jest faktyczny obiekt Canvas oraz przypisywane są mu ustawienia i obiekty.