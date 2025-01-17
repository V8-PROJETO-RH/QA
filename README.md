Como Rodar os Testes
Pré-requisitos
- Node.js e npm instalados
- JDK (para rodar testes com JMeter)
- Docker (se necessário para executar microsserviços localmente)
1. Instalar Dependências
Antes de rodar os testes, instale as dependências necessárias:
```bash
npm install
```
2. Utilizar a Branch de Desenvolvimento
Para garantir que está trabalhando na versão mais recente do projeto, faça checkout na branch de desenvolvimento (`dev`):
```bash
git checkout dev
```
3. Rodar Todos os Testes
Para rodar todos os testes (frontend, backend e performance), utilize o seguinte comando:
```bash
./scripts/run-tests.sh
```
4. Rodar Apenas Testes de Frontend
Para rodar os testes unitários, de integração e E2E do frontend, execute:
```bash
./scripts/run-frontend.sh
```
5. Rodar Apenas Testes de Backend
Para rodar os testes dos microsserviços:
```bash
./scripts/run-backend.sh
```
6. Limpar Relatórios Antigos
Para limpar os relatórios gerados após os testes:
```bash
./scripts/clean-reports.sh
```
Testes Disponíveis
Frontend
- **Unitários**: Testes para componentes individuais (ex. `Button`, `Header`).
- **Integração**: Testes de integração entre componentes e APIs (ex. `LoginIntegration`, `APIIntegration`).
- **E2E**: Testes ponta a ponta utilizando Cypress (ex. `LoginE2E`, `DashboardE2E`).
Backend
- Testes para microsserviços como `user-service`, `job-service` e `application-service`.
Performance
- **Testes de carga**: Testes de desempenho com JMeter (`load-test.jmx`).
- **Testes de estresse**: Testes de estresse de backend (`stress-test.js`).
Relatórios
Os relatórios gerados após a execução dos testes são armazenados nas pastas `reports/junit` e `reports/coverage`. Eles podem ser acessados para visualizar os resultados dos testes e a cobertura de código.

Se você deseja contribuir com melhorias ou correções para os testes, basta abrir uma pull request. Certifique-se de estar na branch `dev` antes de enviar suas alterações. Verifique os testes locais antes de enviar para garantir que todos os testes estejam passando.
