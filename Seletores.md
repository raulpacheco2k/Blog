Olá, comunidade tech! 👋✨

Gostaria de compartilhar um aprendizado recente com vocês. Recentemente, iniciei meus estudos em Cypress e explorando as melhores práticas. Como QA, enfrentamos desafios constantes ao tentar manter a estabilidade de nosso aplicativo diante das frequentes mudanças na interface do usuário.

Durante o estudo das melhores práticas para o Cypress, deparei-me com um conceito extremamente simples, porém muito benéfico: adicionar atributos personalizados para os testes nos elementos do DOM, como, por exemplo, data-test="loginButton". Dessa forma, fortalecemos o seletor utilizados nos testes, pois agora temos um seletor exclusivo para a automação dos testes end-to-end. Com isso, não estamos mais sujeitos as execuções de testes com falhas decorrentes as alterações em classes ou IDs (sem mencionar o XPath).

Essa abordagem reduz significativamente os problemas com os seletores, permitindo os desenvolvedores realizar alterações de código sem o receio de impactar negativamente nos testes automatizados.

💡 Lições Aprendidas:

Evite seletores frágeis: Seletores altamente específicos podem quebrar facilmente. Em vez disso, utilize atributos personalizados de teste para fornecer contexto aos seus seletores.

Isolamento de alterações: A incorporação de atributos, como data-test, isola os seletores de alterações no código CSS ou JavaScript, proporcionando estabilidade aos testes.

Foco na resiliência: Testes resistentes a mudanças significam menos dores de cabeça para a equipe de qualidade. Investir em seletores robustos vale a pena.
