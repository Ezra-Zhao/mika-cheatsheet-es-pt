# Mika · Guia rápido em português

Projeto original: [wangzan101/Mika](https://github.com/wangzan101/Mika) · [Español](README.es.md)

## O que é o Mika

Um agente de código aberto (Apache-2.0) que vive dentro do seu celular Android. Você diz o que precisa e ele abre apps, lê a tela, toca, digita e rola numa **tela de fundo oculta**, enquanto você continua usando o celular normalmente.

Não precisa de root nem de integração com cada app: ele não usa as APIs dos aplicativos, ele olha a tela e procura os botões como uma pessoa faria. E não existe um «servidor do Mika»: o que você diz e o que está na sua tela vai só para o provedor de modelos que você configurar.

O app já tem interface em português e espanhol, então este guia não traduz nada: ele te poupa dos tropeços de instalação, pareamento e permissões que o README em inglês e chinês não conta no seu idioma.

## Comece em três passos

1. **Instale**: baixe o APK em [Releases](https://github.com/wangzan101/Mika/releases/latest) do repositório original.
2. **Conecte um modelo**: em Configurações › Modelo, escolha um provedor e cole sua chave de API, **ou** entre com sua conta do ChatGPT, xAI ou OpenRouter, sem chave.
3. **Só se quiser que ele opere apps**: siga o assistente «Set up phone control» nas Configurações e pareie a depuração sem fio uma vez. Se você só quer chat, web e arquivos, pule este passo.

Primeiro teste razoável: «Coloca alarmes amanhã às 9:40 e às 10:00» ou «Olha o tempo todo dia às 8 e me avisa só se for chover».

## De que celular você precisa

| Uso | Requisito |
|---|---|
| Chat, web e arquivos | Android 11 ou posterior |
| Operar apps do celular | Android 12 ou posterior |
| Recomendado | **Android 14+**: a tela de fundo tem foco próprio e não atrapalha quando você digita na principal |
| Sandbox Linux (Python, Node, shell) | Só dispositivos arm64 |

Na dúvida se o seu celular aguenta? Em Configurações › Recovery & repair há uma **autoverificação de compatibilidade**: 12 checagens em cerca de um minuto.

## Dois modos: comece pelo Ask

| Modo | Comportamento |
|---|---|
| **Ask** (padrão) | Faz tudo sozinho e pergunta **só antes de gastar dinheiro** (fazer um pedido, pagar) |
| **Autonomous** | Executa sem perguntar nada |

O erro de iniciante é estrear o Autonomous no primeiro dia. Deixe no Ask até ver como ele trabalha nos seus apps.

## O que ele sabe fazer

- **Operar apps**: ler listas e históricos de conversa longos, tocar, digitar, compartilhar texto em apps.
- **Navegar na web**: navegador integrado que mantém sua sessão ativa, lê páginas, baixa e envia arquivos; se uma página o bloquear, ele passa para você.
- **Trabalhar sobre o que você está vendo**: toque duas vezes na cápsula flutuante e mande sua tela atual («como respondo isso?», «anota isso»).
- **Tarefas com horário e condições**: «me lembra amanhã às 9», «faz isso toda sexta».
- **Sandbox Linux por conversa**: roda Python, Node e shell sobre os arquivos que você passar.
- **Receber ordens do seu computador**: ferramentas de IA no seu PC podem passar tarefas por CLI + Skill ou por MCP.

## Apps com conhecimento integrado (úteis no Brasil e na América Latina)

O Mika funciona com qualquer app, mas traz conhecimento de uso pré-carregado para vários. Dos mais usados no Brasil e na região: **WhatsApp, Telegram, Uber, Uber Eats, Gmail, YouTube e Instagram** (o Instagram consta como site).

Detalhe honesto: esses arquivos de conhecimento estão escritos em chinês. Não te limita: o modelo lê sem problema e você fala com ele em português ou espanhol.

## Segurança e limites, sem letra miúda escondida

- **Pagamentos, senhas e códigos de verificação**: essas telas bloqueiam a captura, então o Mika não consegue lê-las e devolve o controle para você. É por design, não é defeito.
- **Termos de serviço**: automatizar apps e sites de terceiros pode ir contra as condições de uso deles. Bom senso: para coisas importantes, modo Ask e confira o resultado.
- **A depuração sem fio desliga sozinha** ao trocar de Wi-Fi ou reiniciar o celular. Com sua permissão, o Mika a reativa sozinho; se mesmo assim não conectar, volte ao «Set up phone control» e pareie de novo.
- **Sem servidor próprio**: chaves de API e memórias ficam criptografadas no celular; conversas e registros não saem do aparelho, e as verificações de atualização só falam com o GitHub.
- Algumas marcas cortam a depuração sem fio do sistema; nesse caso, o assistente pode ser iniciado de um computador via USB (guia de instalação do repo original).

## Links

- Repositório: https://github.com/wangzan101/Mika
- Download (APK): https://github.com/wangzan101/Mika/releases/latest
- Guia de instalação do controle do celular: https://github.com/wangzan101/Mika/blob/main/docs/setup-guide.en.md

---

Guía elaborada a partir de la documentación oficial del proyecto · Guia elaborada a partir da documentação oficial do projeto. El software pertenece a sus autores · O software pertence aos seus autores.

Licencias: Mika es Apache-2.0; esta guía se publica bajo licencia MIT. · Licenças: o Mika é Apache-2.0; este guia é publicado sob a licença MIT.
