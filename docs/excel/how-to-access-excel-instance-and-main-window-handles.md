---
title: Acessar a instância do Excel e as alças da janela principal
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acessando alças, alças [Excel 2007], acessando, instâncias de Excel, acessando, identificadores de janela [Excel 2007], acesso do excel
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765389"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Acessar a instância do Excel e as alças da janela principal

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para programar no ambiente do Windows, em alguns casos, você deve saber o identificador da instância do Microsoft Excel ou a janela principal manipular. Por exemplo, essas alças são úteis quando você estiver criando e exibindo caixas de diálogo personalizadas do Windows.
  
Há duas funções somente XLL C API que fornecem acesso a essas alças: a função de [xlGetInst](xlgetinst.md) e o [xlGetHwnd](xlgethwnd.md) funcionam respectivamente. No Win32, todas as manipulações são números inteiros de 32 bits. No entanto, quando **XLOPER** foi criado, o Windows era um sistema de 16 bits. Portanto, a estrutura permitida apenas para as alças de 16 bits. No Win32, quando chamado com **Excel4** ou **Excel4v**, a função **xlGetInst** e a função **xlGetHwnd** retornam apenas a parte inferior da alça de 32 bits completa. 
  
No Excel 2007 e versões posteriores, quando essas funções são chamadas com [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), **XLOPER12** retornado contém um manipulador de 32 bits completa. 
  
Obter o identificador de instância completa é simple em qualquer versão do Excel, conforme ele é passado para o retorno de chamada do Windows **DllMain**, que é chamado quando a DLL é carregada. Se registrar este identificador da instância em uma variável global, você nunca precisará chamar a função **xlGetInst** . 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Obtendo a alça de Excel principal no Excel 2003 e versões anteriores

Para obter a alça principal do Excel no Excel 2003 e versões anteriores de 32 bits, você deve primeiro chamar a função de **xlGetHwnd** para obter a palavra baixa da alça de real. Em seguida, você deve iterar a lista de janelas de nível superior para pesquisar uma correspondência com a palavra baixa retornada. O código a seguir ilustra a técnica. 
  
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
  // which match the LoWord retuned by xlGetHwnd.
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



[Exibindo caixas de diálogo de dentro de uma DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Developing Excel XLLs](developing-excel-xlls.md)

