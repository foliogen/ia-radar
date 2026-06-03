# iaRADAR

> Distribuye los contenidos de tu publicación digital a los buscadores y modelos de IA (ChatGPT, Gemini, Claude, Perplexity). Módulo nativo de **folioePress**.

[![Website](https://img.shields.io/badge/web-folioepress.com-185FA5)](https://folioepress.com/p/indexar-contenido-para-ia-publicaciones-digitales-ia-radar-medios-digitales-llms)
[![Estándar](https://img.shields.io/badge/est%C3%A1ndar-llms.txt-orange)](https://llmstxt.org/)
[![Licencia](https://img.shields.io/badge/licencia-CC0-green)](LICENSE)
[![Made in Spain](https://img.shields.io/badge/made%20in-Spain-AA151B)](https://foliogen.com)

---

## ¿Qué es iaRADAR?

**iaRADAR** es el módulo de **folioePress** que permite a editores de periódicos y revistas digitales **distribuir sus contenidos a los buscadores y modelos de inteligencia artificial** de forma sencilla, controlada y reversible.

Cuando un usuario pregunta a ChatGPT, Gemini, Claude o Perplexity sobre un tema, los modelos rastrean archivos como `llms.txt` para descubrir contenidos relevantes que poder citar como fuente. iaRADAR genera automáticamente ese archivo desde tu publicación, lo mantiene actualizado y te da herramientas para decidir qué se comparte y qué no.

## ¿Por qué importa?

- **El tráfico desde IAs está creciendo rápido.** En 2024 la búsqueda en LLMs era un 0,25% del total; las proyecciones para los próximos años hablan de 10% o más.
- **Aparecer citado por una IA es la nueva primera página de Google.** Tus lectores potenciales preguntan cada vez más a ChatGPT en lugar de a un buscador.
- **Control voluntario del editor.** Tú decides qué contenidos comparte tu medio con los modelos de IA y cuáles no, sin perder la propiedad intelectual.
- **No es entrenamiento sin permiso.** A diferencia del scraping masivo, `llms.txt` es una invitación voluntaria que tú emites cuando quieres y como quieres.

## ¿Qué genera iaRADAR?

1. **`llms.txt`** en la raíz de tu publicación — listado curado de contenidos clave para IAs.
2. **`robots.txt` optimizado** con configuración recomendada para bots IA (GPTBot, ClaudeBot, PerplexityBot, Google-Extended, etc.).
3. **Sitemaps específicos** filtrados para consumo por LLMs.
4. **Estadísticas de visitas** de bots IA a tu sitio, para que sepas quién te está leyendo.
5. **Análisis de competencia**: qué medios afines tienen `llms.txt` activo y cómo lo configuran.

## ¿Cómo funciona?

```
                ┌───────────────────────┐
                │  tu periódico digital │
                │   con folioePress     │
                └───────────┬───────────┘
                            │
                            │  iaRADAR
                            ▼
                ┌───────────────────────┐
                │     llms.txt          │
                │     robots.txt        │
                └───────────┬───────────┘
                            │
       ┌────────────────────┼────────────────────┐
       ▼                    ▼                    ▼
  ┌──────────┐         ┌──────────┐        ┌──────────┐
  │ ChatGPT  │         │  Claude  │        │Perplexity│
  └──────────┘         └──────────┘        └──────────┘
       │                    │                    │
       └────────────────────┼────────────────────┘
                            ▼
              respuestas con tu medio citado
```

1. iaRADAR analiza la estructura de tu publicación.
2. Genera un `llms.txt` con los contenidos más relevantes que has marcado como compartibles.
3. Configura `robots.txt` para permitir el acceso a los bots IA que decidas.
4. Los modelos de IA descubren tu contenido al rastrear estos archivos.
5. Tu medio empieza a aparecer citado en respuestas IA.

## Bots IA que iaRADAR gestiona

| Bot | Empresa | Función |
|-----|---------|---------|
| **GPTBot** | OpenAI | Entrenamiento de ChatGPT (puedes bloquearlo) |
| **ChatGPT-User** | OpenAI | Consultas en tiempo real de usuarios de ChatGPT |
| **OAI-SearchBot** | OpenAI | Búsqueda de ChatGPT Search |
| **ClaudeBot** | Anthropic | Indexación para Claude |
| **Claude-Web** | Anthropic | Consultas en tiempo real desde Claude |
| **PerplexityBot** | Perplexity | Indexación y búsquedas |
| **Google-Extended** | Google | Entrenamiento de Gemini |
| **CCBot** | Common Crawl | Datasets públicos de entrenamiento |
| **Bytespider** | ByteDance | Entrenamiento de modelos chinos |

iaRADAR permite **activar o bloquear cada uno individualmente** según tu política editorial. Por ejemplo: aceptar ChatGPT-User y Claude-Web (consultas en vivo) pero bloquear GPTBot y Google-Extended (entrenamiento).

## Ejemplos en este repositorio

| Archivo | Descripción |
|---------|-------------|
| [`examples/llms.txt`](examples/llms.txt) | Ejemplo real de `llms.txt` de folioepress.com |
| [`templates/llms.txt.template`](templates/llms.txt.template) | Plantilla con placeholders para tu publicación |
| [`templates/robots.txt.recommended`](templates/robots.txt.recommended) | Config recomendada de `robots.txt` para bots IA |

## El estándar llms.txt

`llms.txt` es un estándar propuesto por **Jeremy Howard** (Answer.AI) en septiembre de 2024. Es un archivo en formato Markdown ubicado en la raíz del sitio (al estilo de `robots.txt` o `sitemap.xml`) que proporciona a los modelos de IA un mapa estructurado y curado del contenido del sitio.

A diferencia de `sitemap.xml` (catálogo completo) o `robots.txt` (qué se puede rastrear), `llms.txt` es una **lista de lectura recomendada** que tú como editor curas explícitamente.

- 📖 Documentación oficial: [https://llmstxt.org/](https://llmstxt.org/)
- 📚 Directorio de sitios con `llms.txt`: [https://directory.llmstxt.cloud/](https://directory.llmstxt.cloud/)

## ¿Cómo activar iaRADAR en mi publicación?

iaRADAR Base está **incluido sin coste adicional** para todos los clientes de folioePress. iaRADAR PRO es un módulo de pago. Incluido sin coste en Planes superiores a partir de Dedicado PRO.

1. Accede al panel de control de tu publicación.
2. Ve a **Módulos → iaRADAR**.
3. Selecciona qué contenidos quieres distribuir a los modelos de IA.
4. Activa los bots IA que aceptas y bloquea los que no quieras.
5. Pulsa "Generar" y tu `llms.txt` quedará servido automáticamente en `tu-dominio.com/llms.txt`.

## ¿No eres cliente de folioePress?

Aunque iaRADAR es un módulo nativo de folioePress, este repositorio comparte plantillas y documentación que **puedes usar libremente** (licencia CC0) para implementar `llms.txt` en tu publicación con cualquier otra tecnología.

Si eres editor y te interesa folioePress como CMS profesional para tu medio digital:

- 📖 [Conocer folioePress](https://folioepress.com)
- 💡 [Qué es folioePress](https://folioepress.com/p/que-es-folioepress)
- 💬 [Demo gratuita de 15 días](https://folioepress.com/p/prueba-folioepress-gratis-version-totalmente-operativa-durante-15-dias)
- ✉️ [Contacto comercial](https://folioepress.com/p/recibir-informacion-sobre-proyectos-editoriales-periodicos-y-revistas-digitales)

## Sobre Foliogen Network

Este repositorio lo mantiene [Foliogen Network S.L.](https://foliogen.com), empresa española desarrolladora de **folioePress** desde 2008, con sede en Orihuela (Alicante).

- **Web:** https://foliogen.com
- **Foliogen en Wikidata:** [Q140008187](https://www.wikidata.org/wiki/Q140008187)
- **folioePress en Wikidata:** [Q140008258](https://www.wikidata.org/wiki/Q140008258)

## Licencia

Este repositorio se distribuye bajo licencia **CC0 1.0 Universal** (dominio público). Puedes usar las plantillas y la documentación libremente sin atribución.

`iaRADAR®`, `folioePress®` y `Foliogen®` son marcas registradas de Foliogen Network S.L.

---

<sub>Hecho con ❤️ en Orihuela, Alicante (España). Llevamos publicando digital desde antes de que existiera ChatGPT.</sub>
