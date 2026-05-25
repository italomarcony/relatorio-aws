# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 24 de maio de 2026  
Empresa: Distribuidora Farmacêutica (situação fictícia)  
Responsável: Italo Marcony

## Introdução
Este relatório apresenta uma proposta inicial de adoção de serviços AWS para uma empresa farmacêutica distribuidora de produtos farmacêuticos que ainda não possui ambiente em nuvem. O foco da proposta é reduzir custos operacionais, evitar desperdícios com infraestrutura ociosa e melhorar a gestão de dados e estações de trabalho.

Como se trata de uma empresa do setor farmacêutico, a estratégia prioriza serviços que apoiem armazenamento seguro de documentos e backups, uso eficiente de recursos computacionais e acesso remoto para equipes administrativas, comerciais e de suporte. A escolha dos serviços considera cenários comuns desse tipo de operação, como controle de estoque, sistemas internos, relatórios, documentos regulatórios e acesso corporativo distribuído.

## Descrição do Projeto
A proposta foi organizada em 3 etapas, cada uma associada a um serviço AWS com potencial direto de redução de custos.

### Etapa 1: Amazon S3
- **Nome da ferramenta:** Amazon S3  
- **Foco da ferramenta:** armazenamento escalável de arquivos, backups, documentos fiscais, relatórios, catálogos de produtos e arquivos regulatórios.  
- **Descrição de caso de uso:** a distribuidora pode centralizar documentos administrativos, notas, relatórios de estoque, comprovantes e cópias de segurança em buckets do S3, usando classes de armazenamento mais econômicas conforme a frequência de acesso.

O Amazon S3 oferece diferentes classes de armazenamento criadas para diferentes padrões de acesso, permitindo reduzir custos sem precisar manter servidores locais de arquivos. Para dados com acesso imprevisível, o S3 Intelligent-Tiering move os objetos automaticamente para camadas mais baratas, com economia de até 40% na camada infrequente, até 68% na camada de archive instant access e até 95% para dados raramente acessados em deep archive access.

Para a empresa farmacêutica, isso é útil em documentos históricos, backups antigos, relatórios fechados por período, registros de auditoria e arquivos que precisam ser mantidos por mais tempo. Assim, a empresa reduz gastos com infraestrutura física, manutenção de storage local e crescimento descontrolado de servidores de arquivos.

### Etapa 2: AWS Savings Plans
- **Nome da ferramenta:** AWS Savings Plans  
- **Foco da ferramenta:** redução de custos de computação em workloads contínuos.  
- **Descrição de caso de uso:** após migrar sistemas internos, banco de dados de apoio, APIs, ERP, dashboards e rotinas automatizadas para a AWS, a empresa pode contratar Savings Plans para pagar menos do que pagaria no modelo sob demanda.

Os Savings Plans são um modelo de preços baseado em compromisso de uso por 1 ou 3 anos, aplicável a serviços como Amazon EC2, AWS Lambda e AWS Fargate. O Compute Savings Plan pode reduzir custos em até 66%, enquanto o EC2 Instance Savings Plan pode chegar a até 72% de economia em comparação ao preço On-Demand.

Esse serviço é indicado para uma distribuidora farmacêutica que tenha sistemas estáveis rodando diariamente, como portal interno, integração com estoque, consultas de pedidos, monitoramento logístico e processamento recorrente de dados. Em vez de pagar valor cheio por uso contínuo, a empresa assume um consumo previsível e transforma esse padrão em economia mensal relevante.

### Etapa 3: Amazon WorkSpaces
- **Nome da ferramenta:** Amazon WorkSpaces  
- **Foco da ferramenta:** desktops virtuais para usuários administrativos, atendimento, suporte e equipes remotas.  
- **Descrição de caso de uso:** a empresa pode disponibilizar estações virtuais para colaboradores sem precisar comprar ou renovar tantos computadores físicos de maior capacidade, além de centralizar manutenção e acesso remoto.

O Amazon WorkSpaces oferece opções de cobrança que ajudam no controle de gastos. No modo AutoStop, a cobrança por uso é interrompida quando o desktop virtual não está em uso, mantendo uma taxa base baixa e retomando o ambiente quando o usuário volta a acessar; a própria AWS indica esse modelo para usuários ocasionais ou de meio período.

A página de preços da AWS mostra que a escolha do modelo de consumo altera de forma importante o custo final. Em um exemplo oficial, 10 usuários ocasionais com cobrança por hora geram custo mensal de 204,50 dólares, enquanto outro grupo de 100 usuários com cobrança mensal fixa totaliza 4.400 dólares, mostrando que perfis diferentes exigem modelos diferentes para evitar desperdício.

Para a distribuidora farmacêutica, isso pode reduzir custos com aquisição de máquinas, suporte presencial, trocas frequentes de hardware e preparação de ambientes para filiais ou equipes externas. Também facilita padronização de acesso a sistemas críticos, como ERP, CRM e painéis operacionais.

## Benefícios Esperados
A adoção combinada desses três serviços permite atuar em três frentes principais de economia:

- Redução de custos com armazenamento e backup por meio do Amazon S3 e suas classes de armazenamento.
- Redução do custo de processamento contínuo com AWS Savings Plans para cargas previsíveis.
- Redução de gastos com estações de trabalho e suporte distribuído com Amazon WorkSpaces.
Além da economia direta, a empresa passa a ter melhor previsibilidade financeira, mais escalabilidade e menor dependência de infraestrutura local. Isso é especialmente importante em operações que precisam crescer com segurança, manter documentos por longos períodos e sustentar rotinas administrativas e logísticas sem ampliar custos de forma proporcional.

## Conclusão
Para uma empresa farmacêutica distribuidora que está começando sua jornada em cloud, a recomendação inicial é adotar Amazon S3, AWS Savings Plans e Amazon WorkSpaces como base para uma estratégia de redução de custos. Esses serviços atacam gastos com armazenamento, computação e estações de trabalho, que costumam representar parcelas importantes do custo operacional em empresas em crescimento.

Com essa combinação, a empresa consegue iniciar sua modernização em nuvem de forma controlada, com foco em eficiência financeira e expansão gradual. A continuidade do projeto pode incluir análise de segurança, monitoramento, backup avançado e governança de custos para amadurecer ainda mais o ambiente cloud.

## Anexos
- Modelo de relatório adaptado para o cenário proposto.
- Referências institucionais da AWS utilizadas para embasar a escolha dos serviços.

Assinatura do Responsável pelo Projeto:

Italo Marcony
