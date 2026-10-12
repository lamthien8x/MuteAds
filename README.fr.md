<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Faites taire les pubs et les traqueurs sur votre téléphone, votre PC et votre navigateur.<br>Un interrupteur unique, cinq niveaux de filtrage, sans compte, 100% local.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <b>Français</b><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Pourquoi nous avons créé MuteAds

Tout comme vous, nous en avions assez de l'internet d'aujourd'hui : des bannières agressives qui clignotent partout, des scripts espions qui surveillent le moindre clic, une batterie qui fond à vue d'œil et des bloqueurs lourds qui ralentissent la machine ou finissent par revendre vos données. Nous avons conçu MuteAds avec un principe fondamental : couper net les pubs et traqueurs à la racine en refusant toute connexion à leurs serveurs avant même qu'ils n'atteignent votre écran.

Pas besoin de root. Pas de compte ni d'inscription. Et surtout : **pas un seul octet de votre historique de navigation ne quitte votre appareil**. Tout le filtrage est exécuté localement sur votre propre matériel.

- **Blocage par nom de domaine redoutable** : Fonctionne sur toutes les applications du système (Android, ordinateur) ou directement au cœur de votre navigateur (extension).
- **5 niveaux de filtrage sur mesure** : Du mode « Basique » (hyper sûr, ne casse pas les sites professionnels) au mode « Maximum » (bouclier total). Le niveau 3 est le réglage par défaut idéal.
- **Blocage des publicités YouTube intégré** : Inclus directement dans l'extension de navigateur. Activez l'interrupteur et profitez de vos vidéos sans coupures intempestives.
- **Un interrupteur unique** : La vie est déjà assez compliquée. Besoin de désactiver le filtre quelques instants pour un test ? Un clic suffit, tout revient instantanément à la normale.
- **DNS chiffré moderne** : Prise en charge native du DNS-over-HTTPS (DoH) et DNS-over-TLS (DoT) sur Android et PC pour protéger vos requêtes des FAI et réseaux Wi-Fi publics.
- **Contrôle absolu des règles** : Listes blanches (allowlist), listes noires (blocklist) et correspondances IP personnalisées avec jokers `*`.

## Téléchargements & Versions

> MuteAds est actuellement en version préliminaire (v0.1). Nous peaufinons les versions et préparons la publication sur les stores officiels. En attendant, les installateurs sont directement disponibles sur la page [Releases](../../releases).

| Plateforme | Fonctionnement interne | Statut |
| --- | --- | --- |
| **Android** | VPN local en boucle qui filtre le DNS directement sur l'appareil. Sans root. Android 4.2+ | APK direct sur [Releases](../../releases) |
| **Windows** | Service de filtrage DNS local pour tout l'ordinateur (x64, ARM64) | Disponible sur [Releases](../../releases) |
| **macOS** | Filtre DNS local pour l'ensemble du système Mac | Disponible sur [Releases](../../releases) |
| **Linux** | Proxy DNS autonome pour un poste ou tout le réseau local (nécessite Java) | Disponible sur [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Extension de navigateur MV3 légère et ultra rapide | Publication sur le store en préparation |
| **Firefox 128+** | Extension déclarative moderne et efficace | Publication sur les modules en préparation |

## Niveaux de filtrage

| Niveau | Profil | Ce qui est bloqué |
| --- | --- | --- |
| 1 | Basique (Basic) | Uniquement les réseaux de pubs et de pistage prioritaires. Risque quasi nul de faux positifs. |
| 2 | Équilibré (Balanced) | Couverture élargie incluant les plateformes d'analyse et de télémétrie courantes. |
| 3 | Étendu (Extended) | Protection complète pour la navigation quotidienne. **Recommandé par défaut.** |
| 4 | Strict (Strict) | Filtrage agressif. Peut parfois bloquer certains widgets tiers intégrés. |
| 5 | Maximum (Maximum) | Toute la liste sauf les réseaux sociaux indispensables. Certains sites complexes peuvent nécessiter une exception. |

💡 **Astuce de dev :** Si un site fonctionne mal, baissez simplement le niveau d'un cran ou coupez l'interrupteur un court instant.

## Comment ça marche (Sans tour de magie !)

Chaque fois qu'une application ou une page web souhaite charger un élément, elle doit d'abord demander l'adresse IP associée au nom de domaine (via une requête DNS). MuteAds agit comme votre vigile local :

- Si le domaine appartient à une régie publicitaire ou un traqueur, MuteAds répond aussitôt : *« Inexistant (NXDOMAIN) »*. La connexion n'est jamais établie, ce qui économise forfait de données et batterie.
- S'il s'agit du contenu légitime que vous voulez consulter, la requête est transmise sans encombre à votre serveur DNS habituel et la page s'affiche à pleine vitesse.

Sur Android, cela repose sur un **VPN local** qui ne sort jamais de votre smartphone. Sur ordinateur, MuteAds devient le résolveur DNS local de votre machine. Dans le navigateur, l'extension utilise le moteur ultra performant `declarativeNetRequest`.

## Vie privée : Vos données ne nous intéressent pas

- **Aucun compte, aucune inscription** : Nous n'avons aucun formulaire de collecte ni base de données utilisateurs.
- **100% sur votre appareil** : Le filtrage est exclusivement local. Nous n'exploitons aucun serveur voyeur capable de tracer votre navigation.
- **Mises à jour transparentes** : La seule activité réseau automatique de l'application est la récupération hebdomadaire de la liste actualisée des domaines indésirables.
- **Permissions minimales** : L'extension demande uniquement ce qui est strictement nécessaire : bloquer les requêtes, sauvegarder vos options, planifier le rafraîchissement hebdomadaire et gérer `youtube.com`.

## Bon à savoir

- **Sur Android :** Désactivez impérativement le *DNS privé* dans les réglages réseau de votre téléphone, sinon Android contournera le filtrage local. Pensez aussi à désactiver l'optimisation agressive de batterie.
- **Publicités hébergées en local (first-party) :** Le filtrage DNS pur ne peut pas bloquer les pubs servies directement depuis le même domaine que le contenu principal. C'est pourquoi notre extension intègre un module dédié pour YouTube.
- **Le jeu du chat et de la souris sur YouTube :** Les plateformes vidéo font évoluer leurs scripts publicitaires en permanence. Si une pub réapparaît, pensez à mettre à jour l'extension vers la dernière version.

## Retours & Communauté

Un site mal affiché ou une pub tenace qui s'est faufilée ? N'hésitez pas à ouvrir une [Issue](../../issues) avec l'adresse de la page et le niveau de filtrage utilisé. Chaque retour compte énormément pour nous !

## Licence & Remerciements

L'application Android et le proxy DNS autonome s'appuient sur l'excellent projet open source [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) d'Ingo Zenz, publié sous licence GNU General Public License v2 ou supérieure. Distribué avec passion pour un web plus sain et plus libre.
