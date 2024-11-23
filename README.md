# GridHub

## Itens de Entrega
- Código fonte (frontend): https://github.com/Santlago/webgridhub
- Código fonte (backend): https://github.com/Santlago/apigridhub
- Deploy em nuvem (frontend): http://webgridhub.vercel.app
- Deploy em nuvem (backend): http://gridhub.railway.app
- Vídeo pitch: https://youtu.be/tdruTbBAiNg
- Vídeo demonstrativo do site: https://youtu.be/tdruTbBAiNg

## Integrantes

- Breno Lemes Santiago - RM: 552270
- Felipe Guedes Gonçalves - RM: 550906
- Luiz Felipe Soares de Sousa Lucena - RM: 551365
- Nina Rebello Francisco - RM: 99509
- Vitória Maria de Camargo - RM: 552344

**O GridHub é uma plataforma inovadora que conecta proprietários de microgrids com donos de imóveis, facilitando a implementação de soluções de energia sustentável através de um marketplace intuitivo para locação de espaços.**

## ✨ Funcionalidades

### Para Proprietários de Imóveis (Locadores)
- Criação de perfil completo com foto e informações de contato
- Cadastro de propriedades com especificações detalhadas e fotos
- Integração com mapa interativo via API do Google Maps
- Recebimento e gestão de solicitações de locação dos proprietários de microgrids
- Acompanhamento de microgrids instaladas e espaço disponível
- Suporte a múltiplos tipos de energia (solar, eólica, combustão)

### Para Proprietários de Microgrids (Locatários)
- Gerenciamento completo de perfil incluindo foto
- Cadastro e gestão de suas microgrids com fotos e especificações
- Busca de espaços disponíveis com informações detalhadas relevantes para energia
- Envio de solicitações de locação com mensagens personalizadas
- Monitoramento do desempenho das microgrids através de relatórios detalhados

### Funcionalidades de Investimento
- Sistema simplificado de envio de propostas de investimento
- Conexão direta entre potenciais investidores e proprietários de microgrids
- Processo de comunicação otimizado

## 🔧 Visão Técnica

### Esquema do Banco de Dados
A plataforma utiliza um banco de dados relacional com a seguinte estrutura:

```
USUARIO
- usuario_id (PK)      NUMERIC(5)
- email                VARCHAR(100)
- senha                VARCHAR(100)
- nome                 VARCHAR(100)
- telefone             VARCHAR(30)
- foto_perfil          VARCHAR(100)

ESPACO
- espaco_id (PK)      NUMERIC(5)
- usuario_id (FK)      NUMERIC(5)
- endereco             VARCHAR(200)
- nome_espaco          VARCHAR(100)
- foto_espaco          VARCHAR(100)
- fonte_energia        VARCHAR(20)
- orientacao_solar     VARCHAR(30)
- media_solar          VARCHAR(100)
- topografia           VARCHAR(100)
- area_total           VARCHAR(100)
- direcao_vento        VARCHAR(100)
- velocidade_vento     VARCHAR(100)

MICROGRID
- microgrid_id (PK)   NUMERIC(5)
- usuario_id (FK)      NUMERIC(5)
- espaco_id (FK)       NUMERIC(5)
- nome_microgrid       VARCHAR(100)
- foto_microgrid       VARCHAR(100)
- radiacao_solar_necessaria    VARCHAR(100)
- topografia_necessaria        VARCHAR(100)
- area_total_necessaria        NUMERIC(20)
- velocidade_vento_necessaria  VARCHAR(100)
- fonte_energia                VARCHAR(20)
- meta_financiamento          NUMERIC(20)

INVESTIMENTO
- investimento_id (PK) NUMERIC(5)
- usuario_id (FK)      NUMERIC(5)
- microgrid_id (FK)    NUMERIC(5)
- descricao_proposta   VARCHAR(512)

RELATORIO
- relatorio_id (PK)    NUMERIC(5)
- microgrid_id (FK)    NUMERIC(5)
- energia_gerada       VARCHAR(50)
- temp_painel_solar    VARCHAR(100)
- lucro_gerado         VARCHAR(100)
```

## 🚀 Como Começar
[Instruções de instalação serão adicionadas]

## 🤝 Como Contribuir
Contribuições para o GridHub são bem-vindas! Por favor, leia nossas diretrizes de contribuição antes de enviar pull requests.

## 📝 Licença
[Informações sobre a licença serão adicionadas]

## 🔒 Segurança
Todos os dados dos usuários e transações são tratados de forma segura. A plataforma concentra-se em conectar as partes mantendo transações financeiras sensíveis fora da plataforma.

## 📞 Contato
[Informações de contato serão adicionadas]

---
Construído com ❤️ para um futuro sustentável
