# API 4º Semestre BD
# LizardsDBA - DataGis
<p align="center">
      <img src="docs/assets/logo_lizards.jpeg" alt="logo LizardsDBA" width="200">
</p>
<p align="center">
| <a href ="#desafio"> Desafio</a>  |        
  <a href ="#solução"> Solução</a>  |   
  <a href ="#backlog-do-produto"> Backlog do Produto</a>  |
  <a href ="#dor---definition-of-ready">DoR</a>  |
  <a href ="#dod---definition-of-done">DoD</a>  |
  <a href ="#cronograma-de-sprints"> Cronograma de Sprints</a>  |
  <a href = "#vídeo-de-apresentação"> Vídeo de apresentação</a> |
  <a href ="#tecnologias-utilizadas">Tecnologias</a> |
  <a href ="#manuais">Manuais</a> |
  <a href ="#equipe"> Equipe</a> |
</p>

## Título do projeto
### Plataforma de dados geográficos e imóveis rurais - DataGis

---

## Desafio
A **Visiona Tecnologia Espacial** atua em projetos que utilizam informações territoriais, ambientais e geoespaciais para apoiar processos de planejamento e tomada de decisão. Atualmente, os dados sobre imóveis rurais (Cadastro Ambiental Rural - CAR, APPs, Reserva Legal) vêm de fontes diversas, em diferentes formatos, níveis de qualidade e com frequências de atualização variadas, sem uma gestão centralizada.

Essa descentralização gera sérias dificuldades para garantir a **rastreabilidade** e **auditabilidade** completa das análises (saber qual versão estava vigendo, qual arquivo foi usado, quais dados foram validados ou rejeitados na quarentena e quais regras participaram do cálculo do indicador). Isso é crítico, por exemplo, para a concessão de crédito rural ou auditorias ecológicas.

---

## Solução
O **DataGis** é um MVP baseado em uma arquitetura de dados Medalhão de quatro zonas (Bruta, Tratada, Publicada e Quarentena) projetado para resolver esses gargalos de governança socioambiental.

A plataforma automatiza a ingestão de bases de dados geográficas e tabulares públicas/privadas, executa rotinas automáticas de triagem de qualidade, isola registros inconsistentes para quarentena (registrando detalhadamente os motivos) e processa cruzamentos espaciais e sociais complexos por meio do banco de dados Oracle. Os indicadores resultantes são disponibilizados via APIs REST documentadas e por meio de um portal web interativo dotado de mapas e gráficos de risco. Toda versão publicada é imutável e sua linhagem de dados pode ser auditada de ponta a ponta.


---

## Backlog do Produto

### Tabela – Product Backlog Geral
| Rank | Prioridade | User Story | Estimativa (SP) | Sprint |
| :---: | :---: | :--- | :---: | :---: |
| **1** | Alta | **US01 (Catalogação de Fontes)**: Como Operador de Dados, quero cadastrar as fontes dos dados ambientais para identificar a origem das informações utilizadas nos indicadores. | 3 | 1 |
| **2** | Alta | **US02 (Catalogação de Conjuntos)**: Como Operador de Dados, quero cadastrar os conjuntos fornecidos por cada fonte para organizar suas competências, coberturas e características geográficas. | 5 | 1 |
| **3** | Alta | **US03 (Importação)**: Como Operador de Dados, quero importar conjuntos de dados ambientais para iniciar seu processamento na plataforma. | 8 | 1 |
| **4** | Alta | **US04 (Validação)**: Como Analista Socioambiental, quero que os dados importados sejam validados para evitar o uso de registros inconsistentes nos indicadores ambientais. | 8 | 1 |
| **5** | Alta | **US05 (Diagnóstico de Rejeições)**: Como Operador de Dados, quero consultar os registros rejeitados e seus respectivos problemas para diagnosticar falhas de qualidade nos conjuntos recebidos. | 5 | 1 |
| **6** | Média | **US06 (Reprocessamento)**: Como Operador de Dados, quero reprocessar dados corrigidos para incorporá-los ao fluxo sem perder o histórico das rejeições anteriores. | 5 | 2 |
| **7** | Alta | **US07 (Monitoramento de Cargas)**: Como Operador de Dados, quero acompanhar o andamento das cargas e dos cálculos para identificar falhas e verificar quando os resultados estiverem concluídos. | 8 | 2 |
| **8** | Alta | **US08 (Cobertura Vegetal)**: Como Analista Socioambiental, quero consultar a cobertura vegetal nativa de um imóvel para avaliar sua proporção de vegetação preservada. | 8 | 2 |
| **9** | Alta | **US09 (Reserva Legal)**: Como Analista Socioambiental, quero consultar a situação da Reserva Legal de um imóvel para identificar déficit ou excedente em relação ao mínimo aplicável. | 8 | 2 |
| **10** | Alta | **US10 (APP)**: Como Analista Socioambiental, quero consultar a conservação das Áreas de Preservação Permanente de um imóvel para identificar áreas que necessitam de recuperação. | 8 | 2 |
| **11** | Alta | **US11 (Áreas Protegidas)**: Como Analista Socioambiental, quero identificar sobreposições do imóvel com áreas protegidas para reconhecer restrições territoriais relevantes. | 8 | 2 |
| **12** | Alta | **US12 (Áreas Embargadas)**: Como Analista Socioambiental, quero identificar sobreposições do imóvel com áreas embargadas para reconhecer restrições ambientais associadas à propriedade. | 5 | 2 |
| **13** | Alta | **US13 (Desmatamento)**: Como Analista Socioambiental, quero consultar as áreas de desmatamento sobrepostas ao imóvel para avaliar alterações da cobertura ambiental nos períodos analisados. | 8 | 2 |
| **14** | Alta | **US14 (Focos de Calor)**: Como Analista Socioambiental, quero consultar a incidência de focos de calor no imóvel para identificar ocorrências relacionadas a queimadas. | 5 | 2 |
| **15** | Alta | **US15 (Consolidação de Versão)**: Como Operador de Dados, quero consolidar os resultados aprovados em uma nova versão para preservar o histórico de cada processamento concluído. | 8 | 3 |
| **16** | Alta | **US16 (Publicação)**: Como Operador de Dados, quero publicar uma versão aprovada dos indicadores para disponibilizar resultados confiáveis para consulta. | 5 | 3 |
| **17** | Alta | **US17 (Visualização por Imóvel)**: Como Gestor, quero consultar os indicadores ambientais de um imóvel em mapas, tabelas e gráficos para apoiar sua avaliação socioambiental. | 13 | 3 |
| **18** | Alta | **US18 (Visualização por Município)**: Como Gestor, quero consultar os indicadores consolidados por município para analisar a situação ambiental de diferentes regiões do Paraná. | 8 | 3 |
| **19** | Alta | **US19 (Comparação de Versões)**: Como Gestor, quero comparar versões dos indicadores de um mesmo imóvel para identificar as alterações ocorridas entre diferentes processamentos. | 8 | 3 |
| **20** | Alta | **US20 (Rastreabilidade)**: Como Auditor, quero rastrear um indicador publicado até os dados, transformações e regras utilizados para comprovar sua origem e permitir sua reprodução. | 13 | 3 |
| **21** | Alta | **US21 (Histórico de Operações)**: Como Auditor, quero consultar o histórico das operações realizadas na plataforma para verificar os responsáveis e a conformidade dos processos. | 8 | 3 |
| **22** | Alta | **US22 (Integração via API)**: Como Responsável por Integrações, quero consultar os resultados publicados por API para disponibilizá-los em outras aplicações autorizadas. | 8 | 3 |
| **23** | Média | **US23 (Download de Resultados)**: Como Analista Socioambiental, quero baixar os resultados publicados para utilizá-los em análises complementares. | 5 | 3 |

---

## DoR - Definition of Ready
Para que uma User Story seja considerada pronta para desenvolvimento, ela deve cumprir o checklist acordado:
* [ ] **História Descrita**: A história tem um título claro e seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação**: Todos os critérios de aceitação foram detalhados e acordados com o time.
* [ ] **Insumos de Homologação**: Amostras reais de dados das fontes de imóveis rurais (CAR) e tabelas secundárias estão disponíveis.
* [ ] **Modelo de Dados**: O diagrama relacional da camada de dados envolvida está desenhado e homologado pelo DBA.
* [ ] **Estimativa Realizada**: O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras**: A User Story não depende de outra ainda não concluída ou não iniciada.
* [ ] **Compreensão Validada com o Time**: A Equipe discutiu a história coletivamente e confirma entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida**: Os cenários de teste (unidade e, quando aplicável, integração) foram definidos previamente, alinhados à cobertura mínima exigida.

---

## DoD - Definition of Done
Uma User Story só é considerada finalizada ("Pronta") se atender a todos os critérios de qualidadee:
* [ ] **Estrutura de Banco (Oracle)**: Tabelas da arquitetura medalhão criadas e implantadas na Oracle Cloud, com índices espaciais, constraints e rotinas PL/SQL testadas.
* [ ] **Backend (Spring Boot)**: APIs REST documentadas e integradas ao banco.
* [ ] **Frontend (Vue.js)**: Telas responsivas implementadas conforme wireframes, integradas com Axios, Leaflet e Chart.js.
* [ ] **Versionamento & Git**: Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código**: Código livre de fragmentos comentados.
* [ ] **Cobertura de Testes**: Testes de unidade com **cobertura mínima de 70%** e testes de pipeline funcionando.

---

## Cronograma de Sprints
| Sprint | Período | Documentação |
| :---: | :---: | :---: |
| 🟢 **KICK-OFF GERAL** | 24/08 - 28/08 | [ Kick-off Geral ] |
| 🟢 **CONSTRUÇÃO DO BACKLOG / PLANNING** | 31/08 - 04/09 | [ Planejamento ] |
| 🔴 **SPRINT 1** | 07/09 - 27/09 | [Sprint 1](./docs/processo/sprints/sprint-1/README.md) |
| 🔴 **SPRINT 1 REVIEW/PLANNING** | 28/09 - 02/10 | [Sprint 1](./docs/processo/sprints/sprint-1/README.md) |
| 🔴 **SPRINT 2** | 05/10 - 25/10 | [Sprint 2](./docs/processo/sprints/sprint-2/README.md) |
| 🔴 **SPRINT 2 REVIEW/PLANNING** | 26/10 - 30/10 | [Sprint 2](./docs/processo/sprints/sprint-2/README.md) |
| 🔴 **SPRINT 3** | 02/11 - 22/11 | [Sprint 3](./docs/processo/sprints/sprint-3/README.md) |
| 🔴 **SPRINT 3 REVIEW/PLANNING** | 23/11 - 27/11 | [Sprint 3](./docs/processo/sprints/sprint-3/README.md) |
| 🔴 **FEIRA DE SOLUÇÕES** | 03/12 | [ Feira de soluções ] |


---

## Vídeo de Apresentação
*   **Link**: _a ser adicionado ao final da Sprint 3_

---

## Tecnologias Utilizadas
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-000000?style=for-the-badge&logo=intellij-idea&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)

---

## Manuais
[Manual do Usuário e Técnico](docs/manuais/)

---
## Estratégia de Branch e Padrão de Commit
[Arquivos](docs/processo/sprints/)

---

## Equipe
<table>
  <tr>
    <th>Membro</th>
    <th>Função</th>
    <th>Github</th>
    <th>Linkedin</th>
    <th>Foto</th>
  </tr>
  <tr>
    <td>Lucas Castro</td>
    <td>Product Owner</td>
    <td><a href="https://github.com/stlucass"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/lucas-castro-39a427285"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_lucas.png" alt="Foto Lucas" width="90"></td>
  </tr>
  <tr>
    <td>Brenda Bettini</td>
    <td>Scrum Master</td>
    <td><a href="https://github.com/brendabettini"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/brendabettini/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_brenda.jpeg" alt="Foto Brenda" width="90">
  </td>
  </tr> 
  <tr>
  <tr>
  <tr>
    <td>Benjamin Marques</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/maarquueess"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/benjamin-marques-48a4bb359"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_benjamin.jpeg" alt="Foto Benjamin" width="90"></td>
  </tr>  
    <tr>
    <td>Cauã Mohor</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/CauaDK"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/cauã-mohor-pardini"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_caua.jpeg" alt="Foto Caua" width="90"></td>
  </tr>
<td>Fagner Nascimento</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/fagnerlouis"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/fagnerlouis"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_fagner.jpeg" alt="Foto Fagner" width="90"></td>
  </tr>
  <tr>
    <td>Flávio Pereira</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/jnr98"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/flavjuni"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_flavio.jpeg" alt="Foto Flavio" width="90"></td>
  </tr>  
    <td>Luiz Gustavo</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/oliveiraluizgustavo"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/luiz-gustavo-oliveira09/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_luiz.jpeg" alt="Foto Luiz" width="90"></td>
  </tr>
  <tr>
    <td>Matheus de Paula</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/MrMatheTrue"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/matheus-de-paula-a547161a6"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_matheus.jpeg" alt="Foto Matheus" width="90"></td>
  </tr>
  <tr>
    <td>Richard Rangel</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/Richard-JV-Rangel"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href=""><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="docs/assets/pfp_richard.jpeg" alt="Foto Richard" width="90"></td>
  </tr>
</table>

---

## Requisitos de Permanência
- Reuniões fixas: Participar das reuniões definidas pelo grupo. Caso não possa comparecer, avisar com antecedência e se atualizar depois.
- Ferramenta de Gestão: Manter sempre o backlog atualizado no Jira, registrando tarefas, progresso e conclusão.
- Comunicação: Sempre se comunicar com o grupo pelo WhatsApp ou pessoalmente para alinhar mudanças, tirar dúvidas e informar dificuldades.
- Prazos: Atentar-se aos prazos definidos. O projeto é importante para a conclusão do 3º semestre.
- Responsabilidade individual: Cada integrante é responsável pelas tarefas que assumir.
- Participação ativa: Contribuir com ideias, desenvolvimento, testes e documentação.
- Comprometimento: Evitar deixar tarefas acumularem ou depender constantemente de outros membros.
- Aviso prévio de problemas: Caso tenha dificuldades pessoais ou técnicas, comunicar o grupo o quanto antes.
