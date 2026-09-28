# TSEA Vacuum Regulator MES

Manufacturing Execution System (MES) para gestão do processo de vácuo, teste de estanqueidade e enchimento de reguladores conforme relatório técnico TSEA Energia.

## 📋 Arquitetura

- **Backend**: C# .NET 7+ (API REST + gRPC)
- **Frontend**: React 18 + TypeScript
- **Banco de Dados**: SQL Server / PostgreSQL
- **Mensageria**: RabbitMQ / MQTT
- **Autenticação**: JWT + OAuth2
- **Logging**: Serilog
- **Monitoramento**: Prometheus + Grafana

## 🎯 Funcionalidades Principais

### Gestão de Ciclos de Produção
- Preparação e validação de reguladores
- Controle de evacuação (desbaste → vácuo intermediário → vácuo final)
- Teste de subida de pressão (rate-of-rise)
- Enchimento sob vácuo
- Quebra de vácuo e liberação

### Regras de Negócio (RN01-RN10)
- RN01: Identificação obrigatória
- RN02: Validação de receita
- RN03: Verificação de calibração
- RN04: Segurança mecânica
- RN05: Qualidade do vácuo
- RN06: Teste de estanqueidade
- RN07: Limites de temperatura
- RN08: Integridade de lote (hash)
- RN09: Audit trail
- RN10: Resiliência

### Monitoramento e Analytics
- Dashboard em tempo real
- Gráficos de pressão, temperatura e fluxo
- KPIs: OEE, Yield Rate, Variação Padrão
- Relatórios de qualidade
- Manutenção preditiva

## 📊 Parâmetros Operacionais

| Parâmetro | Valor | Classificação |
|-----------|-------|----------------|
| Produção anual | 3.500 reguladores/ano | Público-TSEA |
| Dias úteis | 250 dias/ano | Hipótese |
| Volume do tanque | 1,5 m³ | Hipótese |
| Velocidade da bomba | 100 m³/h | Hipótese |
| Duração do ciclo | 8 h | Hipótese |
| Temp. do óleo | 50–60 °C | Prática de mercado |

## ⚖️ Conformidade

- ✅ NR-12: Segurança em Máquinas
- ✅ NR-10: Segurança Elétrica
- ✅ NR-13: Vasos de Pressão
- ✅ NR-33: Espaços Confinados
- ✅ ISO 13849-1 / IEC 62061
- ✅ ISO 9001, 14001, 45001
