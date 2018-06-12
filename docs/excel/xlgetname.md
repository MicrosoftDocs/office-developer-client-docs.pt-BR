---
title: xlGetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetName
keywords:
- função xlgetname [excel 2007]
localization_priority: Normal
ms.assetid: 72dbebc0-7436-4771-8fbf-2b445341da65
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 069676957d280a0bf3b398bb23b27f0e654bc655
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765471"
---
# <a name="xlgetname"></a><span data-ttu-id="faedc-104">xlGetName</span><span class="sxs-lookup"><span data-stu-id="faedc-104">xlGetName</span></span>

<span data-ttu-id="faedc-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="faedc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="faedc-106">Retorna o nome completo do arquivo e o caminho da DLL na forma de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="faedc-106">Returns the full path and file name of the DLL in the form of a string.</span></span>
  
```cs
Excel12(xlGetName, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="faedc-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="faedc-107">Parameters</span></span>

<span data-ttu-id="faedc-108">Essa função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="faedc-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="faedc-109">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="faedc-109">Property value/Return value</span></span>

<span data-ttu-id="faedc-110">Retorna o nome de arquivo e caminho (**xltypeStr**).</span><span class="sxs-lookup"><span data-stu-id="faedc-110">Returns the path and file name (**xltypeStr**).</span></span> 
  
## <a name="example"></a><span data-ttu-id="faedc-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="faedc-111">Example</span></span>

`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetNameExample(void)
{
    XLOPER12 xRes;
    Excel12(xlGetName, (LPXLOPER12)&xRes, 0);
    Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="faedc-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="faedc-112">See also</span></span>

- [<span data-ttu-id="faedc-113">Funções da API C que podem ser chamadas apenas por um DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="faedc-113">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

