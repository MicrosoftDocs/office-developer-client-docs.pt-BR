---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- função xlAutoClose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765469"
---
# <a name="xlautoclose"></a>xlAutoClose

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamado pelo Microsoft Excel sempre que o XLL é desativado. O suplemento é desativado quando uma sessão do Excel é encerrada normalmente. O suplemento pode ser desativado pelo usuário durante uma sessão do Excel e essa função será chamada nesse caso.
  
Excel não exige um XLL implementar e exportar essa função, apesar de ser recomendável para que seu XLL pode cancelar o registro de funções e comandos, liberar recursos, desfazer personalizações e assim por diante. Se as funções e comandos não são explicitamente não registrados pelo XLL, o Excel faz isso depois de chamar a função **xlAutoClose** . 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Par�metros

Essa função não assume nenhum argumento.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A implementação dessa função deve retornar 1 (**int**).
  
## <a name="remarks"></a>Coment�rios

Excel chama a função **xlAutoClose** sempre que o XLL estiver desativado, ou seja, descarregado da memória. XLL é desativado nas seguintes situações: 
  
- No final de uma sessão do Excel se ativo durante a sessão normal.
    
- Se explicitamente descarregado durante uma sessão do Excel.
    
- Um XLL pode ser descarregado de várias maneiras:
    
- Usando o Gerenciador de suplemento.
    
- A partir de outra XLL que chama [xlfUnregister](xlfunregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- De uma folha de macro XLM que chama [cancela o registro](xlfunregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
Essa função deve fazer o seguinte:
  
- Remova os menus ou itens de menu que foram adicionados pelo XLL.
    
- Execute qualquer limpeza global necessária.
    
- Exclua todos os nomes que foram criados, especialmente os nomes das funções exportadas. Lembre-se de que registrar funções pode causar alguns nomes a serem criados, se o quarto argumento para **registrar** estiver presente. 
    
## <a name="example"></a>Example

Consulte os arquivos `SAMPLES\EXAMPLE\EXAMPLE.C` e `SAMPLES\GENERIC\GENERIC.C` por exemplo implementações dessa função. O código a seguir é de `SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a>Confira também



[xlAutoOpen](xlautoopen.md)


[Gerenciador de suplemento e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

