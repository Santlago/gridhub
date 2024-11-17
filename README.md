# GridHub

GridHub is a innovative platform that connects microgrid owners with property owners, facilitating the deployment of sustainable energy solutions through a seamless space-leasing marketplace.

## 🌟 Features

### For Property Owners (Locators)
- List your properties with detailed energy-relevant specifications
- Interactive map integration via Google Maps API
- Receive and manage lease requests from microgrid owners
- Track installed microgrids and available space
- Multiple energy type support (solar, wind, combustion)

### For Microgrid Owners (Tenants)
- Register and manage your microgrid specifications
- Search available spaces with detailed energy-relevant information
- Submit lease requests with custom messages
- Monitor microgrid performance through:
  - Solar panel temperature
  - Energy generation metrics
  - Real-time performance tracking

### Investment Features
- Simple investment proposal submission system
- Direct connection between potential investors and microgrid owners
- Streamlined communication process

## 💫 Technical Overview

### Database Schema

The platform uses a relational database with the following structure:

```
USUARIO (User)
- usuario_id (PK)
- email
- senha
- nome
- telefone

ESPACO (Space)
- espaco_id (PK)
- usuario_id (FK)
- fonte_energia
- orientacao_solar
- media_solar
- topografia
- area_total
- direcao_vento
- velocidade_vento

MICROGRID
- microgrid_id (PK)
- usuario_id (FK)
- espaco_id (FK)
- radiacao_solar_necessaria
- topografia_necessaria
- area_total_necessaria
- velocidade_vento_necessaria
- fonte_energia
- meta_financiamento

INVESTIMENTO (Investment)
- investimento_id (PK)
- usuario_id (FK)
- microgrid_id (FK)
- descricao_proposta

RELATORIO (Report)
- relatorio_id (PK)
- microgrid_id (FK)
- energia_gerada
- temp_painel_solar
- lucro_gerado
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
