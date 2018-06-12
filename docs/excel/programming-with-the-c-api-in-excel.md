---
title: Programa��o com a API de C no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
localization_priority: Normal
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 459e57d41ef7497c535e51944bbaf24daee84167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765431"
---
# <a name="programming-with-the-c-api-in-excel"></a>Programa��o com a API de C no Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Use o XLL Software Development Kit e a API de C do Microsoft Excel 2013 para criar fun��es de planilha de alto desempenho para o Excel 2013. As atualiza��es para a API de C do Excel 2013 refletem o suporte cont�nuo para usu�rios para os quais o desempenho da funcionalidade de terceiros ou interna � essencial.
  
## <a name="excel-programming-interfaces"></a>Interfaces de Programa��o do Excel

O Excel oferece v�rias op��es para o desenvolvimento de aplicativos que fazem interface com ele. As interfaces de programa��o do Excel foram adicionadas �s vers�es anteriores na seguinte ordem:
  
- **Linguagem de macro XLM:** A primeira linguagem acess�vel ao usu�rio para a extens�o do Excel e a base da API de C. Embora ainda ofere�a suporte para o Excel�2010, o XLM foi substitu�do pelo Visual Basic for Applications (VBA) h� muito tempo. 
    
- **API de C e XLLs:** As DLLs s�o integradas ao Excel. Essas DLLs oferecem a interface mais r�pida e mais direta para a adi��o de fun��es de planilha de alto desempenho, embora �s custas de alguma complexidade em compara��o com as tecnologias mais recentes. 
    
- **VBA:** Objetos de c�digo do Visual Basic que est�o associados a objetos de pasta de trabalho do Excel. O VBA permite intercepta��es de eventos, a personaliza��o e a adi��o de fun��es e comandos definidos pelo usu�rio. O VBA � a mais comumente usada e a mais facilmente dispon�vel das op��es de extensibilidade. 
    
- **COM:** O padr�o de interoperabilidade de aplicativos baseados no Windows por meio do qual o Excel exp�e seus eventos e objetos. O VBA usa COM para interagir com o Excel. O Excel exporta bibliotecas de tipo COM que podem ajud�-lo a criar recursos e aplicativos de c�digo C++ COM que podem controlar o Excel externamente. 
    
- **O Microsoft .NET Framework:** O ambiente de c�digo gerenciado para v�rias linguagens projetado para o desenvolvimento r�pido de aplicativos para ambientes distribu�dos. A linguagem de programa��o prim�ria para c�digo baseada no .NET Framework � C#, embora muitas linguagens possam ser compiladas para a linguagem intermedi�ria da Microsoft (MSIL). O Excel 2013 pode acessar recursos de c�digo contidos em assemblies do .NET Framework. 
    
## <a name="when-to-use-the-c-api"></a>Quando Usar a API de C

A principal raz�o para gravar XLLs e usar a API de C � criar fun��es de planilha de alto desempenho. Embora as fun��es XLL sejam frequentemente chamadas de definidas pelo usu�rio, o investimento em tempo para obter o entendimento e as habilidades necess�rias para gravar XLLs fazem com que essa tecnologia n�o seja pr�tica para a maioria dos usu�rios. No entanto, os aplicativos de fun��es de alto desempenho, e no Excel 2013, a capacidade de gravar interfaces de v�rios threads em recursos avan�ados do servidor, fazem disso uma parte muito importante da extensibilidade do Excel. 
  
A revis�o da API de C introduzida no Excel 2007 trata principalmente dos aspectos relacionados a c�lculos de alto desempenho, em vez de recursos como a interface do usu�rio.
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>Gravando fun��es de planilha de alto desempenho definidas pelo usu�rio

A API de C do Excel � a op��o ideal quando voc� deseja criar fun��es de planilha de alto desempenho criando suplementos XLL. A API de C oferece o acesso mais direto aos dados da planilha. Os XLLs oferecem ao Excel o acesso mais direto aos recursos da DLL. O desempenho dos XLLs foi ainda mais aprimorado no Excel 2013 com a adi��o de novos tipos de dados e, o mais importante, oferece suporte para a execu��o de fun��es definidas pelo usu�rio em servidores clusterizados.
  
Trabalhar com XLLs tem um pre�o: A API de C n�o tem os recursos de desenvolvimento r�pido de n�vel superior do VBA, COM ou o .NET Framework. O gerenciamento de mem�ria � de n�vel baixo e, portanto,atribui uma maior responsabilidade ao desenvolvedor. Muitos recursos do Excel que s�o expostos pelo COM, tornando-os dispon�veis por meio do VBA e o .NET Framework, n�o s�o expostos � API de C.
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>Acessando Servidores de V�rios Threads Usando Fun��es de Planilha XLL

O rec�lculo de v�rios threads (MTR), que foi introduzido no Excel 2007, permite criar fun��es de planilha XLL seguras para threads. Use essas fun��es para acessar servidores de v�rios threads. As se��es posteriores descrevem com mais detalhes como isso pode aumentar significativamente o desempenho observado pelo usu�rio. Para usu�rios do Excel que muitas vezes precisam acessar uma grande quantidade de energia de processamento, a combina��o de um XLL que usa MTR e um servidor de c�lculo avan�ada fornece a solu��o de desempenho mais elevado.
  
### <a name="customizing-the-excel-user-interface"></a>Personalizando a interface de usu�rio do Excel

Para muitas vers�es do Excel, a API de C n�o tem sido a melhor op��o para personalizar a interface do usu�rio. O VBA possui o melhor acesso a objetos e eventos do Excel. A interface do usu�rio introduzida no Excel 2007 � significativamente diferente das vers�es anteriores em apar�ncia e tecnologia subjacente. � poss�vel personalizar melhor esta interface usando recursos de c�digo gerenciado.
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>Criando aplicativos que possam ser acessados pela Internet

Os Servi�os do Excel, introduzidos com o sistema Microsoft Office de 2007, oferecem a melhor maneira de conceder aos usu�rios acesso a pastas de trabalho e a funcionalidades do Excel usando ferramentas padr�o do navegador da Web. Com linguagens e recursos de desenvolvimento do .NET Framework, essas tecnologias representam uma parte importante da implanta��o do Excel para usu�rios no futuro.
  
### <a name="controlling-excel-from-external-applications"></a>Controlando o Excel de aplicativos externos

O Excel exp�e seus objetos, m�todos e eventos por meio da interface COM. � poss�vel, portanto, usar COM para criar aplicativos independentes que podem iniciar e controlar uma sess�o do Excel ou controlar uma sess�o existente do Excel. Acesse a interface do Excel exposta por COM em v�rias linguagens de desenvolvimento, incluindo C++ e VBA. Da mesma forma, o .NET Framework e C# fornecem uma interface para o Excel que permite acessar e controlar o Excel remotamente.
  
## <a name="asynchronous-calling-of-excel"></a>Chamada ass�ncrona do Excel

O Excel permite que XLLs chamem a API de C somente quando o Excel tiver passado o controle para o XLL. Uma fun��o de planilha chamada pelo Excel pode fazer chamadas novamente para o Excel usando a API de C. Um comando XLL chamado pelo Excel pode chamar a API de C. Comandos e fun��es DLL e XLL chamados pelo VBA quando o pr�prio VBA tiver sido chamado pelo Excel podem chamar a API de C. N�o � poss�vel, por exemplo, definir um retorno de chamada de tempo limite do Windows no XLL e chamar a API de C dele. Tamb�m n�o � poss�vel chamar a API de C de um thread em segundo plano criado pelo XLL. N�o � recomend�vel chamar o Excel de forma ass�ncrona usando COM de um DLL ou XLL.
  
Isso � muito limitador, j� que podem haver aplicativos nos quais voc� deseja que o Excel reaja a um evento de forma ass�ncrona. Por exemplo, talvez voc� queira que o Excel recupere uma parte dos dados na Internet e recalcule sempre que esses dados forem alterados. Ou talvez voc� queira que um thread em segundo plano realize um c�lculo e fa�a com que o Excel calcule novamente assim que ele for conclu�do.
  
Isso pode ser feito ao fazer com que o Excel sonde altera��es ativamente, mas � ineficiente e limitador porque frequentemente envolve a interrup��o da atividade normal do Excel. � poss�vel configurar comandos repetidos com tempo limite usando a API de C ou o VBA, embora isso n�o seja uma solu��o ideal.
  
A condi��o ideal seria ter um processo externo mais eficiente para verificar a altera��o nos dados e que esse processo externo acionasse o Excel para recuperar a atualiza��o e realizar um rec�lculo. � poss�vel fazer isso usando um aplicativo que faz interface com o Excel usando COM. O COM n�o � restrito da mesma forma como a API de C para fazer chamadas somente quando o Excel tiver explicitamente passado o controle para ele. Os aplicativos COM podem chamar m�todos do Excel sempre que o Excel estiver em um estado de prontid�o, embora essas chamadas de m�todo possam ser ignoradas se as caixas de di�logo estiverem sendo exibidas, quando os menus estiverem recolhidos ou quando uma macro estiver em execu��o.
  
## <a name="c-api-and-its-relation-to-xlm"></a>A API de C e sua rela��o com XLM

A linguagem de macro (XLM) do Excel foi o primeiro ambiente de programa��o acess�vel ao usu�rio fornecido no Excel. Ele permitia aos usu�rios criar fun��es e comandos personalizados em folhas de macro especiais parecidas com planilhas comuns. As folhas de macro XLM ainda t�m suporte no Excel 2013. Use todas as fun��es de planilha normais como **SUM** e **LOG** em uma folha de macro, al�m dos itens a seguir que n�o podem ser inseridos em uma planilha: 
  
- Fun��es de informa��o do espa�o de trabalho como **GET.CELL** e **GET.WORKBOOK**.
    
- Fun��es equivalentes a comandos que permitem a automa��o de opera��es comuns de usu�rios como **DEFINE.NAME** e **PASTE**.
    
- Fun��es relacionadas a suplementos como **REGISTER**.
    
- Intercepta��es de eventos equivalentes a comandos como **ON.ENRTY** e **ON.TIME**.
    
- Opera��es espec�ficas da fun��o de macro como **ARGUMENT** e **VOLATILE**.
    
- Opera��es de controle de fluxo como **GOTO** e **RETURN**.
    
No Excel vers�o 3, havia uma vers�o limitada da API de C. No entanto, no Excel vers�o 4, a linguagem XLM foi mapeada para a API de C. Desde ent�o, os DLLs podem chamar todas as fun��es de planilha, comandos e fun��es de informa��o das folhas de macro e configurar intercepta��es de evento. Os DLLs n�o podem chamar fun��es de controle de fluxo XLM de dentro da API de C. Esses comandos e fun��es de folhas de macro est�o documentados no arquivo da Ajuda XLMacr8.hlp (anteriormente conhecido como Macrofun.hlp). Para obter esse arquivo de ajuda, v� para o [Centro de Download da Microsoft](http://download.microsoft.com) e procure por "XLMacr8.hlp". 
  
> [!NOTE]
> [!OBSERVA��O] O Windows Vista e o Windows 7 n�o s�o diretamente compat�veis com arquivos .hlp, mas � poss�vel baixar o [Programa da Ajuda do Windows (WinHlp32.exe) para Windows Vista](http://go.microsoft.com/fwlink/?LinkID=82148) ou o [Programa da Ajuda do Windows (WinHlp32.exe) para Windows 7](http://www.microsoft.com/download/en/details.aspx?id=91) da Microsoft para permitir que esses arquivos sejam abertos. 
  
Os DLLs chamam equivalentes da API de C dessas fun��es e comandos usando as fun��es de retorno de chamada **Excel4**, **Excel4v**, **Excel12** e **Excel12v** (sendo que as duas �ltimas fun��es foram introduzidas no Excel 2007). As constantes enumeradas que correspondem a cada fun��o e comando s�o definidas em um arquivo de cabe�alho e passadas como um dos argumentos desses retornos de chamada. Por exemplo, **GET.CELL** � representado por **xlfGetCell**, **REGISTER** pelo **xlfRegister** e **DEFINE.NAME** pelo **xlcDefineName**.
  
Al�m de fornecer as fun��es de planilha e as fun��es e comandos de folhas de macro, a API de C fornece enumera��es de fun��o e de comando que s� podem ser chamadas usando esses retornos de chamada de dentro de um DLL. Por exemplo, o **xlGetName** habilita o DLL a descobrir seu pr�prio nome de arquivo e caminho completo, necess�rios quando voc� registra comandos e fun��es com o Excel. 
  
Desde a introdu��o das folhas do Visual Basic for Applications (VBA) no Excel vers�o 5 e do Editor do Visual Basic (VBE) na vers�o 8 (Excel 97), a maneira mais f�cil para os usu�rios personalizarem o Excel � usar o VBA em vez de o XLM. Consequentemente, muitas das novas funcionalidades apresentadas em vers�es posteriores do Excel est�o dispon�veis no VBA, mas n�o no XLM ou na API de C. Por exemplo, v�rios comandos, intercepta��es de eventos e recursos aprimorados de caixa de di�logo s�o disponibilizadas no VBA, mas n�o no XLM ou na API de C.
  
Para saber mais, confira [What's New in the C API for Excel](what-s-new-in-the-c-api-for-excel.md).
  
## <a name="see-also"></a>Ver tamb�m



[What's New in the C API for Excel](what-s-new-in-the-c-api-for-excel.md)
  
[C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)


[Getting Started with the Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

