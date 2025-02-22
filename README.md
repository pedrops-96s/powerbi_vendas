# 📊 Power BI - Dashboard de Vendas

## 📌 Visão Geral
Este repositório contém um projeto de **Power BI** voltado para análise de vendas. O dashboard foi desenvolvido para fornecer insights sobre o desempenho comercial, permitindo a análise de métricas como **receita, custos, margem de lucro e desempenho por produto, vendedor e supervisor**.

## 🔧 Tecnologias Utilizadas
- **Power BI** - Para visualização e análise de dados
- **DAX (Data Analysis Expressions)** - Para criação de métricas e cálculos
- **Power Query** - Para transformação e tratamento de dados
- **Excel** - Fonte de dados original
- **GitHub** - Para versionamento e documentação do projeto

## 📂 Estrutura do Projeto

- **/data** - Contém os arquivos de dados utilizados (se aplicável)
- **/reports** - Arquivo `.pbix` do dashboard
- **/docs** - Documentação e guias
- `README.md` - Descrição do projeto

## 📊 Dados Utilizados
O projeto utiliza dois datasets principais:

### **1. Produto**
| Campo         | Descrição                                    |
|--------------|--------------------------------------------|
| Cod Produto  | Código único do produto                    |
| Grupo Produto | Categoria do produto                      |
| Linha Produto | Linha específica dentro do grupo          |
| Fornecedor   | Nome do fornecedor                         |
| Custo Unitário | Custo do produto                         |

### **2. Vendas**
| Campo         | Descrição                                    |
|--------------|--------------------------------------------|
| Data         | Data da venda                               |
| Nota Fiscal  | Número da nota fiscal                      |
| cdProduto    | Código do produto vendido                  |
| cdVendedor  | Código do vendedor responsável              |
| Vendedor     | Nome do vendedor                           |
| Supervisor   | Nome do supervisor do vendedor             |
| Quantidade   | Quantidade vendida                         |
| Valor Unitário | Preço unitário na venda                  |
| Receita      | Valor total da venda                       |

## 🔗 Relacionamento dos Dados
- **Produto [Cod Produto] (Chave Primária) ↔ Vendas [cdProduto] (Chave Estrangeira)** (Relacionamento 1:N)

## 📈 Métricas Principais (DAX)

- **R$ Custo:**
```DAX
R$ Custo = SUMX(Vendas; Vendas[Quantidade] * RELATED(Produto[CustoUnitario]))
```

- **R$ Margem:**
```DAX
R$ Margem = [R$ Receita] - [R$ Custo]
```

- **R$ Receita:**
```DAX
R$ Receita = SUM(Vendas[Receita])
```

## 📊 Dashboards Criados
1. **Receita x Custos x Margem**
2. **Receita por Ano e Mês**
3. **Receita Top 5 por Grupo de Produto**
4. **Vendas de Produto por Vendedor por Ano e o Supervisor deste Vendedor**
5. **Margem por Linha de Produto**
6. **Margem Top 5 por Linha de Produto**
7. **Margem por Vendedor e Supervisor**

## 🚀 Como Usar
1. Baixe o arquivo `.pbix` na pasta `/reports`
2. Abra o Power BI Desktop
3. Importe os arquivos de dados (caso necessário)
4. Explore os dashboards e métricas!

## 📌 Melhorias Futuras
- Inclusão de novos filtros e segmentações
- Integração com novas fontes de dados
- Otimização de medidas DAX

## 🏆 Créditos
Este projeto foi desenvolvido com suporte da plataforma **Xperium**.

## 📞 Contato
Caso tenha dúvidas ou sugestões, entre em contato!

🔗 LinkedIn: [Pedro Henrique](https://www.linkedin.com/in/pedro-henrique-61541b214/)

