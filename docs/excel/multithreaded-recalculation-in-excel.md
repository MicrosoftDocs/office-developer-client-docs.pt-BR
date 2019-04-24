---
title: Recálculo multithreaded no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- células thread-safe [excel 2007],multithreading no Excel,tarefas simultâneas [Excel 2007],funções thread-safe [Excel 2007],recálculo multithreaded [Excel 2007],MTR [Excel 2007],funções XLL [Excel 2007], registrar como thread safe,recálculo [Excel 2007], multithreaded,contenção de memória [Excel 2007],registro de funções XLL como thread safe [Excel 2007],funções não seguras [Excel 2007]
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: f0b6f3d7310cac6d141fc74652a3333f70bda8e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310498"
---
# <a name="multithreaded-recalculation-in-excel"></a>Recálculo multithreaded no Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Office Excel 2007 foi a primeira versão do Excel a usar o MTR (recálculo multithread) de planilhas. Você pode configurar o Excel para usar até 1.024 threads simultâneos ao recalcular, independentemente do número de processadores ou núcleos de processador no computador. 
  
> [!NOTE]
> Há uma sobrecarga do sistema operacional associada a cada thread. Portanto, você não deve configurar o Excel para usar mais threads do que o número necessário. 
  
Se o computador tiver vários processadores ou núcleos de processador, o sistema operacional será responsável pela alocação dos threads para os processadores da maneira mais eficiente.
  
## <a name="excel-mtr-overview"></a>Visão geral do MTR do Excel

O Excel tenta identificar partes da cadeia de cálculo que podem ser recalculadas ao mesmo tempo em threads diferentes. A árvore muito simples a seguir (em que x ← y significa que y só depende de x) mostra um exemplo disso.
  
**Figura 1. Cálculo simultâneo em diferentes threads**

![Cálculo simultâneo em diferentes threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Cálculo simultâneo em diferentes threads")
  
Após o cálculo de A1, A2 e A3 podem ser calculados em um thread, enquanto B1 e C1 podem ser calculados em outro, presumindo que as células sejam thread-safe. 
  
> [!NOTE]
> O termo célula thread-safe significa uma célula que contém apenas funções thread-safe. O que é ou não thread-safe é detalhado em [O que é ou não considerado thread-safe pelo Excel](#xl2007xllsdk_threadsafe). 
  
A maioria das pastas de trabalho contém árvores de dependência bem mais complexas do que esse exemplo. Além disso, o momento do recálculo de uma célula não pode ser conhecido até um cálculo ser feito e pode variar muito, dependendo dos argumentos das funções. Para obter os melhores resultados, o Excel tenta melhorar a ordem de cálculo em cada cálculo até que nenhuma otimização seja mais possível.
  
O Excel usa um único thread principal para executar o seguinte:
  
- Comandos internos
    
- Comandos XLL
    
- Funções da interface do Gerenciador de Suplementos XLL (função **xlAutoOpen** e assim por diante) 
    
- Comandos definidos pelo usuário (muitas vezes chamados de macros) do Microsoft VBA (Visual Basic for Applications)
    
- Funções definidas pelo usuário do VBA
    
- Funções de planilha thread-unsafe internas (confira a próxima seção para obter uma lista)
    
- Funções e comandos definidos pelo usuário de planilha de macro XLM
    
- Funções e comandos de suplemento COM
    
- Funções e operadores em expressões de formatação condicional
    
- Funções e operadores em definições de nome definido usadas em fórmulas de planilha
    
- A avaliação forçada de uma expressão na caixa de edição de fórmula usando a tecla **F9** 
    
Todas as fórmulas de planilha, independentemente de as funções serem thread-safe ou não, são avaliadas no thread principal, a menos que o Excel esteja configurado para usar mais de um thread. Quando o usuário especifica que mais de um thread deve ser usado, os threads adicionais são usados para células thread-safe. O thread principal ainda pode ser usado para células thread-safe quando isso faz sentido do ponto de vista do balanceamento de carga.
  
Vale ressaltar que o Excel não executa mais de um comando de cada vez. Portanto, você não precisa adotar as mesmas precauções necessárias ao escrever funções thread-safe, como o uso de memória thread-local e seções críticas.
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a>O que é ou não considerado thread-safe pelo Excel
<a name="xl2007xllsdk_threadsafe"> </a>

O Excel considera apenas o seguinte como thread-safe:
  
- Todos os operadores unários e binários no Excel.
    
- Quase todas as funções de planilha internas, a partir do Excel 2007 (confira a lista de exceções)
    
- Funções de suplemento XLL registradas explicitamente como thread-safe.
    
As funções de planilha internas que não são thread-safe são:
  
- **FONÉTICA**
    
- **CÉL** quando o argumento "formato" ou "endereço" é usado 
    
- **INDIRETO**
    
- **INFODADOSTABELADINÂMICA**
    
- **MEMBROCUBO**
    
- **VALORCUBO**
    
- **PROPRIEDADEMEMBROCUBO**
    
- **CONJUNTOCUBO**
    
- **MEMBROCLASSIFICADOCUBO**
    
- **MEMBROKPICUBO**
    
- **CONTAGEMCONJUNTOCUBO**
    
- **ENDEREÇO** quando o quinto parâmetro (nome_da_planilha) é fornecido 
    
- Qualquer função de banco de dados (**BDSOMA**, **BDMÉDIA** e assim por diante) que se refere a uma tabela dinâmica
    
- **TIPO.ERRO**
    
- **HIPERLINK**
    
Em termos explícitos, os seguintes itens são considerados não seguros:
  
- Funções definidas pelo usuário do VBA
    
- Funções definidas pelo usuário de suplemento COM
    
- Funções definidas pelo usuário de planilha de macro XLM
    
- Funções de suplementos XLL não explicitamente registradas como thread-safe
    
As implicações são que as operações e funções a seguir não são thread-safe e falham se são chamadas de uma função XLL registrada como thread-safe:
  
- Chamadas para funções de informações XLM; por exemplo, **xlfGetCell** (**OBTER.CÉLULA**).
    
- Chamadas para **xlfSetName** (**DEF.NOME**) para definir ou excluir nomes internos XLL.
    
- Chamadas para funções definidas pelo usuário thread-unsafe usando **xlUDF**.
    
- Chamadas para a função [xlfEvaluate](xlfevaluate.md) para expressões que contenham funções thread-unsafe ou que contenham nomes definidos cujas definições contenham funções thread-unsafe. 
    
- Chamadas para a função [xlAbort](xlabort.md) para limpar uma condição de interrupção. 
    
- Chamadas para a função [xlCoerce](xlcoerce.md) para obter o valor de uma referência de célula não calculada. 
    
> [!NOTE]
> Funções de planilha XLL não podem chamar comandos da API de C, por exemplo, **xlcSave**, independentemente de terem sido registradas como thread-safe ou não. 
  
Considerando que funções XLL declaradas como thread-safe não podem chamar funções de informações XLM ou referenciar células não calculadas, o Excel não permite que funções XLL registradas como equivalentes de planilha de macro também sejam registradas como thread-safe. Portanto, a tentativa de obter o valor de uma referência de célula não calculada usando **xlCoerce** falha com um erro **xlretUncalced**. A chamada de uma função de informações XLM falha com um erro **xlretFailed**. Os outros pontos listados anteriormente falham com um código de erro introduzido na API de C do Excel: **xlretNotThreadSafe**. 
  
Todas as funções de retorno de chamada somente de API de C são thread-safe:
  
- **xlCoerce** (exceto se a coerção de referências de célula não calculada falhar) 
    
- **xlFree**
    
- **xlStack**
    
- **xlSheetId**
    
- **xlSheetNm**
    
- **xlAbort** (exceto quando usada para limpar uma condição de interrupção) 
    
- **xlGetInst**
    
- **xlGetHwnd**
    
- **xlGetBinaryName**
    
- **xlDefineBinaryName**
    
A única exceção é a função **xlSet** que, de qualquer forma, é um equivalente de comando e, portanto, não pode ser chamada de nenhuma função de planilha. 
  
Uma função de planilha XLL pode ser registrada no Excel como thread-safe. Isso informa ao Excel que a função pode ser chamada com segurança e simultaneamente em vários threads, embora você deva verificar se esse realmente é o caso. Você poderá possivelmente desestabilizar o Excel se uma função registrada como thread-safe se comportar de forma não segura.
  
## <a name="registering-xll-functions-as-thread-safe"></a>Registrar funções XLL como thread-safe
<a name="xl2007xllsdk_threadsafe"> </a>

As regras que um desenvolvedor deve cumprir ao escrever funções thread-safe são:
  
- Não chamar recursos em outras DLLs que possam não ser thread-safe.
    
- Não fazer chamadas thread-unsafe por meio da API de C ou COM.
    
- Proteger os recursos que podem ser usados simultaneamente por mais de um thread usando seções críticas.
    
- Usar memória local de thread para armazenamento específico de thread e substituir variáveis estáticas em funções por variáveis locais de thread.
    
O Excel impõe uma restrição adicional: funções thread-safe não podem ser registradas como equivalentes de planilha de macro e, assim, não podem chamar funções de informações XLM nem obter os valores de células não recalculadas.
  
## <a name="memory-contention"></a>Contenção de memória
<a name="xl2007xllsdk_threadsafe"> </a>

Sistemas multi-threaded devem resolver dois problemas fundamentais:
  
- Como proteger a memória que deve ser lida ou gravada por mais de um thread.
    
- Como criar e acessar a memória que é associada e, assim, privada para o thread de execução.
    
O sistema operacional Windows e o SDK (Software Development Kit) do Windows oferecem ferramentas para ambos os itens: seções críticas e a API de TLS (armazenamento local de thread), respectivamente. Saiba mais em [Gerenciamento de Memória no Excel](memory-management-in-excel.md).
  
O primeiro problema pode ocorrer, por exemplo, quando duas funções de planilha (ou duas instâncias de execução simultânea da mesma função) precisam acessar ou modificar uma variável global em um projeto de DLL. Essa variável global pode estar oculta em uma instância globalmente acessível de um objeto de classe.
  
O segundo problema pode ocorrer, por exemplo, quando uma função de planilha declara uma variável estática ou um objeto no código do corpo da função. O compilador de C/C++ apenas cria uma única cópia que todos os threads usam. Isso significa que uma instância da função pode alterar o valor, enquanto outra em um thread diferente pode supor que o valor é o que estava definido antes.
  
## <a name="example-applications-of-mtr"></a>Exemplos de aplicações de MTR
<a name="xl2007xllsdk_threadsafe"> </a>

Qualquer XLL que exporta funções de planilha pode aproveitar o MTR (recálculo multi-threaded) no Excel, desde que essas funções não precisem executar ações thread-unsafe. Isso habilita o Excel a recalcular pastas de trabalho que dependem delas o mais reapidamente possível e, portanto, desejável, seja qual for o aplicativo.
  
Especificamente, o MTR tem enorme impacto em relação ao tempo de recálculo de pastas de trabalho que chamam UDFs (funções definidas pelo usuário) que, por sua vez, chamam processos externos para obter o resultado desejado. Em particular, considere uma UDF que chama um servidor remoto que pode processar várias solicitações ao mesmo tempo e uma pasta de trabalho que contém muitas chamadas para essa função. Se o recálculo da pasta de trabalho for single-threaded, cada chamada à UDF e, assim, ao servidor remoto, deverá ser concluída para que a chamada seguinte possa ser feita. Isso desperdiça a capacidade do servidor de processar várias chamadas ao mesmo tempo. Se o recálculo da pasta de trabalho for multi-threaded, o Excel poderá fazer várias chamadas ao mesmo tempo ou em sequência rápida.
  
Se o Excel estiver configurado para usar o mesmo número de threads que o servidor (vamos chamar isso de N) e a topologia da árvore de dependência da pasta de trabalho o permitir, o tempo total de recálculo poderá ser reduzido para algo próximo de 1/N do tempo de cálculo single-threaded. Isso pode ocorrer até mesmo quando o computador cliente (em que a pasta de trabalho está sendo executada) tem apenas um processador, especialmente quando o tempo necessário para fazer a chamada ao servidor é pequeno em relação ao tempo necessário para o servidor processar a chamada. 
  
Há sobrecarga do sistema operacional para cada thread adicional. Portanto, pode ser necessário testar um pouco para que determinada pasta de trabalho, servidor e computador cliente encontrem o número ideal de threads que o Excel deve ser instruído a usar. 
  
Por exemplo, considere um computador com processador único que esteja executando o Excel e uma pasta de trabalho que contenha 1.000 células. Ele chama uma UDF que, por sua vez, chama um ou mais servidores remotos. Suponha que as 1.000 células não dependam umas das outras. Portanto, o Excel não precisa esperar até que uma chamada seja concluída antes de chamar a próxima. É possível ter alguma flexibilidade para essa restrição sem afetar esse exemplo. Se os servidores podem processar 100 solicitações simultaneamente, e o Excel está configurado para usar 100 threads, o tempo de execução pode ser reduzido para apenas 1/100 disso, em que apenas um thread é usado. A sobrecarga que ocorre quando o Excel aloca chamadas para cada thread e o sistema operacional gerencia 100 threads significa que, na prática, a redução não será tão elevada. Também existe a suposição implícita de que o servidor é bem dimensionado e, se for solicitado a processar 100 tarefas ao mesmo tempo, isso não afetará os tempos de conclusão de tarefas individuais significativamente.
  
Uma aplicação prática em que essa técnica pode oferecer uma vantagem importante refere-se aos métodos Monte Carlo, bem como a outras tarefas com grande volume de números, que podem ser divididas em subtarefas menores que podem ser delegadas a servidores.
  
## <a name="excel-services-considerations"></a>Considerações sobre os Serviços do Excel
<a name="xl2007xllsdk_threadsafe"> </a>

Os Serviços do Excel dão suporte ao carregamento, ao cálculo e à renderização de planilhas do Excel em um servidor. Os usuários podem acessar e interagir com as planilhas usando ferramentas de navegador padrão.
  
UDFs dos Serviços do Excel são criadas usando o código gerenciado do Microsoft .NET Framework e disponibilizados por meio de um assembly do .NET. XLLs não têm suporte nos Serviços do Excel. Um recurso de UDF de servidor de código gerenciado pode chamar um XLL para acessar sua funcionalidade, para que o usuário possa ter a mesma funcionalidade com uma pasta de trabalho carregada servidor no servidor que obteria com uma pasta de trabalho carregada no cliente.
  
Para disponibilizar as funções XLL dessa maneira, elas devem ser encapsuladas em um assembly do .NET que converta argumentos e retorne valores dos tipos de dados nativos para os tipos de dados gerenciados do .NET Framework e chame as funções XLL. O wrapper do .NET deve exportar uma UDF de servidor para cada função XLL que é acessada. Um requisito adicional é que as funções XLL chamadas dessa maneira devem ser thread-safe. Como as funções XLL não são registradas como ocorre no cliente Excel, o servidor e o wrapper do .NET não têm nenhuma maneira de impor que elas sejam thread-safe. É responsabilidade do desenvolvedor de XLL garantir isso.
  
## <a name="see-also"></a>Confira também

- [Recálculo do Excel](excel-recalculation.md)  
- [Gerenciamento de Memória no Excel](memory-management-in-excel.md) 
- [Acessar o código de XLL no Excel](accessing-xll-code-in-excel.md)  
- [Conceitos de programação do Excel](excel-programming-concepts.md)  
- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

