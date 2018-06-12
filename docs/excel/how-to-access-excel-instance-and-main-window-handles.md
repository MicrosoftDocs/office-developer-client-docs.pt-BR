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
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="0d332-104">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="0d332-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="0d332-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0d332-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0d332-106">Para programar no ambiente do Windows, em alguns casos, você deve saber o identificador da instância do Microsoft Excel ou a janela principal manipular.</span><span class="sxs-lookup"><span data-stu-id="0d332-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="0d332-107">Por exemplo, essas alças são úteis quando você estiver criando e exibindo caixas de diálogo personalizadas do Windows.</span><span class="sxs-lookup"><span data-stu-id="0d332-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="0d332-108">Há duas funções somente XLL C API que fornecem acesso a essas alças: a função de [xlGetInst](xlgetinst.md) e o [xlGetHwnd](xlgethwnd.md) funcionam respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0d332-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="0d332-109">No Win32, todas as manipulações são números inteiros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0d332-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="0d332-110">No entanto, quando **XLOPER** foi criado, o Windows era um sistema de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0d332-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="0d332-111">Portanto, a estrutura permitida apenas para as alças de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0d332-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="0d332-112">No Win32, quando chamado com **Excel4** ou **Excel4v**, a função **xlGetInst** e a função **xlGetHwnd** retornam apenas a parte inferior da alça de 32 bits completa.</span><span class="sxs-lookup"><span data-stu-id="0d332-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="0d332-113">No Excel 2007 e versões posteriores, quando essas funções são chamadas com [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), **XLOPER12** retornado contém um manipulador de 32 bits completa.</span><span class="sxs-lookup"><span data-stu-id="0d332-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="0d332-114">Obter o identificador de instância completa é simple em qualquer versão do Excel, conforme ele é passado para o retorno de chamada do Windows **DllMain**, que é chamado quando a DLL é carregada.</span><span class="sxs-lookup"><span data-stu-id="0d332-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="0d332-115">Se registrar este identificador da instância em uma variável global, você nunca precisará chamar a função **xlGetInst** .</span><span class="sxs-lookup"><span data-stu-id="0d332-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="0d332-116">Obtendo a alça de Excel principal no Excel 2003 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="0d332-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="0d332-117">Para obter a alça principal do Excel no Excel 2003 e versões anteriores de 32 bits, você deve primeiro chamar a função de **xlGetHwnd** para obter a palavra baixa da alça de real.</span><span class="sxs-lookup"><span data-stu-id="0d332-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="0d332-118">Em seguida, você deve iterar a lista de janelas de nível superior para pesquisar uma correspondência com a palavra baixa retornada.</span><span class="sxs-lookup"><span data-stu-id="0d332-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="0d332-119">O código a seguir ilustra a técnica.</span><span class="sxs-lookup"><span data-stu-id="0d332-119">The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="0d332-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d332-120">See also</span></span>



[<span data-ttu-id="0d332-121">Exibindo caixas de diálogo de dentro de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="0d332-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="0d332-122">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="0d332-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="0d332-123">Developing Excel XLLs</span><span class="sxs-lookup"><span data-stu-id="0d332-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

