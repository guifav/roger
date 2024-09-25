# Escritor de Artigos AI para Posts de Blog Otimizados para SEO

Para mais informações sobre inteligência artificial, acesse [www.guilhermefavaron.com.br](https://www.guilhermefavaron.com.br)

Este projeto utiliza agentes de IA para criar posts de blog otimizados para SEO sobre qualquer tópico. Ele aproveita a biblioteca CrewAI e os modelos de linguagem da OpenAI para planejar, escrever e editar artigos automaticamente.

Para mais detalhes sobre a utilização deste código, veja sua utilização na prática: [vídeo demonstrativo no Youtube](https://youtu.be/emyRZqY1jpo)

## Guia de Início Rápido para o Google Colab

1. Abra um novo notebook no Google Colab.

2. Instale as bibliotecas necessárias executando:
   ```
   !pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29
   ```

3. Copie e cole todo o código do script fornecido em uma célula do Colab caso não clique no botão do Colab no topo do arquivo "Roger_escritor_de_artigos_para_Blog.ipynb".

4. Configure sua Chave de API da OpenAI:
   - Clique no ícone de "chave" no menu vertical à esquerda.
   - Na seção "Secrets", adicione um novo segredo com o nome `OPENAI_API_KEY` e sua chave de API da OpenAI como valor.

5. (Opcional) Atualize o modelo da OpenAI:
   - Localize a seguinte linha no código:
     ```python
     os.environ["OPENAI_MODEL_NAME"] = 'gpt-3.5-turbo'
     ```
   - Altere 'gpt-3.5-turbo' para o modelo desejado (ex: 'gpt-4o', 'gpt-4o-mini').

6. Defina o tópico desejado:
   - Encontre a seguinte linha no final do código:
     ```python
     result = crew.kickoff(inputs={"topic": "Meias de Algodão"})
     ```
   - Substitua "Meias de Algodão" pelo tópico de sua escolha.

7. Execute todas as células no notebook em ordem.

## Notas Importantes

- **Segurança da Chave de API**: Nunca compartilhe seu notebook ou o publique com sua chave de API visível. Sempre use o recurso de segredos do Colab para proteger sua chave.

- **Seleção de Modelo**: O modelo padrão é 'gpt-3.5-turbo'. Você pode alterá-lo para outros modelos disponíveis da OpenAI como 'gpt-4o' ou 'gpt-4o-mini' para potencialmente melhores resultados, mas esteja ciente dos custos associados.

- **Tempo de Geração de Conteúdo**: Dependendo da complexidade do tópico e do modelo escolhido, o processo de geração do artigo pode levar vários minutos.

- **Variabilidade de Saída**: Como os modelos de linguagem são probabilísticos, você pode obter saídas ligeiramente diferentes cada vez que executar o script, mesmo com a mesma entrada.

- **Personalização**: Você pode modificar as funções dos agentes, objetivos e descrições de tarefas no código para ajustar a saída de acordo com suas necessidades.

- **Tratamento de Erros**: Se encontrar erros relacionados a limites de API ou conectividade, tente executar a célula novamente ou verifique sua chave de API e conexão com a internet.

- **Verificação de Conteúdo**: Sempre revise e verifique os fatos do conteúdo gerado antes de publicar, pois o texto gerado por IA pode às vezes conter imprecisões ou vieses.

## Solução de Problemas

- Se você receber um erro sobre a chave de API da OpenAI, certifique-se de que a configurou corretamente nos segredos do Colab.
- Se a instalação das bibliotecas falhar, tente reiniciar o runtime e executar o comando de instalação novamente.
- Para quaisquer problemas persistentes, consulte a documentação do CrewAI e da OpenAI, ou procure ajuda em fóruns relevantes.

Lembre-se de usar esta ferramenta de forma responsável e em conformidade com as políticas de uso e diretrizes de conteúdo da OpenAI.
