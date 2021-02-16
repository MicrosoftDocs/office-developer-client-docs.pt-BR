---
title: Excel4/Excel12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12
- Excel4
keywords:
- função excel4 [excel 2007],função Excel12 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429443"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função de planilha interna do Microsoft Excel, função ou comando de planilha de macro ou comando especial somente XLL, de dentro de um DLL/XLL ou recurso de código.
  
Todas as versões recentes do Excel suportam **Excel4**. A partir do Excel 2007, **o Excel12** é suportado. 
  
Essas funções podem ser chamadas somente quando o Excel tiver passado o controle para a DLL ou XLL. Eles também podem ser chamados quando o Excel tiver passado pelo controle indiretamente por meio de uma chamada para o VBA (Visual Basic for Applications). Eles não podem ser chamados em nenhum outro momento. Por exemplo, eles não podem ser chamados durante chamadas para a função [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) ou outras vezes quando o sistema operacional tiver chamado a DLL ou de um thread criado pela DLL. 
  
As funções [Excel4v e Excel12v](excel4v-excel12v.md) aceitam seus argumentos como uma matriz, enquanto as funções **Excel4** e **Excel12** aceitam seus argumentos como uma lista de comprimento variável na pilha. Em todos os outros aspectos, **o Excel4** se comporta da mesma forma que o **Excel4v** e o **Excel12** se comporta da mesma forma que o **Excel12v.**
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parâmetros

 _iFunction_ (**int**)
  
Um número que indica o comando, a função ou a função especial que você deseja chamar. Para uma lista de valores  _válidos de iFunction,_ consulte a seção Comentários a seguir. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Um ponteiro para um **XLOPER** (com **Excel4**) ou um **XLOPER12** (com **Excel12**) que conterá o resultado da função avaliada.
  
 _iCount_ (**int**)
  
O número de argumentos subsequentes que serão passados para a função. Em versões do Excel até 2003, pode ser qualquer número de 0 a 30. A partir do Excel 2007, pode ser qualquer número entre 0 e 255.
  
 _argumento1, ..._ (**LPXLOPER** ou **LPXLOPER12**)
  
Os argumentos opcionais para a função. Todos os argumentos devem ser ponteiros para **valores XLOPER** ou **XLOPER12.** 
  
## <a name="return-value"></a>Valor de retorno

Retorna um dos seguintes valores inteiros **(int).**
  
|**Valor**|**Código de retorno**|**Descrição**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |A função foi chamada com êxito. Isso não significa que a função não retornou um valor de erro do Excel; para descobrir isso, você deve ver o tipo e o valor do parâmetro  _pxRes_ resultante.  <br/> |
|1   <br/> |**xlretAbort** <br/> |O comando ou a função foi encerrado de forma anormal (anulação interna). Isso pode ocorrer se uma folha de macro XLM se fechar chamando **CLOSE** ou se o Excel estiver sem memória. Se o Excel retornar esse erro, a função de chamada deverá sair imediatamente. A DLL tem permissão para chamar **xlFree** somente antes de sair. Todas as outras chamadas para a API de C não são permitidas. O usuário pode salvar qualquer trabalho interativamente usando o comando **Salvar** **no** menu Arquivo.  <br/> |
|2   <br/> |**xlretInvXlfn** <br/> |Um número de função inválido foi fornecido. Se você estiver usando constantes do arquivo de header Xlcall.h, isso não deve ocorrer, a menos que você esteja chamando algo que não é suportado na versão do Excel que você está executando.  <br/> |
|4   <br/> |**xlretInvCount** <br/> |Um número inválido de argumentos foi inserido. Em versões até o Excel 2003, o número máximo de argumentos que qualquer função pode levar é 30. A partir do Excel 2007, o número máximo é 255. Alguns exigem um número fixo ou mínimo de argumentos.  <br/> |
|8   <br/> |**xlretInvXloper** <br/> |Um **XLOPER ou** **XLOPER12 inválido** foi passado para a função ou um argumento do tipo errado foi usado.  <br/> |
|16   <br/> |**xlretStackOvfl** <br/> |Ocorreu um estouro de pilha. Use **xlStack** para monitorar a quantidade de espaço à esquerda na pilha. Evite alocar estruturas e matrizes locais (automáticas) muito grandes na pilha sempre que possível; torná-los estáticos. (Observe que um estouro de pilha pode ocorrer sem ser detectado.)  <br/> |
|32  <br/> |**xlretFailed** <br/> |Falha na função equivalente ao comando. Isso equivale a um comando de macro exibindo a caixa de diálogo de alerta de erro de macro.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Foi feita uma tentativa de desreferência de uma célula que ainda não foi calculada, porque ela está agendada para ser recalculada após a célula atual. Nesse caso, a DLL deve retornar o controle para o Excel imediatamente. A DLL tem permissão para chamar **xlFree** somente antes de sair. Todas as outras chamadas para a API de C não são permitidas. Para obter mais informações sobre quais funções podem ou não acessar os valores das células que não foram recalculadas, consulte Comandos, Funções e Estados do [Excel.](excel-commands-functions-and-states.md)  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Foi feita uma tentativa de chamar uma função que não é ou pode não ser thread-safe durante um recálculo multithread da plano de trabalho.  <br/> A partir do Excel 2007, esse valor é retornado e somente nas funções de planilha XLL declaradas como thread-safe.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |A alça da função assíncrona é inválida.  <br/> Esse valor é usado somente pelo Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |A chamada não é suportada em clusters.  <br/> Esse valor é usado somente pelo Excel 2010.  <br/> |
   
## <a name="remarks"></a>Comentários

### <a name="valid-ifunction-values"></a>Valores válidos de iFunction

Os **valores iFunction** válidos são qualquer uma das constantes **xlf...** ou **xlc...** definidas no arquivo de header Xlcall.h ou em qualquer uma das funções especiais a seguir. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Tipos diferentes de funções

 **Excel4** e **Excel12** distinguem entre três classes de funções. As funções são classificadas de acordo com os três estados nos quais o Excel pode chamar a DLL. 
  
- A classe 1 se aplica quando a DLL é chamada de uma planilha como resultado do recálculo. 
    
- A classe 2 se aplica quando a DLL é chamada de dentro de uma macro de função ou de uma planilha onde foi registrada com um sinal de número (#) no texto do tipo.
    
- A classe 3 se aplica quando uma DLL é chamada de um objeto, macro, menu, barra de ferramentas, tecla de atalho, **método ExecuteExcel4Macro** ou o comando **Ferramentas/Macro/Executar.** Para saber mais, confira [Comandos, Funções e Estados do Excel.](excel-commands-functions-and-states.md)
    
A tabela a seguir mostra quais funções são válidas em cada classe.
  
|**Classe 1**|**Classe 2**|**Classe 3**|
|:-----|:-----|:-----|
|Qualquer função de planilha  <br/> Qualquer função xl somente **XLL...** exceto **xlSet**.  <br/> **xlfCaller** <br/> |Qualquer função de planilha  <br/> Qualquer **função xl...** exceto **xlSet**.  <br/> Funções de planilha de macro, incluindo **xlfCaller**, que retornam um valor, mas não executam nenhuma ação que afete o espaço de trabalho ou qualquer pasta de trabalho aberta.  <br/> |Qualquer função, incluindo **xlSet** e funções equivalentes de comando.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Exibindo a caixa de diálogo para uma Command-Equivalent função

Se uma função equivalente de comando tiver uma caixa de diálogo associada, você poderá definir o bit **xlPrompt** em **iFunction**. Isso significa que o Excel exibe a caixa de diálogo apropriada antes de realizar o comando.
  
### <a name="writing-international-dlls"></a>Escrevendo DLLs Internacionais

Se você definir o **bit xlIntl** em **iFunction**, a função ou o comando será executado como se estivesse sendo chamado de uma Planilha de Macro Internacional. Isso significa que o comando se comporta como faria na versão americana do Excel, mesmo que ele seja executado em uma versão internacional (localizada).
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced ou xlretAbort

Depois de receber um desses valores de retorno, sua DLL deve limpar e retornar o controle para o Excel imediatamente. Retornos de chamada no Excel por meio da API de C, exceto **xlFree**, são desabilitados depois de receber um desses valores de retorno.
  
## <a name="example"></a>Exemplo

O exemplo a seguir usa **a função Excel12** para selecionar a célula da qual foi chamada. 
  
Este exemplo de código faz parte de um exemplo maior fornecido no Excel 2010 XLL SDK, no seguinte local onde você instalou o SDK:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Esta função chama uma macro de comando (xlcSelect) e, portanto, funciona somente se for chamada de uma folha de macro XLM. 
  
```cs
short WINAPI Excel12Example(void)
{
    XLOPER12 xRes;
    Excel12(xlfCaller, &xRes, 0);
    Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Confira também



[Excel4v/Excel12v](excel4v-excel12v.md)

