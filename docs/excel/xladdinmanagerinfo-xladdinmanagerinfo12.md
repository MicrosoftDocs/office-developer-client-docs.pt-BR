---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- Função xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407792"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="4489f-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="4489f-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="4489f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4489f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4489f-106">Chamado pelo Microsoft Excel quando o Gerenciador de Complementos é invocado pela primeira vez em uma sessão do Excel.</span><span class="sxs-lookup"><span data-stu-id="4489f-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="4489f-107">Essa função é usada para fornecer ao Add-In Do usuário informações sobre o seu complemento.</span><span class="sxs-lookup"><span data-stu-id="4489f-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="4489f-108">O Excel 2007 e versões posteriores chamam **xlAddInManagerInfo12** de preferência para **xlAddInManagerInfo** se exportado pelo XLL.</span><span class="sxs-lookup"><span data-stu-id="4489f-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="4489f-109">A **função xlAddInManagerInfo12** deve funcionar da mesma maneira que **xlAddInManagerInfo** para evitar diferenças específicas de versão no comportamento do XLL.</span><span class="sxs-lookup"><span data-stu-id="4489f-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="4489f-110">O Excel espera **que xlAddInManagerInfo12** retorne um tipo de dados **XLOPER12,** enquanto **xlAddInManagerInfo** deve retornar um **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="4489f-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="4489f-111">A **função xlAddInManagerInfo12** não é chamada por versões do Excel anteriores ao Excel 2007, pois elas não têm suporte para **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="4489f-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="4489f-112">O Excel não exige um XLL para implementar e exportar qualquer uma dessas funções.</span><span class="sxs-lookup"><span data-stu-id="4489f-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="4489f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4489f-113">Parameters</span></span>

 <span data-ttu-id="4489f-114">_pxAction:_ Um ponteiro para um **XLOPER/XLOPER12** numérico (**xltypeInt** ou **xltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="4489f-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="4489f-115">As informações que o Excel está solicitando.</span><span class="sxs-lookup"><span data-stu-id="4489f-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4489f-116">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4489f-116">Property value/Return value</span></span>

<span data-ttu-id="4489f-117">Se  _pxAction_ for ou puder ser coerced para o número 1, sua implementação dessa função deverá retornar uma cadeia de caracteres contendo algumas informações sobre o complemento, normalmente seu nome e talvez um número de versão.</span><span class="sxs-lookup"><span data-stu-id="4489f-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="4489f-118">Caso contrário, ele deve retornar #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="4489f-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="4489f-119">Se você não retornar uma cadeia de caracteres, o Excel tentará converter o valor retornado em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4489f-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4489f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4489f-120">Remarks</span></span>

<span data-ttu-id="4489f-121">Se a cadeia de caracteres retornada aponta para buffer alocado dinamicamente, você deve garantir que esse buffer seja liberado eventualmente.</span><span class="sxs-lookup"><span data-stu-id="4489f-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="4489f-122">Se a cadeia de caracteres foi alocada pelo Excel, faça isso definindo **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="4489f-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="4489f-123">Se a cadeia de caracteres foi alocada pela DLL, você faz isso definindo **xlbitDLLFree** e também deve implementar em [xlAutoFree](xlautofree-xlautofree12.md) (se você estiver retornando um **XLOPER**) ou **xlAutoFree12** (se estiver retornando um **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="4489f-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="4489f-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4489f-124">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="4489f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4489f-125">See also</span></span>



[<span data-ttu-id="4489f-126">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="4489f-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

