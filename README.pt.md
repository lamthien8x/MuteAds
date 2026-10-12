<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logotipo do MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Silencie anúncios e rastreadores no seu celular, computador e navegador.<br>Um único botão, cinco níveis de filtro, sem contas, 100% no seu dispositivo.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <b>Português</b> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Por que criamos o MuteAds

Assim como você, estávamos cansados da internet moderna: anúncios piscando por todos os lados, rastreadores monitorando cada clique, bateria descarregando sem parar e bloqueadores pesados que deixam o sistema lento ou vendem dados para terceiros. Criamos o MuteAds com um único propósito: eliminar anúncios e rastreadores pela raiz, recusando conexões para seus domínios antes mesmo de chegarem à sua tela.

Sem root. Sem cadastro ou contas. E o mais importante: **nem um único byte da sua navegação sai do seu aparelho**. Toda a filtragem acontece 100% no seu próprio hardware.

- **Bloqueio por domínio que funciona de verdade**: Impede anúncios e coletas invasivas em todos os aplicativos do sistema (Android, PC/Mac) ou direto no navegador (extensão).
- **5 níveis de filtragem inteligentes**: Do nível "Básico" (ultrasse seguro, não quebra sites bancários ou de trabalho) ao "Máximo" (escudo de privacidade rígido). O nível 3 é nosso padrão equilibrado.
- **Bloqueio nativo de anúncios do YouTube**: Integrado na extensão de navegador. Ative o botão e assista aos seus vídeos sem interrupções indesejadas.
- **Um botão liga/desliga central**: A vida já tem configurações demais. Precisa pausar o filtro para testar algo? Um clique desliga tudo e tudo volta ao normal instantaneamente.
- **DNS criptografado moderno**: Suporte completo a DNS-over-HTTPS (DoH) e DNS-over-TLS (DoT) no Android e computador para impedir espionagem do seu provedor de internet.
- **Controle total das regras**: Crie suas próprias listas de permissão (allowlist), listas de bloqueio (blocklist) e redirecionamentos de IP personalizados com suporte a curingas `*`.

## Downloads e Versões

> O MuteAds está em fase de lançamento inicial (v0.1). Estamos trabalhando na publicação nas lojas oficiais. Enquanto isso, os instaladores diretos estão disponíveis na página de [Releases](../../releases).

| Plataforma | Funcionamento interno | Status |
| --- | --- | --- |
| **Android** | VPN local em loopback que filtra o DNS no próprio aparelho. Sem root. Android 4.2+ | APK em [Releases](../../releases) |
| **Windows** | Filtro DNS local para todo o computador (x64, ARM64) | Disponível em [Releases](../../releases) |
| **macOS** | Filtro DNS local para todo o sistema Mac | Disponível em [Releases](../../releases) |
| **Linux** | Proxy DNS independente para uma máquina ou toda a rede local (requer Java) | Disponível em [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Extensão de navegador MV3 ultraleve e de alto desempenho | Preparando envio para a loja |
| **Firefox 128+** | Extensão declarativa moderna e rápida | Preparando envio para a loja |

## Níveis de Filtragem

| Nível | Perfil | O que é bloqueado |
| --- | --- | --- |
| 1 | Básico (Basic) | Apenas servidores de publicidade e rastreamento de prioridade crítica. Mínimo risco de falsos positivos. |
| 2 | Equilibrado (Balanced) | Cobertura mais ampla incluindo analíticas comuns de telemetria. |
| 3 | Estendido (Extended) | Proteção robusta e abrangente para o uso diário. **Padrão recomendado.** |
| 4 | Estrito (Strict) | Filtragem agressiva. Pode eventualmente afetar widgets de terceiros incorporados. |
| 5 | Máximo (Maximum) | Aplica a lista completa exceto redes sociais essenciais. Alguns sites específicos podem necessitar de liberação. |

💡 **Dica do desenvolvedor:** Se uma página apresentar problemas de carregamento, basta reduzir o filtro em um nível ou desativar o botão momentaneamente.

## Como funciona (Sem truques de mágica!)

Toda vez que um aplicativo ou página quer carregar algo na rede, primeiro precisa descobrir o endereço IP daquele domínio (via consulta DNS). O MuteAds funciona como seu porteiro particular:

- Se o domínio pertencer a uma rede de anúncios ou rastreadores, o MuteAds responde imediatamente: *"Inexistente (NXDOMAIN)"*. A conexão nunca acontece, economizando seu pacote de dados e a bateria.
- Se for o conteúdo legítimo que você realmente pediu, a consulta é encaminhada normalmente aos servidores DNS padrão e a página abre com velocidade máxima.

No Android, isso roda através de uma **VPN local em loopback** que nunca envia dados para servidores externos. No computador, o app se torna o servidor DNS local da sua máquina. No navegador, a extensão aproveita a API oficial de altíssima velocidade `declarativeNetRequest`.

## Privacidade em primeiro lugar: Seus dados não nos interessam

- **Sem contas, sem login**: Não possuímos formulários de cadastro e nenhum banco de dados central de usuários.
- **100% no seu dispositivo**: A filtragem acontece exclusivamente no seu aparelho. Não possuímos servidores intermediários bisbilhotando sua navegação.
- **Atualizações transparentes**: A única conexão periódica que o app faz é o download automático das listas de bloqueio atualizadas aproximadamente uma vez por semana.
- **Permissões mínimas**: A extensão solicita apenas o que é estritamente indispensável para filtrar requisições, salvar opções, agendar atualizações semanais e operar no `youtube.com`.

## Dicas importantes

- **Usuários de Android:** Desative a opção de *DNS Privado* nas configurações de rede do seu celular, caso contrário o Android ignorará a filtragem local. Desative também a otimização de bateria para o app.
- **Anúncios hospedados no próprio domínio:** O bloqueio por DNS não consegue impedir anúncios entregues pelo mesmo domínio do conteúdo principal. É por isso que nossa extensão inclui um motor exclusivo dedicado ao YouTube.
- **O jogo de gato e rato no YouTube:** Plataformas de vídeo alteram seus scripts com frequência. Se algum anúncio escapar, certifique-se de atualizar a extensão para a versão mais recente.

## Comentários e Comunidade

Encontrou uma página com falha ou um anúncio insistente que passou despercebido? Abra uma [Issue](../../issues) informando o endereço da página e o nível de filtro utilizado. Seu feedback faz toda a diferença para o projeto!

## Licença e Créditos

O aplicativo Android e o proxy DNS independente são construídos sobre a excelente base open source [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) de Ingo Zenz, distribuída sob a GNU General Public License v2 ou posterior. Criado com dedicação por uma internet mais livre.
