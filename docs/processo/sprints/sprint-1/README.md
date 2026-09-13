# API 4º Semestre BD
# LizardsDBA - DataGis
# Documentação - Sprint 1
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
| User stories de rank 1, 2, 3 e 4 (26 story points) | User story de rank 5 (8 story points) |

## Backlog da Sprint 1

| Rank | Prioridade | User Story | Estimativa (SP) |
| :---: | :---: | :--- | :---: |
| **1** | Alta | **US01 (Catalogação de Dados)**: Como Operador de Dados, quero catalogar as fontes oficiais e seus respectivos conjuntos de dados para identificar a origem, a competência e as características das informações utilizadas nos indicadores. | 5 |
| **2** | Alta | **US02 (Importação de Dados)**: Como Operador de Dados, quero importar conjuntos de dados ambientais para iniciar seu processamento e preservar as informações originalmente recebidas. | 8 |
| **3** | Alta | **US03 (Controle de Qualidade)**: Como Operador de Dados, quero validar os dados importados e consultar os registros rejeitados para corrigir problemas de qualidade antes do cálculo dos indicadores. | 8 |
| **4** | Alta | **US04 (Monitoramento de Processamentos)**: Como Operador de Dados, quero acompanhar o andamento das cargas e dos cálculos para identificar falhas e verificar a conclusão dos processamentos. | 5 |

---

## Burndown da Sprint 1 

---

## DoR e DoD por User Story – Sprint 1

### US01 (Catalogação de Dados)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com o time.
* [ ] **Insumos de Homologação:** Informações e metadados das fontes oficiais (ex: CAR, IBGE, INPE) a serem catalogadas estão disponíveis.
* [ ] **Modelo de Dados:** O diagrama relacional contendo a tabela `FONTE_DADO` está desenhado e homologado pelo DBA.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras:** A User Story não depende de outra ainda não concluída ou não iniciada.
* [ ] **Compreensão Validada com o Time:** A Equipe discutiu a história coletivamente e confirma entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste (unidade e, quando aplicável, integração) foram definidos previamente, alinhados à cobertura mínima exigida.

**DoD - Definition of Done**
* [ ] **Estrutura de Banco (Oracle):** Tabela de catálogo (`FONTE_DADO`) implantada na Oracle Cloud, com constraints e rotinas PL/SQL testadas.
* [ ] **Backend (Spring Boot):** APIs REST de catálogo documentadas e integradas ao banco.
* [ ] **Frontend (Vue.js):** Tela de "Conjuntos de dados" responsiva implementada conforme wireframes.
* [ ] **Versionamento & Git:** Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código:** Código livre de fragmentos comentados.
* [ ] **Cobertura de Testes:** Testes de unidade com cobertura mínima de 70% e testes de pipeline funcionando.

---

### US02 (Importação de Dados)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com o time.
* [ ] **Insumos de Homologação:** Amostras reais de dados de limites territoriais rurais em formatos CSV, JSON e GeoJSON estão disponíveis.
* [ ] **Modelo de Dados:** O diagrama relacional da Zona Bruta está desenhado e homologado pelo DBA.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras:** A User Story não depende de outra (depende apenas da conclusão prévia da US01 para associar a fonte).
* [ ] **Compreensão Validada com o Time:** A Equipe discutiu a história coletivamente e confirma entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste (unidade e, quando aplicável, integração) foram definidos previamente, alinhados à cobertura mínima exigida.

**DoD - Definition of Done**
* [ ] **Estrutura de Banco (Oracle):** Tabelas da Zona Bruta (Staging) criadas e implantadas na Oracle Cloud, preparadas para receber dados textuais e geometrias brutas (CLOB).
* [ ] **Backend (Spring Boot):** APIs REST de upload de arquivos documentadas e integradas para iniciar processos.
* [ ] **Frontend (Vue.js):** Tela de ingestão responsiva implementada, integrada com Axios para envio dos arquivos.
* [ ] **Versionamento & Git:** Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código:** Código livre de fragmentos comentados.
* [ ] **Cobertura de Testes:** Testes de unidade com cobertura mínima de 70% e testes de pipeline funcionando.

---

### US03 (Controle de Qualidade)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com o time.
* [ ] **Insumos de Homologação:** Amostras de dados reais contendo registros válidos e registros com inconsistências (ex: CPF/CNPJ inválido, geometria corrompida) estão disponíveis para testes.
* [ ] **Modelo de Dados:** O diagrama relacional da Zona Tratada está desenhado e homologado pelo DBA.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras:** A User Story não depende de outra.
* [ ] **Compreensão Validada com o Time:** A Equipe discutiu a história coletivamente e confirma entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste (unidade e, quando aplicável, integração) foram definidos previamente, alinhados à cobertura mínima exigida.

**DoD - Definition of Done**
* [ ] **Estrutura de Banco (Oracle):** Tabelas da Zona Tratada e Quarentena implantadas, com conversão para `SDO_GEOMETRY` (Oracle Spatial) e índices espaciais validados.
* [ ] **Backend (Spring Boot):** APIs REST de consulta à quarentena documentadas e integradas ao banco.
* [ ] **Frontend (Vue.js):** Tela para consultar registros rejeitados com seus respectivos motivos implementada.
* [ ] **Versionamento & Git:** Branch de funcionalidade (`feat/`) criada e Pull Request (PR) aberto e revisado por outro par.
* [ ] **Qualidade de Código:** Código livre de fragmentos comentados.
* [ ] **Cobertura de Testes:** Testes de unidade com cobertura mínima de 70% e testes de pipeline funcionando.

---

### US04 (Monitoramento de Processamentos)
**DoR - Definition of Ready**
* [ ] **História Descrita:** A história tem um título claro e seu objetivo de negócio é plenamente compreendido.
* [ ] **Critérios de Aceitação:** Todos os critérios de aceitação foram detalhados e acordados com o time.
* [ ] **Insumos de Homologação:** Logs e status de execução estão acessíveis para mapeamento e integração.
* [ ] **Modelo de Dados:** O modelo e a estrutura de leitura de logs para rastreamento de execuções estão validados com o DBA.
* [ ] **Estimativa Realizada:** O esforço de desenvolvimento foi estimado e pontuado em Story Points pela equipe.
* [ ] **Sem Dependências Bloqueadoras:** A User Story não depende de outra.
* [ ] **Compreensão Validada com o Time:** A Equipe discutiu a história coletivamente e confirma entendimento comum do escopo.
* [ ] **Estratégia de Testes Definida:** Os cenários de teste (unidade e, quando aplicável, integração) foram definidos previamente, alinhados à cobertura mínima exigida.

**DoD - Definition of Done**
* [ ] **Backend e Integração:** APIs REST documentadas consumindo os status, falhas e métricas do Apache Airflow.
* [ ] **Frontend (Vue.js):** Tela de "Execuções do pipeline" implementada, exibindo o andamento das cargas, tempo de duração e registros rejeitados.
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
