# Reddit

## Descrição

O Reddit é uma rede social e fórum de discussão organizado em milhares de comunidades independentes chamadas **subreddits** (ex: r/brasil, r/gaming, r/worldnews). Fundado em 2005, o Reddit se descreve oficialmente como "uma comunidade de comunidades", construída em torno de interesses, paixões e confiança compartilhados entre os usuários.

Dentro de cada subreddit, os usuários publicam conteúdo (texto, links, imagens, vídeos) que pode ser votado positivamente (*upvote*) ou negativamente (*downvote*) pelos demais membros, o que determina sua visibilidade e posição no feed. Cada publicação também pode receber comentários organizados em formato de discussão em árvore (threads aninhadas).

O Reddit deve ser utilizado quando alguém quer encontrar discussões aprofundadas sobre um assunto específico, buscar recomendações e opiniões de outras pessoas, acompanhar notícias filtradas por comunidades de interesse ou participar de debates moderados por voluntários dentro de cada subreddit.

## Público-alvo

- Pessoas interessadas em discussões aprofundadas sobre hobbies, notícias ou nichos específicos;
- Usuários que buscam recomendações, opiniões e experiências de terceiros antes de tomar decisões (compras, viagens, carreira);
- Comunidades de jogos, tecnologia, ciência, entretenimento e cultura pop;
- Criadores de conteúdo que quiram engajar com públicos segmentados por interesse;
- Moderadores voluntários que administram e mantêm regras em suas próprias comunidades;
- Anunciantes que buscam públicos altamente segmentados por tema.

## Funcionalidades

- Criação e participação em comunidades (subreddits) sobre qualquer assunto;
- Publicação de posts em texto, link, imagem, vídeo ou enquete (poll);
- Sistema de votos (upvote/downvote) que define a relevância do conteúdo;
- Comentários organizados em threads aninhadas, também votáveis;
- Mensagens diretas e chats entre usuários;
- Ferramentas de moderação para donos e moderadores de subreddits (regras próprias, remoção de posts, AutoModerator);
- Sistema de "prêmios" (awards) que os usuários podem dar a posts e comentários;
- Busca de posts, comunidades e usuários dentro da plataforma;
- Perfil de usuário com histórico de posts, comentários e karma (pontuação de reputação);
- Reddit Premium: assinatura paga que remove anúncios e concede benefícios extras;
- Navegação anônima (sem login) para leitura de conteúdo público em diversas regiões.

## Tecnologias utilizadas

### Backend
- **Python**: linguagem original do Reddit, ainda usada em partes do sistema;
- **Go**: linguagem para a qual o Reddit vem migrando serviços centrais de alto tráfego (Comentários, Contas, Posts e Subreddits foram migrados de um monólito em Python para microsserviços em Go, conforme detalhado no próprio blog de engenharia do Reddit);
- **PostgreSQL**: principal banco de dados relacional, usado para persistência de dados (incluindo AWS Aurora Postgres como armazenamento unificado de metadados de mídia);
- **Cassandra**: banco de dados NoSQL usado historicamente para armazenamento distribuído em grande escala;
- **Redis**: usado para cache e captura de eventos de mudança de dados (*change data capture*);
- **Memcached**: usado como camada adicional de cache;
- **Kafka**: usado para processamento de mensagens e streams de dados entre serviços.

### Infraestrutura e operação
- **AWS S3**: armazenamento de arquivos e mídia;
- **Docker e Kubernetes**: containerização e orquestração dos serviços;
- **Prometheus e Grafana**: monitoramento e visualização de métricas do sistema.

### Clientes (aplicativos e site)
- **React**: usado no frontend do site (reddit.com);
- **Kotlin** com **Jetpack Compose**: usado no aplicativo nativo para Android;
- **Swift** com **SwiftUI**: usado no aplicativo nativo para iOS.

## Requisitos técnicos para utilização

### Aplicativo mobile (segundo o suporte oficial do Reddit)
- **Android**: versão mínima Android OS 10, com o aplicativo atualizado para a versão 2026.10 ou superior;
- **iOS**: versão mínima iOS 16, com o aplicativo atualizado para a versão 2025.33 ou superior.

### Site (versão web)
- Navegador atualizado (Chrome, Firefox, Edge, Safari ou similar);
- Conexão com a internet ativa.

### Geral
- Conta gratuita no Reddit para publicar, comentar, votar ou enviar mensagens (a leitura pública de conteúdo pode ser feita sem login em diversas regiões);
- Assinatura Reddit Premium é opcional, para remover anúncios e obter benefícios extras.

## Desenvolvedores


- [Victor Rigonati Barbaresco]
- [Roger Carvalho Mantovani]
- [Thiago Rafael Alves Dos Santos Junior]
- [Leonardo Aparecido Rezende Bispo]
- [Bruno Silva Moura]

## Fontes

- [Reddit Help – Android & iOS minimum supported OS and app versions](https://support.reddithelp.com/hc/en-us/articles/26843930661780-Android-iOS-minimum-supported-OS-and-app-versions)
- [InfoQ – Reddit Migrates Comment Backend from Python to Go Microservice to Halve Latency (baseado em post oficial do blog de engenharia do Reddit)](https://www.infoq.com/news/2025/11/reddit-comments-go-migration/)
- [The Pragmatic Engineer – Building Reddit's iOS and Android app (entrevista com engenheiros do Reddit)](https://newsletter.pragmaticengineer.com/p/building-reddits-ios-and-android)
- [Vagas oficiais de engenharia do Reddit – redditinc.com / Built In](https://builtin.com/job/staff-software-engineer-storage/8113287)
- [Scale Engineer – How Reddit designed their Metadata Store to serve 100k req/sec](https://scaleengineer.com/blog/how-reddit-designed-their-metadata-store-to-serve-100k-req-sec)
