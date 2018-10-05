---
title: Programação com a API de C no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
localization_priority: Normal
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 53167241ebfaf8524fb58d14b4e1299809cdee50
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401619"
---
# <a name="programming-with-the-c-api-in-excel"></a>Programação com a API de C no Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Você pode usar a API de C e o Excel 2013 XLL Software Development Kit para criar funções de planilha de alto desempenho para o Excel 2013. As atualizações da API de C do Excel 2013 refletem o suporte contínuo aos usuários para os quais o desempenho da funcionalidade de terceiros ou interna é fundamental.
  
## <a name="excel-programming-interfaces"></a>Interfaces de Programação do Excel

O Excel oferece várias opções para desenvolver aplicativos que se integrem a ele. As interfaces de programação do Excel foram adicionadas a versões anteriores na seguinte ordem:
  
- **Linguagem de macro XLM:** a primeira linguagem acessível ao usuário para a extensão do Excel e a base da API de C. Embora ainda seja compatível com o Excel 2010, o XLM foi substituído há muito tempo pelo Visual Basic for Applications (VBA). 
    
- **API de C e XLLs:** DLLs integradas ao Excel. Essas DLLs oferecem a interface mais rápida e mais direta para a adição de funções de planilha de alto desempenho, embora às custas de alguma complexidade em comparação com as tecnologias mais recentes. 
    
- **VBA:** objetos com código do Visual Basic que estão associados a objetos de pasta de trabalho do Excel. O VBA permite interceptações de eventos, a personalização e a adição de funções e comandos definidos pelo usuário. O VBA é a opção de extensibilidade mais comumente usada e de maior disponibilidade. 
    
- **COM:** o padrão de interoperabilidade para aplicativos baseados no Windows, pelo qual o Excel expõe eventos e objetos. O VBA usa o COM para interagir com o Excel. O Excel exporta as bibliotecas do tipo COM que podem ajudar a criar aplicativos e recursos de código C++ COM que podem controlar o Excel externamente. 
    
- **O Microsoft .NET Framework:** o ambiente de código gerenciado para várias linguagens projetado para o desenvolvimento rápido de aplicativos para ambientes distribuídos. A linguagem de programação primária para código baseada no .NET Framework é C#, embora muitas linguagens possam ser compiladas para a linguagem intermediária da Microsoft (MSIL). O Excel 2013 pode acessar recursos de código contidos em assemblies do .NET Framework. 
    
## <a name="when-to-use-the-c-api"></a>Quando Usar a API de C

A principal razão para gravar XLLs e usar a API de C é criar funções de planilha de alto desempenho. Embora as funções XLL sejam frequentemente chamadas de funções definidas pelo usuário, o tempo investido para obter a compreensão e as habilidades necessárias para gravar XLLs tornam essa tecnologia inviável para a maioria dos usuários. No entanto, os aplicativos com funções de alto desempenho (no Excel 2013, a capacidade de gravar interfaces com vários threads para criar recursos de servidor eficientes) fazem dessa uma parte crucial da extensibilidade do Excel. 
  
A revisão da API de C introduzida no Excel 2007 trata principalmente dos aspectos relacionados a cálculos de alto desempenho, em vez de recursos como a interface do usuário.
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>Gravando funções de planilha de alto desempenho definidas pelo usuário

A API de C do Excel é a opção ideal quando você deseja criar funções de planilha de alto desempenho criando suplementos XLL. A API de C oferece o acesso mais direto aos dados da planilha. Os XLLs oferecem ao Excel o acesso mais direto aos recursos da DLL. O desempenho dos XLLs é aprimorado no Excel 2013 pela adição de novos tipos de dados e, sobretudo, do suporte para a execução de funções definidas pelo usuário em servidores clusterizados.
  
Trabalhar com os XLLs tem um custo: a API de C não tem os recursos de desenvolvimento rápido de nível superior do VBA, COM ou o .NET Framework. O gerenciamento de memória é de nível baixo e, portanto, atribui uma maior responsabilidade ao desenvolvedor. Muitos recursos do Excel que são expostos pelo COM, tornando-os disponíveis por meio do VBA e o .NET Framework, não são expostos à API de C.
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>Acessando Servidores de Vários Threads Usando Funções de Planilha XLL

O recálculo de vários threads (MTR), que foi introduzido no Excel 2007, permite criar funções de planilha XLL seguras para threads. Use essas funções para acessar servidores de vários threads. As seções posteriores descrevem com mais detalhes como isso pode aumentar significativamente o desempenho observado pelo usuário. Para usuários do Excel que muitas vezes precisam acessar uma grande quantidade de energia de processamento, a combinação de um XLL que usa MTR e um servidor de cálculo avançada fornece a solução de desempenho mais elevado.
  
### <a name="customizing-the-excel-user-interface"></a>Personalizando a interface de usuário do Excel

Para muitas versões do Excel, a API de C não tem sido a melhor opção para personalizar a interface do usuário. O VBA possui o melhor acesso a objetos e eventos do Excel. A interface do usuário introduzida no Excel 2007 é significativamente diferente das versões anteriores em aparência e tecnologia subjacente. É possível personalizar melhor esta interface usando recursos de código gerenciado.
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>Criando aplicativos que possam ser acessados pela Internet

Os Serviços do Excel, introduzidos com o sistema Microsoft Office 2007, oferecem a melhor maneira de conceder aos usuários acesso a pastas de trabalho e a funcionalidades do Excel usando ferramentas padrão do navegador da Web. Com linguagens e recursos de desenvolvimento do .NET Framework, essas tecnologias representam uma parte importante da implantação do Excel para usuários no futuro.
  
### <a name="controlling-excel-from-external-applications"></a>Controlando o Excel de aplicativos externos

O Excel expõe seus objetos, métodos e eventos por meio da interface COM. É possível, portanto, usar COM para criar aplicativos independentes que podem iniciar e controlar uma sessão do Excel ou controlar uma sessão existente do Excel. Acesse a interface do Excel exposta por COM em várias linguagens de desenvolvimento, incluindo C++ e VBA. Da mesma forma, o .NET Framework e C# fornecem uma interface para o Excel que permite acessar e controlar o Excel remotamente.
  
## <a name="asynchronous-calling-of-excel"></a>Chamada assíncrona do Excel

O Excel permite que XLLs chamem a API de C somente quando o Excel tiver passado o controle para o XLL. Uma função de planilha chamada pelo Excel pode fazer chamadas novamente para o Excel usando a API de C. Um comando XLL chamado pelo Excel pode chamar a API de C. Comandos e funções DLL e XLL chamados pelo VBA quando o próprio VBA tiver sido chamado pelo Excel podem chamar a API de C. Não é possível, por exemplo, definir um retorno de chamada de tempo limite do Windows no XLL e chamar a API de C dele. Também não é possível chamar a API de C de um thread em segundo plano criado pelo XLL. Não é recomendável chamar o Excel de forma assíncrona usando COM de uma DLL ou XLL.
  
Isso é muito limitador, já que podem haver aplicativos nos quais você deseja que o Excel reaja a um evento de forma assíncrona. Por exemplo, talvez você queira que o Excel recupere uma parte dos dados na Internet e recalcule sempre que esses dados forem alterados. Ou talvez você queira que um thread em segundo plano realize um cálculo e faça com que o Excel calcule novamente assim que ele for concluído.
  
Isso pode ser feito ao fazer com que o Excel sonde alterações ativamente, mas é ineficiente e limitador porque frequentemente envolve a interrupção da atividade normal do Excel. É possível configurar comandos repetidos com tempo limite usando a API de C ou o VBA, embora essa não seja a solução ideal.
  
A condição ideal seria ter um processo externo mais eficiente para verificar a alteração nos dados e que esse processo externo acionasse o Excel para recuperar a atualização e realizar um recálculo. É possível fazer isso usando um aplicativo que faz interface com o Excel usando COM. O COM não é restrito da mesma forma como a API de C para fazer chamadas somente quando o Excel tiver explicitamente passado o controle para ele.Os aplicativos COM podem chamar métodos do Excel sempre que o Excel estiver em um estado de prontidão, embora essas chamadas de método possam ser ignoradas se as caixas de diálogo estiverem sendo exibidas, quando os menus estiverem recolhidos ou quando uma macro estiver em execução.
  
## <a name="c-api-and-its-relation-to-xlm"></a>A API de C e sua relação com XLM

A linguagem de macro (XLM) do Excel foi o primeiro ambiente de programação acessível ao usuário fornecido no Excel. Ela permitia aos usuários criar funções e comandos personalizados em folhas de macro especiais parecidas com planilhas comuns. As folhas de macro XLM ainda são compatíveis com o Excel 2013. Use todas as funções de planilha de costume, como **SOMA** e **LOG** na folha de macro, além dos seguintes itens que não podem ser inseridos na planilha: 
  
- Funções de informação do espaço de trabalho, como **INFO.CÉL** e **INFO.PASTA.TRABALHO**.
    
- Funções equivalentes a comandos que permitem a automação de operações comuns de usuário, como **DEFINE.NAME** e **PASTE**.
    
- Funções relacionadas a suplementos como **REGISTRO**.
    
- Interceptações de eventos equivalentes a comandos como **ON.ENTRY** e **ON.TIME**.
    
- Operações específicas da função de macro como **ARGUMENTO** e **TEMPORÁRIO**.
    
- Operações de controle de fluxo como **IRPARA** e **RETORNO**.
    
Havia uma versão limitada da API de C no Excel versão 3. No entanto, no Excel versão 4, a linguagem XLM foi mapeada para a API de C. Desde então, as DLLs podem chamar todas as funções de planilha, comandos e funções de informação das folhas de macro e configurar interceptações de evento. As DLLs não podem chamar funções de controle de fluxo XLM de dentro da API de C. Esses comandos e funções de folhas de macro estão documentados no arquivo da Ajuda XLMacr8.hlp (anteriormente conhecido como Macrofun.hlp). Para obter este arquivo de ajuda, acesse o [Centro de Download da Microsoft](https://download.microsoft.com) e pesquise "XLMacr8.hlp". 
  
> [!NOTE]
> O Windows Vista e o Windows 7 não são diretamente compatíveis com arquivos .hlp, mas é possível baixar o [Programa da Ajuda do Windows (WinHlp32.exe) para Windows Vista](https://go.microsoft.com/fwlink/?LinkID=82148) ou o [Programa da Ajuda do Windows (WinHlp32.exe) para Windows 7](https://www.microsoft.com/download/en/details.aspx?id=91) da Microsoft para permitir que esses arquivos sejam abertos. 
  
As DLLs chamam equivalentes da API de C dessas funções e comandos, usando as funções de retorno de chamada **Excel4**, **Excel4v**, **Excel12** e **Excel12v** (sendo que as duas últimas funções foram introduzidas no Excel 2007). As constantes enumeradas que correspondem a cada função e comando são definidas em um arquivo de cabeçalho e passadas como um dos argumentos desses retornos de chamada. Por exemplo, **INFO.CÉL** é representada como **xlfGetCell**, **REGISTRO** como **xlfRegister** e **DEFINE.NAME** como **xlcDefineName**.
  
Além de fornecer as funções de planilha e as funções e comandos de folhas de macro, a API de C fornece enumerações de função e de comando que só podem ser chamadas usando esses retornos de chamada de dentro de uma DLL. Por exemplo, **xlGetName** permite que a DLL encontre por conta própria o caminho completo e o nome do arquivo, o que é necessário ao registrar funções e comandos com o Excel. 
  
Desde a introdução das folhas do Visual Basic for Applications (VBA) no Excel versão 5 e do Editor do Visual Basic (VBE) na versão 8 (Excel 97), a maneira mais fácil para os usuários personalizarem o Excel é usar o VBA em vez de o XLM. Consequentemente, muitas das novas funcionalidades apresentadas em versões posteriores do Excel estão disponíveis no VBA, mas não no XLM ou na API de C. Por exemplo, vários comandos, interceptações de eventos e recursos aprimorados de caixa de diálogo são disponibilizadas no VBA, mas não no XLM ou na API de C.
  
Para saber mais, confira [What's New in the C API for Excel](what-s-new-in-the-c-api-for-excel.md).
  
## <a name="see-also"></a>Confira também



[Novidades na API de C do Excel](what-s-new-in-the-c-api-for-excel.md)
  
[Retorno de chamada da API de C: funções Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)


[Introdução ao Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

