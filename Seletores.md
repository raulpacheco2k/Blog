Olá, comunidade de QAs! 👋✨

Gostaria de compartilhar uma descoberta recente com vocês. Recentemente, iniciei meus estudos em Cypress e explorei as melhores práticas. Como QA, enfrentamos desafios constantes ao tentar manter a estabilidade de nosso aplicativo diante das frequentes mudanças na interface do usuário.

Sem mais delongas, durante o estudo das melhores práticas para o Cypress, deparei-me com um conceito extremamente simples, porém muito benéfico: adicionar atributos personalizados aos testes nos elementos do DOM, como, por exemplo, data-test="loginButton". Dessa forma, fortalecemos o seletor utilizado nos testes, pois agora temos um seletor exclusivo para a automação dos testes end-to-end. Com isso, não estamos mais sujeitos a execuções de teste com falhas decorrentes as alterações em classes ou IDs (sem mencionar o XPath).

Essa abordagem reduz significativamente os problemas com os seletores, permitindo os desenvolvedores realizar alterações de código sem o receio de impactar negativamente nos testes automatizados.

💡 Lições Aprendidas:

Evite Seletores Frágeis: Seletores altamente específicos podem quebrar facilmente. Em vez disso, utilize atributos personalizados de teste para fornecer contexto aos seus seletores.

Isolamento de Alterações: A incorporação de atributos, como data-test, isola os seletores de alterações no código CSS ou JavaScript, proporcionando estabilidade aos testes.

Foco na Resiliência: Testes resistentes a mudanças significam menos dores de cabeça para a equipe de qualidade. Investir em seletores robustos vale a pena.
