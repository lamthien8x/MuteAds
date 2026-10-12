<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logotipo de MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Silencia los anuncios y rastreadores en tu teléfono, ordenador y navegador.<br>Un solo interruptor, cinco niveles de filtrado, sin cuentas, 100% en tu dispositivo.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <b>Español</b> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## ¿Por qué creamos MuteAds?

Al igual que tú, estábamos hartos del internet actual: banners parpadeantes que invaden la pantalla, scripts de rastreo que vigilan cada clic, baterías que se agotan a media tarde y bloqueadores pesados que ralentizan el equipo o terminan vendiéndose a las agencias de publicidad. Creamos MuteAds con un objetivo claro: cortar de raíz los anuncios y rastreadores impidiendo la conexión a sus dominios antes de que lleguen a tu pantalla.

Sin necesidad de root. Sin cuentas ni registros. Y lo más importante: **ni un solo byte de tu actividad de navegación sale de tu dispositivo**. Todo el filtrado se resuelve localmente en tu propio hardware.

- **Bloqueo por dominio que funciona**: Detiene anuncios y analíticas intrusivas en todas las aplicaciones del sistema (Android, PC/Mac) o directamente dentro de tu navegador (extensión).
- **5 niveles de filtrado flexibles**: Desde el nivel "Básico" (ultraseguro, no rompe portales de trabajo) hasta "Máximo" (escudo de privacidad total). El nivel 3 es nuestro valor predeterminado recomendado.
- **Bloqueo de anuncios de YouTube integrado**: Incluido en la extensión del navegador. Enciende el interruptor y disfruta de tus vídeos sin interrupciones molestas.
- **Un único interruptor maestro**: La vida ya es bastante complicada. ¿Necesitas pausar el filtrado un momento para probar algo? Un clic lo desactiva y todo vuelve a la normalidad de inmediato.
- **DNS cifrado moderno**: Soporte nativo para DNS-over-HTTPS (DoH) y DNS-over-TLS (DoT) en Android y escritorio, protegiendo tus consultas de miradas indiscretas de proveedores de internet.
- **Control total de reglas**: Añade tus propias listas de permisos (allowlist), listas de bloqueo (blocklist) y mapeos de IP personalizados, con comodines `*`.

## Descargas y estado del proyecto

> MuteAds se encuentra en fase de lanzamiento temprano (versión 0.1). Estamos afinando detalles y preparando la llegada a las tiendas oficiales. Mientras tanto, puedes descargar los instaladores directos en la página de [Releases](../../releases).

| Plataforma | Cómo funciona por dentro | Estado |
| --- | --- | --- |
| **Android** | VPN local que filtra el DNS en el propio dispositivo. Sin root. Android 4.2+ | APK en [Releases](../../releases) |
| **Windows** | Filtro DNS local para todo el sistema (x64, ARM64) | Disponible en [Releases](../../releases) |
| **macOS** | Filtro DNS local para todo el sistema operativo | Disponible en [Releases](../../releases) |
| **Linux** | Proxy DNS independiente para un equipo o toda la red local (requiere Java) | Disponible en [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Extensión de navegador MV3 ultraligera y eficiente | Preparando publicación en la tienda |
| **Firefox 128+** | Extensión declarativa rápida y moderna | Preparando publicación en los complementos |

## Niveles de filtrado

| Nivel | Perfil | Qué se bloquea |
| --- | --- | --- |
| 1 | Básico (Basic) | Solo redes de anuncios y rastreo de máxima prioridad. Mínimo riesgo de falsos positivos. |
| 2 | Equilibrado (Balanced) | Mayor cobertura, incluyendo plataformas de analítica y telemetría comunes. |
| 3 | Extendido (Extended) | Bloqueo amplio ideal para el uso diario. **Recomendado por defecto.** |
| 4 | Estricto (Strict) | Filtrado agresivo. Puede interferir ocasionalmente con widgets o comentarios externos. |
| 5 | Máximo (Maximum) | Aplica toda la lista de bloqueo excepto redes sociales esenciales. Algunas páginas complejas pueden requerir excepciones. |

💡 **Consejo de desarrollador:** Si un sitio web no carga correctamente, simplemente baja el filtro un nivel o apaga el interruptor durante unos segundos.

## Cómo funciona (¡Sin trucos de magia!)

Cada vez que una aplicación o página web intenta cargar contenido, primero debe consultar qué dirección IP corresponde al nombre de dominio (mediante una consulta DNS). MuteAds actúa como tu guardián local:

- Si el dominio pertenece a una red de publicidad o rastreo, MuteAds responde al instante: *"No existe (NXDOMAIN)"*. La conexión jamás llega a establecerse, ahorrando datos móviles y batería.
- Si se trata de contenido legítimo que deseas ver, la consulta pasa sin demoras a los servidores DNS tradicionales y la página carga a toda velocidad.

En Android, esto se realiza mediante una **VPN local de bucle invertido** que jamás envía tráfico fuera de tu teléfono. En el ordenador, MuteAds se convierte en el servidor DNS local de tu máquina. En navegadores, la extensión aprovecha la rapidísima API nativa `declarativeNetRequest`.

## Privacidad real: No queremos tus datos

- **Sin cuentas ni registros**: No tenemos formularios de suscripción ni bases de datos de usuarios.
- **100% en tu dispositivo**: El filtrado ocurre íntegramente en tu máquina. No tenemos servidores intermediarios que espíen tus hábitos de navegación.
- **Actualizaciones limpias**: La única conexión periódica que hace la app es para descargar listas de dominios actualizadas aproximadamente una vez por semana.
- **Permisos mínimos**: La extensión solo solicita lo estrictamente necesario: bloquear peticiones, guardar tus preferencias, la alarma de actualización semanal y acceso a `youtube.com`.

## Cosas útiles que debes saber

- **En Android:** Recuerda desactivar *DNS Privado* en los ajustes de red de tu teléfono, ya que de lo contrario Android omitirá el filtro local. Desactiva también la optimización agresiva de batería.
- **Anuncios del mismo dominio:** El bloqueo DNS puro no puede filtrar anuncios alojados en el mismo dominio que el contenido principal. Por esa razón, nuestra extensión de navegador incorpora un motor específico para YouTube.
- **El juego del gato y el ratón en YouTube:** Las plataformas de vídeo modifican sus sistemas de anuncios con frecuencia. Si un anuncio llega a colarse, asegúrate de actualizar la extensión a la última versión.

## Comentarios y comunidad

¿Encontraste una página rota o un anuncio que logró colarse? Abre un [Issue](../../issues) indicando la dirección de la página y el nivel de filtrado que tenías activo. ¡Leemos cada comentario y agradecemos mucho tu apoyo!

## Licencia y créditos

La aplicación de Android y el proxy DNS independiente se basan en el formidable proyecto de código abierto [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) de Ingo Zenz, publicado bajo la licencia GNU General Public License v2 o posterior. Desarrollado con cariño para un internet más limpio.
