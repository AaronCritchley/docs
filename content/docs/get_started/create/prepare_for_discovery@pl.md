---
$title: Przygotowanie strony do wykrywania i rozpowszechniania
---

Czasami dana strona, na przykład artykuł wiadomości, potrzebna jest w wersji AMP i tradycyjnej. Rozważmy następujący przypadek: Jeśli usługa Szukaj w Google znajdzie wersję tradycyjną tej strony, *skąd będzie wiedziała, że istnieje również wersja AMP tej strony*?

## Powiązanie stron za pomocą elementu &lt;link>

Aby rozwiązać ten problem, do każdej wersji strony dodaliśmy informacje o drugiej wersji, używając znaczników `<link>` w sekcji `<head>`.

Dodaj następujący wpis do strony w wersji tradycyjnej:

[sourcecode:html]
<link rel="amphtml" href="https://www.example.com/url/to/amp/document.html">
[/sourcecode]

A ten do strony AMP:

[sourcecode:html]
<link rel="canonical" href="https://www.example.com/url/to/full/document.html">
[/sourcecode]

## A co, jeśli jest tylko jedna strona?

Jeśli jest tylko jedna wersja strony i jest to wersja AMP, nadal konieczne jest dodanie do niej linku kanonicznego, które w takim wypadku wskaże tę samą stronę:

[sourcecode:html]
<link rel="canonical" href="https://www.example.com/url/to/amp/document.html">
[/sourcecode]

<a class="go-button button" href="/pl/docs/get_started/create/publish.html">Przejdź do kroku 6</a>
