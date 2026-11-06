# FIA Aprendizagem Conexionista
# 05/11/2026

Aluno: João Pedro do Nascimento Seixas<br><br>
Aluno: José Henrique da Cruz Costa<br><br>
Aluno: John Kennedy de Almeida Castro<br><br>
Aluna: Livia Karolina Gomes do Nascimento<br><br>
Aluno: Lorenzo Augusto da Costa Freitas<br><br>

Explicação do Código:<br><br>
#Arquitetura e Parâmetros<br><br>

Trata-se de uma rede neural com 2 camadas, configurada da seguinte forma:<br><br>

Tamanho do lote (N): são processados 64 exemplos ao mesmo tempo.<br><br>
Entrada (D_in): os dados recebidos têm 1000 dimensões.<br><br>
Camada oculta (H): conta com 100 neurônios e usa a função de ativação Sigmoide.<br><br>
Camada de saída (D_out): devolve 10 dimensões (as predições).<br><br>
Ciclos de treino: o loop roda por 2000 iterações.<br><br>
Taxa de aprendizado: fixada em 1e-4 (0.0001), usada na atualização dos pesos.<br><br>

#Etapas do Treinamento<br><br>

O código se organiza em quatro partes principais:<br><br>

Definição da rede: estabelece o tamanho das camadas e cria as matrizes dos dados de entrada (x), das saídas alvo (y) e dos pesos (w1, w2), todos com valores aleatórios.<br><br>
Forward pass (Propagação): gera a previsão da rede ao calcular os valores da camada oculta (com a função sigmoide) e da saída. Depois, mede o erro (loss) ao comparar o resultado obtido com o alvo esperado.<br><br>
Cálculo dos gradientes: usa a técnica de backpropagation (regra da cadeia) para obter as derivadas analíticas, o que define quanto cada peso contribui para o erro total.<br><br>
Descida de gradiente: ajusta os pesos subtraindo deles os gradientes multiplicados pela taxa de aprendizado (1e-4), reduzindo o erro de forma iterativa.
Saída Esperada<br><br>

Ao rodar o código, serão impressas 2000 linhas no console. Cada linha mostra o número da iteração (de 0 a 1999) junto com o valor da função de perda (loss) naquele instante. Como a meta é aprender a partir dos dados, espera-se que o loss comece alto e vá diminuindo gradualmente ao longo das iterações.
