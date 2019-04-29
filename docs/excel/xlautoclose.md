---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- função xlautoclose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e27ac922c4ba53a30e8e485d3210acc62b7d4bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415856"
---
# <a name="xlautoclose"></a>xlAutoClose

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamada pelo Microsoft Excel sempre que o XLL está desativado. O suplemento é desativado quando a sessão do Excel termina normalmente. O suplemento pode ser desativado pelo usuário durante uma sessão do Excel e, nesse caso, essa função será chamada.
  
O Excel não requer um XLL para implementar e exportar essa função, embora seja recomendável para que o XLL possa cancelar o registro de comandos e funções, liberar recursos, desfazer personalizações e assim por diante. Se as funções e comandos não forem explicitamente registrados pelo XLL, o Excel executa isso depois de chamar a função **xlAutoClose**. 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A implementação dessa função deve retornar 1 (**int**).
  
## <a name="remarks"></a>Comentários

O Excel chama a função **xlAutoClose** sempre que o XLL está desativado, ou seja, não está carregado na memória. O XLL é desativado nas seguintes situações: 
  
- No final normal de uma sessão do Excel, se for ativado durante a sessão.
    
- Se for explicitamente descarregado durante uma sessão do Excel.
    
- Um XLL pode ser descarregado de várias maneiras:
    
- Usando o Gerenciador de Suplemento.
    
- A partir de outro XLL que chama [xlfUnregister](xlfunregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- A partir de uma planilha de macro XLL que chama [xlfUnregister](xlfunregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
Esta função deve fazer o seguinte:
  
- Remova os menus ou itens de menu adicionados pelo XLL.
    
- Execute qualquer limpeza global necessária.
    
- Exclua os nomes foram criados, especialmente nomes de funções exportadas. Lembre-se de que registrar funções pode causar a criação de alguns nomes, se o quarto argumento **REGISTER** estiver presente. 
    
## <a name="example"></a>Exemplo

Veja os arquivos `SAMPLES\EXAMPLE\EXAMPLE.C` e `SAMPLES\GENERIC\GENERIC.C` como exemplos de implementações dessa função. O código a seguir é de `SAMPLES\GENERIC\GENERIC.C`.
  
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


[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

