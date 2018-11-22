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
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643175"
---
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="8b185-104">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="8b185-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="8b185-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8b185-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8b185-106">Para o programa no ambiente do Windows, às vezes é preciso conhecer a alça da instância do Microsoft Excel ou a alça da janela principal. </span><span class="sxs-lookup"><span data-stu-id="8b185-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="8b185-107">Por exemplo, essas alças são úteis quando você está criando e exibindo as caixas de diálogo personalizadas do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b185-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="8b185-108">Há duas funções de API de C somente XLL que fornecem acesso a essas alças; a função [xlGetInst](xlgetinst.md) e a função [xlGetHwnd](xlgethwnd.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8b185-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="8b185-109">No Win32, todas as alças são números inteiros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8b185-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="8b185-110">No entanto, quando o **XLOPER** foi criado, o Windows era um sistema de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8b185-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="8b185-111">Portanto, a estrutura só permitia alças de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8b185-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="8b185-112">No Win32, quando chamada com o **Excel4** ou o **Excel4v**, a função **xlGetInst** e a função **xlGetHwnd** retornavam apenas a parte inferior da alça completa de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8b185-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="8b185-113">No Excel 2007 e nas versões posteriores, quando essas funções são chamadas com [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), o **XLOPER12** retornado contém alça completa de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8b185-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="8b185-114">Obter a alça de instância completa é um processo simples em qualquer versão do Excel, e ela é passada para o retorno do Windows **DllMain**, que é chamado quando a DLL é carregada.</span><span class="sxs-lookup"><span data-stu-id="8b185-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="8b185-115">Se você gravar esta alça de instância em uma variável global, nunca vai precisar chamar a função **xlGetInst**.</span><span class="sxs-lookup"><span data-stu-id="8b185-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="8b185-116">Obtenção da Alça Principal do Excel no Excel 2003 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="8b185-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="8b185-117">Para obter a alça principal do Excel no Excel 2003 e nas versões anteriores de 32 bits, você precisa primeiro chamar a função **xlGetHwnd** para obter a palavra inferior da alça real.</span><span class="sxs-lookup"><span data-stu-id="8b185-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="8b185-118">Em seguida, você deve iterar lista de janelas de nível superior para procurar uma correspondência com a palavra inferior retornada.</span><span class="sxs-lookup"><span data-stu-id="8b185-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="8b185-119">O código a seguir ilustra a técnica.</span><span class="sxs-lookup"><span data-stu-id="8b185-119">The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="8b185-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b185-120">See also</span></span>



[<span data-ttu-id="8b185-121">Exibir caixas de diálogo de dentro de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="8b185-121">Displaying dialog boxes from within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="8b185-122">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="8b185-122">C API functions that can be called only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="8b185-123">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="8b185-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

