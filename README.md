# Comando Cypress

npm install cypress --save-dev

npx cypress open

## Código

```javascript
describe('Simulacao de Carga Simples com Cypress', () => {
  it('Simula multiplos acessos a aplicacao', () => {
    const numRequests = 50; // Numero de requisicoes simuladas

    // Loop para simular multiplos acessos
    for (let i = 0; i < numRequests; i++) {
      cy.visit('https://exemplo.com') // Substitua pela URL da aplicacao
        .then(() => {
          // Verifica se a pagina foi carregada corretamente
          cy.title().should('include', 'nomeExemplo'); //Substitua o nome de página
        });
    }
  });
});
