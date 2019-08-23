---
title: Acessar a instância do Excel e as alças da janela principal
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acessar as alças do Excel, alças [Excel 2007], acessar, instâncias do Excel, acessar, alças da janela [Excel 2007], acessar
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310756"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Acessar a instância do Excel e as alças da janela principal

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para o programa no ambiente do Windows, às vezes é preciso conhecer a alça da instância do Microsoft Excel ou a alça da janela principal.  Por exemplo, essas alças são úteis quando você está criando e exibindo as caixas de diálogo personalizadas do Windows.
  
Há duas funções de API de C somente XLL que fornecem acesso a essas alças; a função [xlGetInst](xlgetinst.md) e a função [xlGetHwnd](xlgethwnd.md), respectivamente. No Win32, todas as alças são números inteiros de 32 bits. No entanto, quando o **XLOPER** foi criado, o Windows era um sistema de 16 bits. Portanto, a estrutura só permitia alças de 16 bits. No Win32, quando chamada com o **Excel4** ou o **Excel4v**, a função **xlGetInst** e a função **xlGetHwnd** retornavam apenas a parte inferior da alça completa de 32 bits. 
  
No Excel 2007 e nas versões posteriores, quando essas funções são chamadas com [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), o **XLOPER12** retornado contém alça completa de 32 bits. 
  
Obter a alça de instância completa é um processo simples em qualquer versão do Excel, e ela é passada para o retorno do Windows **DllMain**, que é chamado quando a DLL é carregada. Se você gravar esta alça de instância em uma variável global, nunca vai precisar chamar a função **xlGetInst**. 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Obtenção da Alça Principal do Excel no Excel 2003 e versões anteriores

Para obter a alça principal do Excel no Excel 2003 e nas versões anteriores de 32 bits, você precisa primeiro chamar a função **xlGetHwnd** para obter a palavra inferior da alça real. Em seguida, você deve iterar lista de janelas de nível superior para procurar uma correspondência com a palavra inferior retornada. O código a seguir ilustra a técnica. 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord returned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a>Confira também



[Exibir caixas de diálogo de dentro de uma DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

