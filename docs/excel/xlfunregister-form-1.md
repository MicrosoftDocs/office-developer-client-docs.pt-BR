---
title: xlfUnregister (Formulário 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- função xlfunregister [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410081"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (Formulário 1)

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel. Isso equivale a chamar **Unregister** de uma folha de macro XLM do Excel. 
  
**xlfUnregister** pode ser chamado de duas formas: 
  
- Formulário 1: cancela o registro de um comando ou função individual.
    
- Formulário 2: descarrega e desativa um XLL.
    
Chamado no formato 1, essa função reduz a contagem de uso de uma função DLL ou de um comando que foi previamente registrado usando **xlfRegister** ou **Register**. Se a contagem de uso já for zero, essa função não terá efeito. Quando a contagem de uso de todas as funções em uma DLL chega a zero, a DLL é descarregada da memória.
  
**xlfRegister** (Form 1) também define um nome oculto que é o argumento de texto da função, _pxFunctionText_, e que é avaliado como a ID de registro de função ou comando. Ao cancelar o registro da função, esse nome deve ser excluído usando o **xlfSetName** para que o nome da função não seja mais listado pelo assistente de função. Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parâmetros

_pxRegisterId_ (**xltypeNum**)
  
A ID de registro da função a ser cancelada.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se bem-sucedido, retorna **true** (**xltypeBool**), caso contrário, retorna false.
  
## <a name="remarks"></a>Comentários

A ID de registro da função é retornada por **xlfRegister** quando a função é registrada pela primeira vez. Ela também pode ser obtida chamando-se a [função xlfRegisterId](xlfregisterid.md) ou a [função xlfEvaluate](xlfevaluate.md). Observe que xlfRegisterId tenta registrar a função se ela ainda não tiver sido registrada. Por esse motivo, se você estiver apenas tentando obter a ID para que possa cancelar o registro da função, é melhor obtê-la passando o nome registrado para **xlfEvaluate**. Se a função não tiver sido registrada, o **xlfEvaluate** falhará com um #NAME? erros. 
  
## <a name="example"></a>Exemplo

Consulte o código para a função **fExit** no `\SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a>Confira também

- [xlfRegister (Formulário 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formulário 2)](xlfunregister-form-2.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

