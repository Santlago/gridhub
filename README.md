# GridHub

GridHub is a innovative platform that connects microgrid owners with property owners, facilitating the deployment of sustainable energy solutions through a seamless space-leasing marketplace.

## 🌟 Features

### For Property Owners (Locators)
- Create a complete profile with photo and contact information
- List your properties with detailed specifications and photos
- Interactive map integration via Google Maps API
- Receive and manage lease requests from microgrid owners
- Track installed microgrids and available space
- Multiple energy type support (solar, wind, combustion)

### For Microgrid Owners (Tenants)
- Comprehensive profile management including profile picture
- Register and manage your microgrids with photos and specifications
- Search available spaces with detailed energy-relevant information
- Submit lease requests with custom messages
- Monitor microgrid performance through detailed reports

### Investment Features
- Simple investment proposal submission system
- Direct connection between potential investors and microgrid owners
- Streamlined communication process

## 💫 Technical Overview

### Database Schema

The platform uses a relational database with the following structure:

```
USUARIO (User)
- usuario_id (PK)      NUMERIC(5)
- email                VARCHAR(100)
- senha                VARCHAR(100)
- nome                 VARCHAR(100)
- telefone             VARCHAR(30)
- foto_perfil          VARCHAR(100)

ESPACO (Space)
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

INVESTIMENTO (Investment)
- investimento_id (PK) NUMERIC(5)
- usuario_id (FK)      NUMERIC(5)
- microgrid_id (FK)    NUMERIC(5)
- descricao_proposta   VARCHAR(512)

RELATORIO (Report)
- relatorio_id (PK)    NUMERIC(5)
- microgrid_id (FK)    NUMERIC(5)
- energia_gerada       VARCHAR(50)
- temp_painel_solar    VARCHAR(100)
- lucro_gerado         VARCHAR(100)
```

## 🚀 Getting Started

[Installation instructions to be added]

## 🤝 Contributing

We welcome contributions to GridHub! Please read our contributing guidelines before submitting pull requests.

## 📝 License

[License information to be added]

## 🔒 Security

All user data and transactions are handled securely. The platform focuses on connecting parties while keeping sensitive financial transactions off-platform.

## 📞 Contact

[Contact information to be added]

---
Built with ❤️ for a sustainable future
