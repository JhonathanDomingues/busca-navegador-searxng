# SearXNG - Instância Local

Instância privada do [SearXNG](https://github.com/searxng/searxng), um metabuscador open-source que agrega resultados de múltiplos motores de busca sem rastrear os usuários.

## Requisitos

- Docker
- Docker Compose

## Como usar

### Subir a instância

```bash
docker compose up -d
```

### Parar a instância

```bash
docker compose down
```

### Ver logs

```bash
docker compose logs -f
```

### Acessar

Após iniciar, acesse: [http://localhost:8080](http://localhost:8080)

## Configuração

As configurações estão em `searxng/settings.yml`. Os principais ajustes feitos nesta instância:

- **Motores ativos**: Google, DuckDuckGo, Bing, GitHub, Stack Overflow, Wikipedia
- **Formato de saída**: HTML e JSON
- **Bind**: `0.0.0.0:8080` (acessível na rede local)
- **Rate limiter**: desativado (uso privado)

## Estrutura

```
.
├── docker-compose.yml      # Definição do serviço Docker
├── settings.yml            # Configurações gerais (raiz)
└── searxng/
    └── settings.yml        # Configurações da instância SearXNG
```
