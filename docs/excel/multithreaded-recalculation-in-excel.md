---
title: Recálculo multithreaded no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- células de thread-safe [excel 2007], multithreading no Excel, tarefas simultâneas [Excel 2007], funções thread-safe [Excel 2007], recálculo multithreaded [Excel 2007], MTR [Excel 2007], funções XLL [Excel 2007], registrando como thread-safe, [recálculo Excel 2007], memória multithreaded, contenção [Excel 2007], registrando XLL funciona como thread seguras funções inseguras [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765425"
---
# <a name="multithreaded-recalculation-in-excel"></a>Recálculo multithreaded no Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Office Excel 2007 era a primeira versão do Excel use o recálculo multithreaded (MTR) das planilhas. Você pode configurar o Excel use até segmentos simultâneos de 1024 quando recalcular, independentemente do número de processadores ou núcleos de processador no computador. 
  
> [!NOTE]
> Há um sistema operacional sobrecarga associado com cada segmento, portanto você não deve configurar o Excel para usar mais threads do que você precisa. 
  
Se o computador tiver vários processadores ou núcleos de processador, o sistema operacional leva a responsabilidade para alocar os threads aos processadores da maneira mais eficiente.
  
## <a name="excel-mtr-overview"></a>Visão geral do Excel MTR

Excel tenta identificar partes da cadeia de cálculo que podem ser recalculadas simultaneamente em threads diferentes. A seguinte árvore muito simple (onde y x ← significa y depende somente x) mostra um exemplo disso.
  
**Figura 1. Calculando simultaneamente em threads diferentes**

![Calculando simultaneamente em threads diferentes] (media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculando simultaneamente em threads diferentes")
  
Depois que é calculado A1, A2 e, em seguida, A3 podem ser calculado em um segmento, enquanto B1 e, em seguida, C1 podem ser calculado em outro, supondo que todas as células são thread-safe. 
  
> [!NOTE]
> A célula de thread-safe termo significa que uma célula que contém apenas as funções thread-safe. O que é e não é thread-safe são detalhados [What ' s e é não considerado Thread seguros pelo Excel](#xl2007xllsdk_threadsafe). 
  
Pastas de trabalho mais práticas contêm árvores de dependência muito mais complexas do que esse exemplo. Além disso, o tempo de recálculo de uma célula não pode ser conhecido até que um cálculo é feito e pode variar bastante dependendo argumentos das funções. Para obter os melhores resultados, o Excel tenta melhorar a ordem de cálculo em cada cálculo até sem otimização adicional é possível.
  
Excel usa um único segmento principal para executar ou executar o seguinte:
  
- Comandos internos
    
- Comandos XLL
    
- Funções de interface do Gerenciador de suplementos XLL (função**xlAutoOpen** e assim por diante) 
    
- Microsoft Visual Basic para comandos definida pelo usuário de Applications (VBA) (geralmente conhecidos como macros)
    
- Funções definidas pelo usuário do VBA
    
- Funções de planilha não seguros thread internas (consulte a próxima seção para obter uma lista)
    
- Funções e definidas pelo usuário comandos de folha de macro XLM
    
- Funções e comandos do suplemento de COM
    
- Funções e operadores em expressões de formatação condicionais
    
- Funções e operadores dentro das definições de nome definido usadas em fórmulas de planilha
    
- Avaliação de uma expressão na caixa Editar fórmula usando a tecla **F9** forçada 
    
Todas as fórmulas de planilha, independentemente se as funções estão thread-safe ou não, são avaliadas no thread principal, a menos que o Excel está configurado para usar mais de um segmento. Quando o usuário Especifica o que mais de um segmento deve ser usado, os threads adicionais são usados para as células de thread-safe. Observe que o thread principal ainda pode ser usado para as células de thread-safe quando fizer sentido do ponto de vista balanceamento de carga.
  
Vale precisar reiniciar que Excel não fique mais de um comando ao mesmo tempo, portanto você não precisa empregar as mesmas precauções como quando você estiver escrevendo funções thread-safe, como o uso de memória local de segmento e seções críticas.
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a>O que é e não é considerado thread seguros pelo Excel
<a name="xl2007xllsdk_threadsafe"> </a>

Excel considera apenas o seguinte procedimento ao thread seguro:
  
- Todos os operadores unário e binário no Excel.
    
- Quase todas as funções de planilha internas iniciada no Excel 2007 (consulte a lista de exceções)
    
- Suplemento funções XLL que foram registradas explicitamente como thread-safe.
    
As funções de planilha internas que não são thread-safe são:
  
- **FONÉTICO**
    
- **CÉLULA** quando o argumento do "formato" ou "address" é usado 
    
- **INDIRETAS**
    
- **GETPIVOTDATA**
    
- **CUBEMEMBER**
    
- **CUBEVALUE**
    
- **CUBEMEMBERPROPERTY**
    
- **CUBESET**
    
- **CUBERANKEDMEMBER**
    
- **CUBEKPIMEMBER**
    
- **CUBESETCOUNT**
    
- **Endereço** onde o quinto parâmetro (o sheet_name) é fornecido 
    
- Qualquer função de banco de dados (**DSUM**, **BDMÉDIA**e assim por diante) que se refere a uma tabela dinâmica
    
- **ERRO. TIPO**
    
- **HIPERLINK**
    
Para ser explícitas, a seguir é considerada inseguros:
  
- Funções definidas pelo usuário do VBA
    
- COM suplemento-funções definidas pelo usuário
    
- Funções definidas pelo usuário de folha de macro XLM
    
- Funções de Suplemento XLL não explicitamente registrado como thread-safe
    
As implicações são que as operações e funções a seguir não são thread-safe e falharem se eles forem chamados de uma função XLL registrada como thread-safe:
  
- Chamadas para funções de informações XLM, por exemplo, **xlfGetCell** (**GET. CÉLULA**).
    
- Chamadas para **xlfSetName** (**SET.NAME**) para definir ou excluir os nomes internos XLL.
    
- Chamadas para funções definidas pelo usuário de thread-inseguras usando **xlUDF**.
    
- Chamadas para a função [xlfEvaluate](xlfevaluate.md) para expressões que contêm funções thread-inseguras ou que contêm nomes definidos cujas definições contêm funções thread-inseguros. 
    
- Chamadas para a função [xlAbort](xlabort.md) para limpar uma condição de quebra. 
    
- Chamadas para a função [xlCoerce](xlcoerce.md) para obter o valor de uma referência de célula não calculadas. 
    
> [!NOTE]
> Funções de planilha XLL não têm permissão para chamar os comandos do C API, por exemplo, **xlcSave**, independentemente se eles tiverem sido registrados como thread-safe ou não. 
  
Visto que as funções XLL declaradas como thread-safe não é possível chamar funções de informações XLM ou referência a células não calculadas, Excel não permite que as funções XLL registrados como equivalentes de folha de macro para também ser registrada como thread-safe. Portanto, a tentativa de obter o valor de uma referência de célula não calculadas usando **xlCoerce** falha com um erro de **xlretUncalced** . Função de informações chamar um XLM falhará com um erro **xlretFailed** . Os outros pontos listados anteriormente falharem com um código de erro introduzido do C API do Excel: **xlretNotThreadSafe**. 
  
As funções de retorno de chamada do C API somente são todas thread-safe:
  
- **xlCoerce** (exceto embora coerção da célula não calculada referencia falhar) 
    
- **xlFree**
    
- **xlStack**
    
- **xlSheetId**
    
- **xlSheetNm**
    
- **xlAbort** (exceto quando usado para limpar uma condição de quebra) 
    
- **xlGetInst**
    
- **xlGetHwnd**
    
- **xlGetBinaryName**
    
- **xlDefineBinaryName**
    
A única exceção é a função **xlSet** , que é, em qualquer caso, um equivalente de comando e, portanto não podem ser chamados a partir de qualquer função de planilha. 
  
Uma função de planilha XLL pode ser registrada com o Excel como thread-safe. Isso informa ao Excel que a função pode ser chamada com segurança e simultaneamente em vários threads, embora você deve garantir isso é realmente o caso. Você possivelmente pode desestabilizar Excel se uma função registrada como thread-safe, em seguida, se comporta de forma não segura.
  
## <a name="registering-xll-functions-as-thread-safe"></a>Registrando as funções XLL como thread-safe
<a name="xl2007xllsdk_threadsafe"> </a>

As regras que um desenvolvedor deve cumprir ao escrever funções thread-safe são:
  
- Não chame recursos de outras DLLs que podem não ser thread-safe.
    
- Não faça qualquer não seguros thread chamadas através do C API ou COM.
    
- Protege os recursos que poderiam ser usados simultaneamente por mais de um segmento usando as seções críticas.
    
- Use memória local de segmento para armazenamento específicos de segmento e substituir as variáveis estáticas dentro das funções com variáveis de segmento locais.
    
Excel impõe uma restrição adicional: funções thread-safe não pode ser registradas como equivalentes de folha de macro e, portanto, não é possível chamar as funções de informações ou obter os valores de células não recalculadas.
  
## <a name="memory-contention"></a>Contenção de memória
<a name="xl2007xllsdk_threadsafe"> </a>

Sistemas multithread devem atender duas questões fundamentais:
  
- Como proteger a memória que deve ser lido ou gravada por mais de um segmento.
    
- Como criar e memória de acesso que está associado e então particulares para, a execução do thread.
    
O sistema operacional Windows e Windows Software Development Kit (SDK) fornecem ferramentas para ambos dessas: seções críticas e a API de armazenamento de thread local (TLS) respectivamente. Para saber mais, consulte [Memory Management in Excel](memory-management-in-excel.md).
  
O primeiro problema pode surgir, por exemplo, quando duas funções de planilha (ou duas instâncias simultaneamente a execução da mesma função) precisam acessar ou modificar uma variável global em um projeto DLL. Lembre-se de que tal variável global pode estar ocultos em uma instância de um objeto de classe do acessível globalmente.
  
O segundo problema pode surgir, por exemplo, quando uma função de planilha declara uma variável estática ou um objeto no código do corpo da função. O compilador C/C++ cria apenas uma única cópia que usam todos os threads. Isso significa que uma instância da função poderia alterar o valor, enquanto a outra em um segmento diferente pode supondo que o valor é o que ele anteriormente definido.
  
## <a name="example-applications-of-mtr"></a>Aplicativos de exemplo de MTR
<a name="xl2007xllsdk_threadsafe"> </a>

Qualquer XLL que exporta as funções de planilha pode tirar proveito de recálculo multithreaded (MTR) no Excel, desde que essas funções não é necessário realizar ações não seguros thread. Isso permite que o Excel recalcule pastas de trabalho que dependem deles mais rápido possível e, portanto, é desejável que for o aplicativo.
  
Especificamente, MTR tem um enorme impacto sobre o tempo de recálculo das pastas de trabalho que chamam funções definidas pelo usuário (UDFs) que sozinhos chamar processos externos para obter o resultado desejado. Em particular, considere um UDF que chame um servidor remoto que pode processar muitas solicitações simultaneamente e uma pasta de trabalho que contém o número de chamadas para essa função. Se o recálculo da pasta de trabalho for single-threaded, cada chamada UDF e, portanto com o servidor remoto, deve concluir antes de seguir uma pode ser feita. Isso desperdiça a capacidade do servidor para processar muitas chamadas ao mesmo tempo. Se não for multithreaded recálculo da pasta de trabalho, o Excel pode fazer várias chamadas ao mesmo tempo ou em sucessão rápida.
  
Se o Excel está configurado para usar o mesmo número de threads como o servidor — chamá-lo N — e a topologia da árvore de dependência da pasta de trabalho permite que ele, o tempo total de recálculo poderia ser reduzido para algo se aproximando 1/N do tempo cálculo com um único segmento. Isso pode ser true, até mesmo, onde o computador cliente (em que a pasta de trabalho está sendo executado) tiver apenas um processador, especialmente onde o tempo necessário para fazer a chamada para o servidor é pequeno em relação ao tempo que leva o servidor ao processo a chamada. 
  
Não há sobrecarga de sistema operacional para cada segmento adicional. Portanto, alguns experimentação pode ser necessária para uma determinada pasta de trabalho e um determinado servidor e o computador cliente para localizar o número ideal de threads que Excel deve ser informado de usar. 
  
Por exemplo, considere um processador único computador que está executando o Excel e uma pasta de trabalho que contém as 1.000 células. Ele chama um UDF, que por sua vez, chama um ou mais servidores remotos. Suponha que a 1.000 células não dependem uns dos outros, para que o Excel não tenha esperar por uma chamada concluir antes de chamar o próximo. (Alguns relaxamento desta restrição é possível sem afetar neste exemplo.) Se os servidores podem processar solicitações de 100 simultaneamente e Excel está configurado para usar a 100 segmentos, o tempo de execução pode ser reduzido ao mínimo 1/100th que onde apenas um segmento é usado. A sobrecarga associada Excel alocar chamadas para cada segmento e o sistema operacional Gerenciando 100 segmentos significa que, na prática, a redução não será bastante nesse excelente. Há também uma pressuposição implícita aqui que o servidor é bem dimensionado e solicitando que ele processar 100 tarefas simultaneamente não afetará os tempos de conclusão de tarefa individual significativamente.
  
Um aplicativo prático nas quais essa técnica pode ter um importante benefício é de métodos Monte Carlo, assim como outras tarefas numericamente intensivas que podem ser divididas em subtarefas menores que podem ser delegadas aos servidores.
  
## <a name="excel-services-considerations"></a>Considerações de serviços do Excel
<a name="xl2007xllsdk_threadsafe"> </a>

Excel Services suporta o carregamento, calculando e renderização de planilhas do Excel em um servidor. Os usuários podem então acessar e interagir com as planilhas, usando as ferramentas padrão do navegador.
  
UDFs de serviços do Excel são criados usando código gerenciado do Microsoft .NET Framework e torná-los disponíveis, embora um assembly do .NET. XLLs não são suportados pelos serviços do Excel. Um servidor de código gerenciado recurso UDF pode ligar para um XLL para acessar sua funcionalidade, para que o usuário pode ter a mesma funcionalidade com uma pasta de trabalho do servidor carregado, assim como acontece com uma pasta de trabalho carregados pelo cliente.
  
Para disponibilizar as funções de um XLL dessa maneira, eles, portanto, devem ser quebrados em um assembly do .NET que converte argumentos e valores de retorno de tipos de dados nativos para os tipos de dados do .NET Framework gerenciados e que chama as funções XLL. O wrapper .NET seria exportar um servidor UDF para cada função XLL sendo acessado. Um requisito adicional é que todas as funções XLL chamadas dessa forma devem ser thread-safe. Como as funções XLL não são registradas da maneira que estão com o cliente do Excel, o servidor e o wrapper .NET não têm como impondo que eles são thread-safe. É responsabilidade do desenvolvedor XLL garantir isso.
  
## <a name="see-also"></a>Confira também

- [Recálculo do Excel](excel-recalculation.md)  
- [Gerenciamento de memória no Excel](memory-management-in-excel.md) 
- [Acessar o código de XLL no Excel](accessing-xll-code-in-excel.md)  
- [Excel Programming Concepts](excel-programming-concepts.md)  
- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

