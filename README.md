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
| **1** | Alta | **US01 (Catalogação de Dados)**: Como Operador de Dados, quero catalogar as fontes oficiais e seus respectivos conjuntos de dados para identificar a origem, a competência e as características das informações utilizadas nos indicadores. | 5 | 1 |
| **2** | Alta | **US02 (Importação de Dados)**: Como Operador de Dados, quero importar conjuntos de dados ambientais para iniciar seu processamento e preservar as informações originalmente recebidas. | 8 | 1 |
| **3** | Alta | **US03 (Controle de Qualidade)**: Como Operador de Dados, quero validar os dados importados e consultar os registros rejeitados para corrigir problemas de qualidade antes do cálculo dos indicadores. | 8 | 1 |
| **4** | Alta | **US04 (Monitoramento de Processamentos)**: Como Operador de Dados, quero acompanhar o andamento das cargas e dos cálculos para identificar falhas e verificar a conclusão dos processamentos. | 5 | 1 |
| **5** | Alta | **US05 (Indicadores de Conservação)**: Como Analista Socioambiental, quero consultar os indicadores de conservação de um imóvel para avaliar sua cobertura vegetal, sua Reserva Legal e suas Áreas de Preservação Permanente. | 8 | 2 |
| **6** | Alta | **US06 (Restrições Territoriais)**: Como Analista Socioambiental, quero identificar sobreposições do imóvel com áreas protegidas e embargadas para reconhecer restrições ambientais associadas à propriedade. | 8 | 2 |
| **7** | Alta | **US07 (Eventos Ambientais)**: Como Analista Socioambiental, quero consultar ocorrências de desmatamento e focos de calor no imóvel para identificar eventos ambientais nos períodos analisados. | 8 | 2 |
| **8** | Alta | **US08 (Versionamento e Publicação)**: Como Operador de Dados, quero consolidar e publicar uma versão aprovada dos resultados para disponibilizar indicadores confiáveis sem perder o histórico dos processamentos anteriores. | 8 | 2 |
| **9** | Alta | **US09 (Consulta de Indicadores)**: Como Gestor, quero consultar os indicadores ambientais publicados por imóvel e por município para apoiar a avaliação socioambiental de propriedades e regiões do Paraná. | 8 | 3 |
| **10** | Média | **US10 (Comparação de Versões)**: Como Gestor, quero comparar versões dos indicadores de um mesmo imóvel para identificar alterações entre diferentes competências e processamentos. | 5 | 3 |
| **11** | Alta | **US11 (Auditoria e Rastreabilidade)**: Como Auditor, quero rastrear os resultados publicados e consultar as operações que os originaram para comprovar sua procedência, integridade e responsabilidade. | 8 | 3 |
| **12** | Média | **US12 (Integração via API)**: Como Responsável por Integrações, quero consultar os resultados publicados por API para disponibilizá-los em outras aplicações autorizadas. | 5 | 3 |

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
