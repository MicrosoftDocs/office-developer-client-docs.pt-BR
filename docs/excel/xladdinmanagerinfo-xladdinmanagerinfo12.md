---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- função xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765442"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="4c481-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="4c481-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="4c481-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4c481-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4c481-106">Chamado pelo Microsoft Excel quando o Gerenciador de suplementos é invocado pela primeira vez em uma sessão do Excel.</span><span class="sxs-lookup"><span data-stu-id="4c481-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="4c481-107">Essa função é usada para fornecer o Gerenciador de suplementos com informações sobre o add-in.</span><span class="sxs-lookup"><span data-stu-id="4c481-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="4c481-108">Excel 2007 e versões posteriores chamar **xlAddInManagerInfo12** em preferência **xlAddInManagerInfo** se exportá-los por XLL.</span><span class="sxs-lookup"><span data-stu-id="4c481-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="4c481-109">A função **xlAddInManagerInfo12** deve funcionar da mesma maneira como **xlAddInManagerInfo** para evitar específicos da versão diferenças no comportamento da XLL.</span><span class="sxs-lookup"><span data-stu-id="4c481-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="4c481-110">Excel espera **xlAddInManagerInfo12** para retornar um tipo de dados **XLOPER12** , enquanto **xlAddInManagerInfo** deve retornar **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="4c481-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="4c481-111">A função **xlAddInManagerInfo12** não é chamada por versões anteriores ao Excel 2007, do Excel, conforme eles não suportam o **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="4c481-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="4c481-112">Excel não exige um XLL implementar e exportar qualquer uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="4c481-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="4c481-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c481-113">Parameters</span></span>

 <span data-ttu-id="4c481-114">_pxAction:_ Um ponteiro para um de numéricos **XLOPER/XLOPER12** (**xltypeInt** ou **xltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="4c481-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="4c481-115">As informações que solicita Excel.</span><span class="sxs-lookup"><span data-stu-id="4c481-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4c481-116">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4c481-116">Property value/Return value</span></span>

<span data-ttu-id="4c481-117">Se _pxAction_ for, ou pode ser forçados para, o número 1, a implementação dessa função deve retornar uma cadeia de caracteres que contém algumas informações sobre o suplemento, geralmente seu nome e talvez um número de versão.</span><span class="sxs-lookup"><span data-stu-id="4c481-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="4c481-118">Caso contrário, ele deverá retornar #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="4c481-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="4c481-119">Se você não retornar uma cadeia de caracteres, o Excel tenta converter o valor retornado para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4c481-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c481-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c481-120">Remarks</span></span>

<span data-ttu-id="4c481-121">Se a cadeia de caracteres retornada aponta para o buffer alocado dinamicamente, você deve garantir que esse buffer eventualmente é liberado.</span><span class="sxs-lookup"><span data-stu-id="4c481-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="4c481-122">Se a cadeia de caracteres foi alocada pelo Excel, você pode fazer isso, definindo **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="4c481-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="4c481-123">Se a cadeia de caracteres foi alocada pela DLL, para fazer isso, a configuração **xlbitDLLFree**e você também deve implementar no [xlAutoFree](xlautofree-xlautofree12.md) (se você estiver retornando um **XLOPER**) ou **xlAutoFree12** (se você estiver retornando **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="4c481-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="4c481-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4c481-124">Example</span></span>

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a><span data-ttu-id="4c481-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c481-125">See also</span></span>



[<span data-ttu-id="4c481-126">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="4c481-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

