---
title: xlfUnregister (Formulário 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- função xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765473"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (Formulário 1)

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado a partir de um comando DLL ou XLL próprio foi chamado pelo Microsoft Excel. Isso é equivalente a chamar **cancela o registro** de uma folha de macro do Excel XLM. 
  
**xlfUnregister** pode ser chamado de duas formas: 
  
- Formulário 1: Cancela o registro de um comando individual ou uma função.
    
- Formulário 2: Descarrega e desativa um XLL.
    
Chamado no formulário 1, essa função reduz a contagem de uso de uma função DLL ou o comando que foi registrado anteriormente usando **xlfRegister** ou **registrar**. Se a contagem de uso já for zero, essa função não tem efeito. Quando a contagem de uso de todas as funções em uma DLL chega a zero, a DLL seja descarregada da memória.
  
**xlfRegister** (Forma 1) também define um nome oculto, que é o argumento de texto de função, _pxFunctionText_, e que avalia para a função ou a ID de registro. do comando Quando a função Cancelando o registro, esse nome deve ser excluído usando **xlfSetName** , de modo que o nome da função não está mais listado pelo Assistente de função. Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parâmetros

_pxRegisterId_ (**xltypeNum**)
  
A ID do registro da função a ser cancelado.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se tiver êxito, retornará **TRUE** (**xltypeBool**), caso contrário, ele retornará FALSE.
  
## <a name="remarks"></a>Comentários

O registro retornado por **xlfRegister** ID da função quando a função for primeira registrado. Ele também pode ser obtido chamando-se a [função xlfRegisterId](xlfregisterid.md) ou a [função xlfEvaluate](xlfevaluate.md). Observe que xlfRegisterId tenta registrar a função se ele já não foi registrado. Por esse motivo, se você estiver tentando apenas obter a identificação de modo que você pode cancelar o registro de função, é melhor obtê-lo, passando o nome registrado para **xlfEvaluate**. Se a função não foi registrada, **xlfEvaluate** falhar com um #NAME? erro. 
  
## <a name="example"></a>Exemplo

Ver o código para a função **fExit** em `\SAMPLES\GENERIC\GENERIC.C`.
  
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

- [xlfRegister (Form 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formulário 2)](xlfunregister-form-2.md)
- [Funções XLM essenciais e úteis para a API de C](essential-and-useful-c-api-xlm-functions.md)

