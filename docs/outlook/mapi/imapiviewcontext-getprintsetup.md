---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425124"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="3b047-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="3b047-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="3b047-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b047-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b047-105">Recupera as informações de impressão atuais.</span><span class="sxs-lookup"><span data-stu-id="3b047-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="3b047-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b047-106">Parameters</span></span>

 <span data-ttu-id="3b047-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b047-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3b047-108">no Bitmask dos sinalizadores que controlam o tipo das cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="3b047-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="3b047-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="3b047-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3b047-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3b047-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3b047-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3b047-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="3b047-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3b047-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3b047-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="3b047-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="3b047-114">bota Ponteiro para um ponteiro para uma estrutura que contém as informações de impressão.</span><span class="sxs-lookup"><span data-stu-id="3b047-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b047-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3b047-115">Return value</span></span>

<span data-ttu-id="3b047-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b047-116">S_OK</span></span> 
  
> <span data-ttu-id="3b047-117">As informações de impressão foram recuperadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="3b047-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b047-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b047-118">Remarks</span></span>

<span data-ttu-id="3b047-119">Os objetos Form chamam o método **IMAPIViewContext:: GetPrintSetup** para recuperar informações sobre a configuração da impressora antes de tentar imprimir a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="3b047-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3b047-120">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="3b047-120">Notes to implementers</span></span>

<span data-ttu-id="3b047-121">Aloque os membros **hDevMode** e **HDevName** da estrutura [FORMPRINTSETUP](formprintsetup.md) usando a função **GlobalAlloc**do Win32.</span><span class="sxs-lookup"><span data-stu-id="3b047-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3b047-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="3b047-122">Notes to callers</span></span>

<span data-ttu-id="3b047-123">Se você espera que os membros **hDevMode** e **HDevName** da estrutura **FORMPRINTSETUP** apontados pelo parâmetro _lppFormPrintSetup_ como cadeias de caracteres Unicode, defina _parâmetroulflags_ como MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="3b047-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="3b047-124">Caso contrário, **GetPrintSetup** retornará essas cadeias de caracteres no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3b047-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="3b047-125">Libere os membros **hDevMode** e **HDevName** da estrutura **FORMPRINTSETUP** chamando a função Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="3b047-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="3b047-126">Libere toda a estrutura do **FORMPRINTSETUP** chamando [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3b047-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b047-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b047-127">See also</span></span>



[<span data-ttu-id="3b047-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="3b047-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="3b047-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b047-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

