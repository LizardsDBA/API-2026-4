# API 4º Semestre BD
# LizardsDBA - DataGis
# Documentação - Sprint 2
<p align="center">
      <img src="/docs/assets/logo_lizards.jpeg" alt="logo LizardsDBA" width="200">
</p>

## Desafio 

| Capacidade estimada da equipe por sprint |
| --- |
| 32 Story points |

## Sprint Goal

| Meta da sprint | Previsão da sprint |
| --- | --- |
| User stories de rank 5, 6 e 7 (24 story points) | User story de rank 8 (8 story points) |

## Backlog da Sprint 2

| Rank | Prioridade | User Story | Estimativa (SP) |
| :---: | :---: | :--- | :---: |
| **5** | Média | **US05 (Indicadores de Conservação)**: Como Analista Socioambiental, quero consultar os indicadores de conservação de um imóvel para avaliar sua cobertura vegetal, sua Reserva Legal e suas Áreas de Preservação Permanente. | 8 |
| **6** | Média | **US06 (Restrições Territoriais)**: Como Analista Socioambiental, quero identificar sobreposições do imóvel com áreas protegidas e embargadas para reconhecer restrições ambientais associadas à propriedade. | 8 |
| **7** | Média | **US07 (Eventos Ambientais)**: Como Analista Socioambiental, quero consultar ocorrências de desmatamento e focos de calor no imóvel para identificar eventos ambientais nos períodos analisados. | 8 |
| **8** | Média | **US08 (Versionamento e Publicação)**: Como Operador de Dados, quero consolidar e publicar uma versão aprovada dos resultados para disponibilizar indicadores confiáveis sem perder o histórico dos processamentos anteriores. | 8 |

---

## Burndown da Sprint 2 

---

## DoR e DoD por User Story – Sprint 2

### US05 (Indicadores de Conservação)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e o seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com a equipe.
* [ ] **Insumos de Homologação:** Arquivos e dados geoespaciais tratados referentes à Área de Preservação Permanente (APP), Reserva Legal (RL) e vegetação nativa estão disponíveis na base de dados.
* [ ] **Modelo de Dados:** O diagrama relacional para o armazenamento dos cálculos de conservação (ICV, IRL, IAPP) está desenhado e homologado pelo DBA.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras:** A User Story não depende de outra.
* [ ] **Compreensão Validada com a Equipe:** A equipe discutiu a história coletivamente e confirma o entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste (unidade e integração) foram definidos previamente, alinhados à cobertura mínima exigida.

**DoD - Definition of Done**
* [ ] **Estrutura de Banco de Dados (Oracle):** Rotinas em PL/SQL criadas para calcular as áreas e porcentagens de vegetação nativa, APP e RL em relação à área total do imóvel.
* [ ] **Backend (Spring Boot):** APIs REST desenvolvidas e documentadas (OpenAPI) para expor os indicadores de conservação calculados.
* [ ] **Frontend (Vue.js):** Tela com gráficos e tabelas (utilizando Chart.js) implementada para exibir o balanço ecológico (passivo/excedente) da propriedade.
* [ ] **Versionamento & Git:** Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código:** Código limpo e livre de fragmentos comentados.
* [ ] **Cobertura de Testes:** Testes de unidade com cobertura mínima de 70% e testes de pipeline funcionando.

---

### US06 (Restrições Territoriais)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e o seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com a equipe.
* [ ] **Insumos de Homologação:** Dados vetoriais oficiais de Terras Indígenas, Unidades de Conservação e Áreas Embargadas do IBAMA/ICMBio estão disponíveis para teste.
* [ ] **Modelo de Dados:** O modelo relacional para registrar os alertas de intersecção e infrações está homologado pelo DBA.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras:** A User Story não depende de outra ainda não iniciada.
* [ ] **Compreensão Validada com a Equipe:** A equipe discutiu a história coletivamente e confirma o entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste (unidade e integração) foram definidos previamente.

**DoD - Definition of Done**
* [ ] **Estrutura de Banco de Dados (Oracle):** Queries espaciais implementadas e testadas para cruzar a geometria do imóvel rural com as áreas protegidas e embargadas.
* [ ] **Backend (Spring Boot):** APIs REST documentadas.
* [ ] **Frontend (Vue.js):** Mapa interativo (Leaflet) implementado para visualizar de forma clara as sobreposições entre os polígonos do imóvel e as áreas de restrição.
* [ ] **Versionamento & Git:** Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código:** Código livre de fragmentos comentados.
* [ ] **Cobertura de Testes:** Testes de unidade com cobertura mínima de 70% e testes de pipeline funcionando.

---

### US07 (Eventos Ambientais)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e o seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com a equipe.
* [ ] **Insumos de Homologação:** Arquivos do INPE contendo o desmatamento (PRODES) e os focos de calor diários (lat/long) estão carregados para homologação.
* [ ] **Modelo de Dados:** Estrutura de dados para o histórico temporal de eventos ambientais validada com o DBA.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras:** A User Story não depende de outra ainda não iniciada.
* [ ] **Compreensão Validada com a Equipe:** A equipe discutiu a história coletivamente e confirma o entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste (unidade e integração) foram definidos previamente.

**DoD - Definition of Done**
* [ ] **Estrutura de Banco de Dados (Oracle):** Funções analíticas e espaciais implementadas para contabilizar focos de calor e calcular a área suprimida de vegetação (IDesmat) em recortes temporais específicos.
* [ ] **Backend (Spring Boot):** APIs REST desenvolvidas para consultar a linha temporal de eventos detectados no perímetro do imóvel.
* [ ] **Frontend (Vue.js):** Tela com gráficos temporais e marcadores no mapa implementada para ilustrar a incidência de queimadas e desmatamento.
* [ ] **Versionamento & Git:** Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código:** Código livre de fragmentos comentados.
* [ ] **Cobertura de Testes:** Testes de unidade com cobertura mínima de 70% e testes de pipeline funcionando.

---

### US08 (Versionamento e Publicação)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e o seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com a equipe.
* [ ] **Insumos de Homologação:** Massa de dados com indicadores já calculados pelas histórias US05, US06 e US07 pronta para ser consolidada.
* [ ] **Modelo de Dados:** O diagrama das tabelas da Zona Publicada (Gold) está validado.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Compreensão Validada com a Equipe:** A equipe discutiu a história coletivamente e confirma o entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste definidos com ênfase na verificação de imutabilidade.

**DoD - Definition of Done**
* [ ] **Estrutura de Banco de Dados (Oracle):** Dados de conformidade ambiental persistidos na Zona Publicada, associados a um Hash SHA-256 único.
* [ ] **Backend (Spring Boot):** Serviço de assinatura digital implementado para gerar a versão imutável associando regras, execução e dados de entrada.
* [ ] **Frontend (Vue.js):** Funcionalidade para o usuário publicar a versão consolidada e consultar o catálogo de versões vigentes e anteriores.
* [ ] **Versionamento & Git:** Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código:** Código livre de fragmentos comentados.
* [ ] **Cobertura de Testes:** Testes de unidade com cobertura mínima de 70% e testes de pipeline funcionando.

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
    <td>Fagner Nascimento</td>
    <td>Product Owner</td>
    <td><a href="https://github.com/fagnerlouis"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/fagnerlouis"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_fagner.jpeg" alt="Foto Fagner" width="90"></td>
  </tr>
  <tr>
    <td>Flávio Pereira</td>
    <td>Scrum Master</td>
    <td><a href="https://github.com/jnr98"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/flavjuni"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_flavio.jpeg" alt="Foto Flavio" width="90"></td>
  </tr>  
  <tr>
    <td>Benjamin Marques</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/maarquueess"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/benjamin-marques-48a4bb359"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_benjamin.jpeg" alt="Foto Benjamin" width="90"></td>
  </tr>  
  <tr>
    <td>Brenda Bettini</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/brendabettini"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/brendabettini/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_brenda.jpeg" alt="Foto Brenda" width="90">
  </td>
  </tr> 
    <tr>
    <td>Cauã Mohor</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/CauaDK"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/cauã-mohor-pardini"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_caua.jpeg" alt="Foto Caua" width="90"></td>
  </tr> 
  <tr>
    <td>Lucas Castro</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/stlucass"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/lucas-castro-39a427285"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_lucas.png" alt="Foto Lucas" width="90"></td>
  </tr>
  <tr>
    <td>Luiz Gustavo</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/oliveiraluizgustavo"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/luiz-gustavo-oliveira09/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_luiz.jpeg" alt="Foto Luiz" width="90"></td>
  </tr>
  <tr>
    <td>Matheus de Paula</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/MrMatheTrue"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/matheus-de-paula-a547161a6/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_matheus.jpeg" alt="Foto Matheus" width="90"></td>
  </tr>
  <tr>
    <td>Richard Rangel</td>
    <td>Desenvolvedor</td>
    <td><a href="https://github.com/Richard-JV-Rangel"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"></a></td>
    <td><a href="https://www.linkedin.com/in/richard-rangel-86182a306/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a></td>
    <td><img src="https://github.com/LizardsDBA/API-2026-3/blob/main/docs/assets/pfp_richard.jpeg" alt="Foto Richard" width="90"></td>
  </tr>
</table>
