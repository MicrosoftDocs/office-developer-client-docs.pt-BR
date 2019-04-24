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
- função Excel4 [Excel 2007], função Excel12 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304106"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função de planilha interna do Microsoft Excel, comando ou comando de folha de macro, ou somente função especial ou comando de XLL, de dentro de uma DLL/XLL ou de um recurso de código.
  
Todas as versões recentes do Excel dão suporte a **Excel4**. A partir do Excel 2007, há suporte para **Excel12** . 
  
Essas funções podem ser chamadas somente quando o Excel tiver passado controle para a DLL ou XLL. Eles também podem ser chamados quando o Excel tiver passado controle indiretamente por meio de uma chamada para Visual Basic for Applications (VBA). Eles não podem ser chamados em nenhum outro momento. Por exemplo, eles não podem ser chamados durante chamadas para a função [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) ou outras vezes quando o sistema operacional chamou a dll ou de um thread criado pela dll. 
  
As funções [Excel4v e Excel12v](excel4v-excel12v.md) aceitam seus argumentos como uma matriz, enquanto as funções **Excel4** e **Excel12** aceitam seus argumentos como uma lista de comprimento variável na pilha. Em todos os outros aspectos, o **Excel4** comporta o mesmo que **Excel4v**e **Excel12** se comporta da mesma forma que **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parâmetros

 _iFunction_ (**int**)
  
Um número que indica o comando, a função ou a função especial que você deseja chamar. Para obter uma lista de valores de _iFunction_ válidos, consulte a seção comentários a seguir. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Um ponteiro para um **XLOPER** (com **Excel4**) ou um **XLOPER12** (com **Excel12**) que irá armazenar o resultado da função avaliada.
  
 _iCount_ (**int**)
  
O número de argumentos subsequentes que serão passados para a função. Em versões do Excel até 2003, pode ser qualquer número de 0 a 30. A partir do Excel 2007, pode ser qualquer número de 0 a 255.
  
 _argument1,..._ (**LPXLOPER** ou **LPXLOPER12**)
  
Os argumentos opcionais para a função. Todos os argumentos devem ser ponteiros para valores **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valor de retorno

Retorna um dos seguintes valores inteiros (**int**).
  
|**Valor**|**Código de retorno**|**Descrição**|
|:-----|:-----|:-----|
|,0  <br/> |**xlretSuccess** <br/> |A função foi chamada com êxito. Isso não significa que a função não retornou um valor de erro do Excel; para descobrir isso, você deve examinar o tipo e o valor do parâmetro _pxRes_ resultante.  <br/> |
|1  <br/> |**xlretAbort** <br/> |O comando ou função foi encerrado de forma anormal (anulação interna). Isso pode ocorrer se uma folha de macro XLM se fechar ao chamar **Close**ou se o Excel estiver sem memória. Se o Excel retornar esse erro, a função de chamada deverá sair imediatamente. A DLL tem permissão para chamar **xlFree** apenas antes de sair. Todas as outras chamadas para a API de C não são permitidas. O usuário pode salvar qualquer trabalho interativamente usando o comando **salvar** no menu **arquivo** .  <br/> |
|duas  <br/> |**xlretInvXlfn** <br/> |Um número de função inválido foi fornecido. Se você estiver usando constantes do arquivo de cabeçalho xlcall. h, isso não deve ocorrer, a menos que você esteja chamando algo que não é suportado na versão do Excel que você está executando.  <br/> |
|quatro  <br/> |**xlretInvCount** <br/> |Um número inválido de argumentos foi inserido. Nas versões até o Excel 2003, o número máximo de argumentos que qualquer função pode levar é 30. A partir do Excel 2007, o número máximo é 255. Alguns exigem um número fixo ou mínimo de argumentos.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Um **XLOPER** ou **XLOPER12** inválido foi passado para a função ou um argumento do tipo incorreto foi usado.  <br/> |
|dezesseis  <br/> |**xlretStackOvfl** <br/> |Um estouro de pilha ocorreu. Use **xlStack** para monitorar a quantidade de espaço restante na pilha. Evite alocar matrizes locais e estruturas (automáticas) muito grandes na pilha, onde for possível; torná-los estáticos. (Observe que um estouro de pilha pode ocorrer sem ser detectado.)  <br/> |
|32  <br/> |**xlretFailed** <br/> |Uma função de comando equivalente falhou. Isso equivale a um comando de macro que exibe a caixa de diálogo de alerta de erro de macro.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Foi feita uma tentativa de cancelar a referência de uma célula que ainda não foi calculada, pois ela está agendada para ser recalculada após a célula atual. Nesse caso, a DLL deve retornar o controle para o Excel imediatamente. A DLL tem permissão para chamar **xlFree** apenas antes de sair. Todas as outras chamadas para a API de C não são permitidas. Para obter mais informações sobre quais funções podem ou não acessar os valores das células que não foram recalculadas, consulte [comandos, funções e Estados do Excel](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Foi feita uma tentativa de chamar uma função que não é, ou pode não ser, thread-safe durante um recálculo de vários threads da pasta de trabalho.  <br/> A partir do Excel 2007, esse valor é retornado e somente dentro das funções de planilha XLL declaradas como thread-safe.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |O identificador de função assíncrona é inválido.  <br/> Esse valor é usado apenas pelo Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |Não há suporte para a chamada em clusters.  <br/> Esse valor é usado apenas pelo Excel 2010.  <br/> |
   
## <a name="remarks"></a>Comentários

### <a name="valid-ifunction-values"></a>Valores válidos do iFunction

Os valores válidos do **iFunction** são qualquer uma das constantes **XLF...** ou **xlC...** definidas no arquivo de cabeçalho xlcall. h ou em qualquer uma das seguintes funções especiais. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Diferentes tipos de funções

 **Excel4** e **Excel12** distinguem entre três classes de funções. As funções são classificadas de acordo com os três Estados nos quais o Excel pode chamar a DLL. 
  
- A classe 1 se aplica quando a DLL é chamada a partir de uma planilha como resultado de recálculo. 
    
- A classe 2 se aplica quando a DLL é chamada a partir de uma macro de função ou de uma planilha onde foi registrada com um sinal de número (#) no texto do tipo.
    
- A classe 3 se aplica quando uma DLL é chamada a partir de um objeto, macro, menu, barra de ferramentas, tecla de atalho, método **ExecuteExcel4Macro** ou o comando **ferramentas/macro/executar** . Para obter mais informações, consulte [comandos, funções e Estados do Excel](excel-commands-functions-and-states.md).
    
A tabela a seguir mostra quais funções são válidas em cada classe.
  
|**Classe 1**|**Classe 2**|**Classe 3**|
|:-----|:-----|:-----|
|Qualquer função de planilha  <br/> Qualquer função **XL...** somente XLL exceto **xlSet**.  <br/> **xlfCaller** <br/> |Qualquer função de planilha  <br/> Qualquer função **XL...** exceto **xlSet**.  <br/> Funções de folha de macro, incluindo **xlfCaller**, que retornam um valor mas não executam nenhuma ação que afete o espaço de trabalho ou qualquer pasta de trabalho aberta.  <br/> |Qualquer função, incluindo **xlSet** e funções equivalentes a comandos.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Exibindo a caixa de diálogo de uma função de comando equivalente

Se uma função de comando equivalente tiver uma caixa de diálogo associada, você poderá definir o bit **xlPrompt** em **iFunction**. Isso significa que o Excel exibe a caixa de diálogo apropriada antes de executar o comando.
  
### <a name="writing-international-dlls"></a>Escrevendo DLLs internacionais

Se você definir o bit **xlIntl** em **iFunction**, a função ou o comando será executado como se estivesse sendo chamado de uma folha de macro internacional. Isso significa que o comando se comporta como faria na versão norte-americana do Excel, mesmo que esteja em execução em uma versão internacional (localizada).
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced ou xlretAbort

Após receber um desses valores de retorno, sua DLL deve limpar e retornar o controle para o Excel imediatamente. Os retornos de chamada no Excel por meio da API C, exceto **xlFree**, são desabilitados depois de receber um desses valores de retorno.
  
## <a name="example"></a>Exemplo

O exemplo a seguir usa a função **Excel12** para selecionar a célula da qual ela foi chamada. 
  
Este exemplo de código é parte de um exemplo maior fornecido no Excel 2010 XLL SDK, no seguinte local onde você instalou o SDK:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Essa função chama uma macro de comando (xlcSelect) e, portanto, funciona somente se for chamado a partir de uma folha de macro XLM. 
  
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

