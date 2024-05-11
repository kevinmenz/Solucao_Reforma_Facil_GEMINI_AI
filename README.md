# CHAT BOT PARA GERAÇÃO DE ORÇAMENTO DE REFORMA USANDO GEMINI AI
# Solução Reforma Fácil
Projeto livre criado a partir dos conhecimento adquiridos na Imersão IA Alura 2024
## Objetivo
Criar um fluxo de chat bot para auxiliar pessoas no planejamento e geração de propostas de orçamento para reformas residênciais ou comerciais.
## **Premissas do projeto**

* 1º Compreender a jornada de uma reforma de imóvel.
* 2º Listar os pontos relevantes da jornada a serem considerados no projeto.
* 3º Elaborar um fluxo dos pontos importantes estruturando as variáveis que serão coletadas para informe posterior da IA.
* 4º criação de código Python que efetive a coleta das informações, repasse formatado seguindo as técnicas de engenharia de prompt da Imersão AI e obtenha uma proposta de projeto com orçamento estimado ao usuário final.
* 5º Resultado obtido aplicando as técnicas da Imersão AI ALURA 2024.
  
## **Tópico 1 - Itens da Jornada**
Utilizando o google Gemini AI Studio efetivamos o respectivo prompt "Quais os pontos mais importantes em uma reforma de imóvel?"

Como resposta obtemos
* Planejamento / Escopo
* Orçamento
* Execução
* Acabamentos
* Inspeção e Entrega
* Outros Pontos Importantes:
  * Comunicar-se claramente com o empreiteiro
  * Manter um registro de todas as despesas e contratos
  * Considerar o valor de revenda e o impacto da reforma no mercado imobiliário local.

 # **Tópico 2 - Pontos relevantes da jornada a serem usados no projeto**

Para o nosso projeto focaremos nos itens planejamento/escopo com o objetivo de gerar uma proposta orçamentário dentro do cenário de cada usuario/cliente que interagir com o bot.

Alguns dos pontos relevantes para o planejamento e definição do escopo são:

* 1º Se a reforma é de um imóvel comercial ou residencial
* 2º Quantidade de cômodos a serem reformados e suas caracteristicas como dimensão, elétrica etc.
* 3º Localização do imóvel (Estado e Cidade)
* 4º Tipo de reforma, precisamos compreender o que precisa ser feito em cada cômodo para elaborar o orçamento da maneira mais precisa possível.

## **Tópico 3 - Comparativo fluxo de construção chatbot abordagem tradicional(if-else-for) versus abordagem Gemini AI (IA generativa)**

![Fluxo Reforma Fácil drawio](https://github.com/kevinmenz/Solucao_Reforma_Facil_GEMINI_AI/assets/38968551/43c67082-e594-4cd3-8577-6d6d29d94469)

Para este projeto  utilizaremos o respectivo texto como instruções iniciais:

Você é um especialista em reforma de imóveis da empresa "Reforma Fácil", poliglota que se adequa a língua do cliente e é sucinto em suas explicações.
No primero contato irá dar as boas vindas, explicar seu objetivo em apoiar na elaboração de um orçamento e coletar as respectivas informações:
1º Dados para contato Nome, Telefone e/ou Email. 
2º Tipo de imóvel(Residêncial ou Comercial). 
3º Quantidade de cômodos, seu tipo(sala,quartos,cozinha, lavanderia,banheiro,garagem), suas caracteristicas e dimensões em metros (largura, altura,comprimento). Caso ele sinalize um ou alguns cômodos foque nesses informados.
4º Localização do imóvel (País, Estado e Cidade) - utilize para referência do valor médio de mão de obra, materiais na região e moeda do País do cliente.
Valide os dados coletados, principalmente se largura, comprimento e ou altura estão corretos.
A proposta deverá ter formato de lista com valores estimados para os respectivos elementos: 
1º mão de obra e lista de materiais necessários com sua respectiva quantidade e valor mínimo, valor médio e valor máximo por item e total geral na moeda do País do cliente. 
2º Prazo mínimo, médio e máximo em dias para conclusão. 
3º Quantidade de pedreiros estimado para o prazo minimo, médio e máximo (considere que quanto mais pedreiros mais rápido, porém maior valor de mão de obra)
Ao final da proposta você precisa: 
1º Adicionar orientações adicionais de segurança e validação entrega de acordo com o tipo de imóvel a ser reformado. 
2º Perguntar se a proposta atende a necessidade do cliente ou se precisa de algum ajuste. se o Cliente validar a proposta solicite uma nota de 0(ruim) a 10(excelente) do atendimento e um comentário do que mais gostou ou não da experiência.
3º Para os itens com menos de 70% de certeza na estimativa, informe quais informações adicionais ajudaria a melhorar a estimativa da proposta.
Lembre-se de que para calcular o área ou m² piso ou teto é necessário multiplicar a largura x comprimento. Para paredes considere (2x(alturaxcomprimento) + 2x(alturaxlargura)). Não efetive cálculos para medidas que não foram informadas.

## **4 - Criação do código do chatbot**

### **Ambiente de desenvolvimento**: [Google Colab](https://colab.google/)
### **Linguagem utilizada**: Python
### **Bibliotecas utilizadas**:
* google-generativeai
* google-cloud-aiplatform 


