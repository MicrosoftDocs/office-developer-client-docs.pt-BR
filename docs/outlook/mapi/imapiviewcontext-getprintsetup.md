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
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="8e35b-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="8e35b-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="8e35b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e35b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e35b-105">Recupera informações de impressão atuais.</span><span class="sxs-lookup"><span data-stu-id="8e35b-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="8e35b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e35b-106">Parameters</span></span>

 <span data-ttu-id="8e35b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e35b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8e35b-108">[in] Máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="8e35b-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="8e35b-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="8e35b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8e35b-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e35b-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8e35b-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e35b-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="8e35b-112">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8e35b-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8e35b-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="8e35b-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="8e35b-114">[out] Ponteiro para um ponteiro para uma estrutura que contém as informações de impressão.</span><span class="sxs-lookup"><span data-stu-id="8e35b-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e35b-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8e35b-115">Return value</span></span>

<span data-ttu-id="8e35b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e35b-116">S_OK</span></span> 
  
> <span data-ttu-id="8e35b-117">As informações de impressão foram recuperadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="8e35b-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e35b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e35b-118">Remarks</span></span>

<span data-ttu-id="8e35b-119">Objetos de formulário chamam o método **IMAPIViewContext::GetPrintSetup** para recuperar informações sobre a instalação da impressora antes de tentar imprimir a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="8e35b-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8e35b-120">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="8e35b-120">Notes to implementers</span></span>

<span data-ttu-id="8e35b-121">Aloque **os membros hDevMode** e **hDevName** da estrutura [FORMPRINTSETUP](formprintsetup.md) usando a função **Win32 GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="8e35b-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e35b-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8e35b-122">Notes to callers</span></span>

<span data-ttu-id="8e35b-123">Se você espera que os membros **hDevMode** e **hDevName** da estrutura **FORMPRINTSETUP** apontados pelo parâmetro  _lppFormPrintSetup_ sejam cadeias de caracteres Unicode, defina  _ulFlags_ como MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="8e35b-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="8e35b-124">Caso contrário, **GetPrintSetup** retornará essas cadeias de caracteres no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8e35b-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="8e35b-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="8e35b-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="8e35b-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="8e35b-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e35b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e35b-127">See also</span></span>



[<span data-ttu-id="8e35b-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="8e35b-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="8e35b-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e35b-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

