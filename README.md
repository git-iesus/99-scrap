#🚀 99-Scrap
Um bot de automação inteligente desenvolvido em Python para monitorar, analisar e enviar propostas em projetos do site 99Freelas. O sistema utiliza uma abordagem híbrida de Web Scraping e RPA (Automação Robótica de Processos) para identificar oportunidades e precificar serviços de forma competitiva.

##📋 Sobre o Projeto
O objetivo deste projeto é otimizar o tempo de prospecção de freelancers. Ao invés de buscar projetos manualmente, o script varre múltiplas categorias, analisa a média de preços oferecida pela concorrência e submete uma proposta automaticamente com um valor calculado estrategicamente para ser competitivo.

##⚙️ Como Funciona (Arquitetura Híbrida)
O projeto combina duas técnicas principais para superar barreiras de anti-bot e capturar dados dinâmicos:

###Coleta de Dados Rápida (Requests + BeautifulSoup):
* O bot varre listas de projetos (Design, TI, Marketing, etc.) via requisições HTTP para mapear URLs rapidamente sem abrir o navegador.
* Interação Humana Simulada (PyAutoGUI):
* Para acessar dados sensíveis (como a média das propostas, que exige login) e preencher o formulário, o bot assume o controle do mouse e teclado.
* Ele navega visualmente, copia informações da tela e preenche a proposta simulando a digitação humana.

###Algoritmo de Precificação Dinâmica:
* O script lê a "Média das Propostas" e a "Duração Média" dos concorrentes.
* Calcula automaticamente um lance levemente inferior à média do mercado (Média - 1) para posicionar a proposta como o melhor custo-benefício.
* Lance mínimo : R$ 97,00
* Prazo mínimo : 2 dias

##✨ Funcionalidades
✅ Multi-Categoria: Varre listas de Design, Redação, Dev, Marketing, etc.
✅ Scraping Profundo: Extrai nome do cliente, orçamento original e métricas da concorrência.
✅ Bypass de Proteções: Usa navegação real (browser automation) para lidar com cookies e sessões de login.
✅ Smart Bidding: Lógica matemática para definir valor e prazo automaticamente.
✅ Relatório em Excel: Gera uma planilha .xlsx ao final com todos os projetos processados, valores de mercado e a proposta enviada.
✅ Safety First: Implementado com FAILSAFE (parada de emergência) e delays aleatórios para evitar bloqueios.

##🛠️ Tecnologias Utilizadas
Linguagem: Python 3
Web Scraping: BeautifulSoup4, Requests
Automação (GUI/RPA): PyAutoGUI, Pyperclip
Manipulação de Dados: Pandas, OpenPyXL, RegEx
Navegação: Webbrowser (Native)
