describe('Simulacao de Carga Simples com Cypress', () => {
  it('Simula multiplos acessos a aplicacao', () => {
    const numRequests = 50; // Numero de requisicoes simuladas
      // Loop para simular multiplos acessos
      for (let i = 0; i < numRequests; i++) {
        cy.visit('https://www.wikipedia.org/') // Substitua pela URL da aplicacao
        .then(() => {
      // Verifica se a pagina foi carregada corretamente
      cy.title().should('include', 'Wikipedia');
      });
    }
  });
});
