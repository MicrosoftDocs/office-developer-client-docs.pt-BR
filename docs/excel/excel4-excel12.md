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
- função Excel4 [excel 2007], função Excel12 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c7caf4923e336020928006f6838de5eaeba814a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586806"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função de planilha do Microsoft Excel interna, função de folha de macro ou comando, ou somente XLL função especial ou comando, a partir de dentro de um recurso de código ou DLL/XLL.
  
Suportam a todas as versões recentes do Excel **Excel4**. Iniciando no Excel 2007, **Excel12** é suportado. 
  
Essas funções podem ser chamadas apenas quando o Excel tiver passado o controle para a DLL ou XLL. Também pode ser chamados quando o Excel passou controle indiretamente por meio de uma chamada para o Visual Basic for Applications (VBA). Eles não podem ser chamados em qualquer outro momento. Por exemplo, eles não podem ser chamados durante as chamadas para a função [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) ou outros horários, quando o sistema operacional tem chamado a DLL ou de um segmento criado pela DLL. 
  
As funções [Excel4v e Excel12v](excel4v-excel12v.md) aceitam seus argumentos como uma matriz, enquanto as funções **Excel4** e **Excel12** aceitam seus argumentos como uma lista de comprimento variável na pilha. Em todos os outros aspectos, **Excel4** se comporta igual **Excel4v**e **Excel12** se comporta igual **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parâmetros

 _iFunction_ (**int**)
  
Um número que indica o comando, função ou função especial que você deseja chamar. Para obter uma lista de valores válidos _iFunction_ , consulte a seção de comentários a seguir. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Um ponteiro para uma **XLOPER** (com **Excel4**) ou uma **XLOPER12** (com **Excel12**) que irá armazenar o resultado da função avaliado.
  
 _iCount_ (**int**)
  
O número de argumentos subsequentes que serão passados para a função. Em versões do Excel até 2003, isso pode ser qualquer número entre 0 e 30. Iniciando no Excel 2007, isso pode ser qualquer número de 0 a 255.
  
 _Argumento1,..._ (**LPXLOPER** ou **LPXLOPER12**)
  
Os argumentos opcionais para a função. Todos os argumentos devem ser ponteiros para valores **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores inteiros (**int**).
  
|**Valor**|**Código de retorno**|**Descrição**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |A função foi chamada com êxito. Isso significa que a função não retornou um valor de erro do Excel; Para descobrir isso, você deve examinar o tipo e o valor do parâmetro _pxRes_ resultante.  <br/> |
|1  <br/> |**xlretAbort** <br/> |O comando ou a função foi finalizada de forma anormal (anulação interna). Isso pode acontecer se uma folha de macro XLM fecha a mesmo chamando **CLOSE**, ou se o Excel está sem memória. Se o Excel retorna este erro, a função de chamada deve sair imediatamente. A DLL tem permissão para chamar **xlFree** somente antes de sair. Todas as outras chamadas à API C não são permitidas. O usuário poderá salvar qualquer trabalho interativamente usando o comando **Salvar** no menu **arquivo** .  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Um número de função inválido foi fornecido. Se você estiver usando constantes do arquivo de cabeçalho do xlcall. h, isso não deve ocorrer, a menos que você está chamando algo que não há suporte para a versão do Excel que você está executando.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Um número inválido de argumentos foi inserido. Nas versões até o Excel 2003, o número máximo de argumentos que pode ser realizadas por qualquer função é 30. Iniciando no Excel 2007, o número máximo é 255. Alguns exigir um número fixo ou mínimo de argumentos.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Um **XLOPER** ou o **XLOPER12** inválido foi passado para a função ou um argumento de tipo incorreto foi usado.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Estouro de pilha. Use **xlStack** para monitorar a quantidade de sala esquerda na pilha. Evitar a alocação muito grandes matrizes de (automáticos) locais e estruturas na pilha de onde for possível; torná-los estático. (Observe que um estouro de pilha pode ocorrer sem ser detectado).  <br/> |
|32  <br/> |**xlretFailed** <br/> |Uma função equivalente do comando falhou. Isso é equivalente a um comando de macro exibindo a caixa de diálogo alerta de erro de macro.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Foi feita uma tentativa a referência a uma célula que não foi calculada ainda, pois ele está agendado para ser recalculada após a célula atual. Nesse caso, a DLL deve retornar controle para o Excel imediatamente. A DLL tem permissão para chamar **xlFree** somente antes de sair. Todas as outras chamadas à API C não são permitidas. Para obter mais informações sobre quais funções podem e não podem acessar os valores das células que não foram recalculados, consulte [Excel comandos, funções e estados](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Foi feita uma tentativa para chamar uma função que não é ou não pode ser, thread-safe durante um recálculo multithreaded da pasta de trabalho.  <br/> Iniciando no Excel 2007, esse valor é retornado e somente dentro de funções de planilha XLL declaradas como acesso thread-safe.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |O identificador de função assíncronas é inválido.  <br/> Esse valor é usado somente pelo Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |A chamada não é suportada em clusters.  <br/> Esse valor é usado somente pelo Excel 2010.  <br/> |
   
## <a name="remarks"></a>Comentários

### <a name="valid-ifunction-values"></a>Valores válidos iFunction

Valores válidos **iFunction** são quaisquer das constantes **xlf …** ou **xlc …** definidas no arquivo de cabeçalho do xlcall. h ou qualquer uma das seguintes funções especiais. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Diferentes tipos de funções

 **Excel4** e **Excel12** distinguir entre três classes de funções. As funções são classificadas de acordo com os três estados em que o Excel pode chamar a DLL. 
  
- Classe 1 se aplica quando a DLL é chamada de uma planilha como resultado de recálculo. 
    
- Classe 2 se aplica quando a DLL é chamada de dentro de uma macro de função ou de uma planilha em que ele foi registrado com um sinal de número (#) no texto tipo.
    
- Classe 3 se aplica quando uma DLL é chamada de um objeto, macro, menu, barra de ferramentas, tecla de atalho, método **ExecuteExcel4Macro** ou o comando de **Execução/de Macro de ferramentas** . Para obter mais informações, consulte [Excel comandos, funções e estados](excel-commands-functions-and-states.md).
    
A tabela a seguir mostra quais funções são válidas em cada classe.
  
|**Classe 1**|**Classe 2**|**Classe 3**|
|:-----|:-----|:-----|
|Qualquer função de planilha  <br/> Qualquer função somente XLL **xl …** exceto **xlSet**.  <br/> **xlfCaller** <br/> |Qualquer função de planilha  <br/> Qualquer função do **xl …** exceto **xlSet**.  <br/> Macro folha funções, incluindo **xlfCaller**, que retornam um valor, mas executam nenhuma ação que afeta o espaço de trabalho ou qualquer pasta de trabalho aberta.  <br/> |Qualquer função, incluindo **xlSet** e funções de comando equivalente.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Exibir a caixa de diálogo para uma função equivalente de comando

Se uma função equivalente do comando tiver uma caixa de diálogo associada, você pode definir o bit **xlPrompt** no **iFunction**. Isso significa que o Excel exibe a caixa de diálogo apropriada antes de executar o comando.
  
### <a name="writing-international-dlls"></a>Gravando DLLs internacionais

Se você definir o bit **xlIntl** no **iFunction**, a função ou o comando é realizado como se ele estava sendo chamado a partir de uma folha de Macro internacional. Isso significa que o comando se comporta como faria na versão dos EUA do Excel, mesmo se ele é executado em uma versão (localizada) internacional.
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced ou xlretAbort

Após receber um desses valores de retorno, sua DLL deve limpar e retorne imediatamente o controle para o Excel. Retornos de chamada para o Excel por meio da API C, exceto **xlFree**, estão desabilitados após receber um desses valores de retorno.
  
## <a name="example"></a>Exemplo

O exemplo a seguir usa a função **Excel12** para selecionar a célula do qual ele foi chamado. 
  
Este exemplo de código é parte de um exemplo maior fornecido no SDK do Excel 2010 XLL, no seguinte local onde você instalou o SDK:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Essa função chama uma macro de comando (xlcSelect) e, portanto, funciona somente se ele for chamado a partir de uma folha de macro XLM. 
  
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

