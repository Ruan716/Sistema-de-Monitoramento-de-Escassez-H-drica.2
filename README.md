# Sistema de Monitoramento de Escassez Hídrica

>Olá! Gostaria de compartilhar meu primeiro projeto prático na Engenharia Ambiental e Sanitária. Utilizando Python, criei um script que visa desenvolver um sistema de avaliação de escassez hídrica capaz de identificar situações de escassez hídrica através do recebimento de dados de vazão e nível e emitir mensagens de aviso nos casos de escassez e não escassez.

## Lógica do código:
#### 1º

    #=== Sistema de Monitoramento de Escassez Hídrica ===
    print('=== Sistema de Monitoramento de Escassez Hídrica ===')
    
>##### '#' É utilizado para fazer comentários no código, que não afetam a sua estrutura nem seus resultados. Nesse código os comentários serão utilizados para organizar e detalhar cada parte do código.
>##### A função 'print()' é utilizada para mostrar informações na tela. Nesse caso será mostrado no terminal '=== Sistema de Monitoramento de Escassez Hídrica ==='.
#
#### 2º

    #Entrada de Dados
    rio = input('Digite o nome do Rio: ')
    cidade = input('Digite o nome da cidade: ')
    nivel = float(input('Digite o nível (cm): '))
    vazao = float(input('Digite a vazão (m³/s): '))

>##### '=' É utilizado para atribuir um valor a uma variável. Nesse caso, a variável 'rio' recebe o valor 'input('Digite o nome do Rio: ').
>##### 'input( )' É utilizado para receber dados do usuário.
>##### Ex: No terminal será mostrado: 'Digite o nome do rio: ', para que o usuário adicione tal informação.
>##### 'float( )' transforma uma informação textual em um número decimal.
>##### Sem o 'float( )', quando o usuário pusesse o valor do nível o python entenderia como um texto e não seria possível comparar com os valores dos limites críticos, que são números.
>##### Ex: No terminal será mostrado: 'Digite o nível (cm): ', para que o usuário adicione tal informação.
#
#### 3º

    #Limites Críticos de Segurança Hídrica
    nivel_minimo = 100 #cm
    vazao_minima = 0.45 #m³/s
>##### Para estabelecer os níveis críticos deve-se utilizar '=' para atribuir valores para as variáveis nivel_minimo e vazao_minima.
#
#### 4º
    #Mensagem de Alerta
    if nivel < nivel_minimo or vazao < vazao_minima: 
        print('STATUS:[!] ALERTA DE BAIXOS NÍVEIS DE ÁGUA.')
        print('AÇÃO: Hora de Economizar!')
    else:
        print('STATUS:[OK] Níveis de água estáveis.')
        print('AÇÃO: Não há risco imediato de escassez.')
>##### A função 'if' significa 'se', '<' significa 'menor que' e 'or' significa 'ou', detalhando: Se o valor da variável 'nivel' for menor que o valor da variável 'nivel_minimo' ou se o valor da variável 'vazao' for menor que o valor da variável 'vazao_minima' a mensagem transmitida na tela para o usuário será: 'STATUS:[!] ALERTA DE BAIXOS NÍVEIS DE ÁGUA. AÇÃO: Hora de Economizar!'
>##### A função 'else' que significa 'senão' acontece quando não há o cumprimento das condições estabelecidas no 'if', logo se o valor da variável 'nivel' não for menor que o valor da variável 'nivel_minimo' e se o valor da variável 'vazao' não for menor que o valor da variável 'vazao_minima' a mensagem transmitida na tela para o usuário será: 'STATUS:[OK] Níveis de água estáveis. AÇÃO: Não há risco imediato de escassez.'
#
# Código completo
    # === Sistema de Monitoramento de Escassez Hídrica ===
    print('=== Sistema de Monitoramento de Escassez Hídrica ===')

    #Entrada de Dados
    rio = input('Digite o nome do Rio: ')
    cidade = input('Digite o nome da cidade: ')
    nivel = float(input('Digite o nível (cm): '))
    vazao = float(input('Digite a vazão (m³/s): '))

    #Limites Críticos de Segurança Hídrica
    nivel_minimo = 100 #cm
    vazao_minima = 0.45 #m³/s

    #Mensagem de Alerta
    if nivel < nivel_minimo or vazao < vazao_minima:
        print('STATUS:[!] ALERTA DE BAIXOS NÍVEIS DE ÁGUA.')
        print('AÇÃO: Hora de Economizar!')
    else:
        print('STATUS:[OK] Níveis de água estáveis.')
        print('AÇÃO: Não há risco imediato de escassez.')
