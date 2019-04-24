---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316581"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="f897c-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f897c-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="f897c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f897c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f897c-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro do objeto de suporte anterior.</span><span class="sxs-lookup"><span data-stu-id="f897c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="f897c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f897c-106">Parameters</span></span>

 <span data-ttu-id="f897c-107">_And_</span><span class="sxs-lookup"><span data-stu-id="f897c-107">_hResult_</span></span>
  
> <span data-ttu-id="f897c-108">no Um identificador para o valor de erro gerado na chamada de método anterior para o objeto support.</span><span class="sxs-lookup"><span data-stu-id="f897c-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="f897c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f897c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f897c-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="f897c-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="f897c-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f897c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f897c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f897c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f897c-113">As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f897c-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="f897c-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f897c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f897c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f897c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="f897c-116">bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="f897c-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="f897c-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não for possível fornecer uma estrutura **MAPIERROR** com informações de erro apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f897c-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f897c-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f897c-118">Return value</span></span>

<span data-ttu-id="f897c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f897c-119">S_OK</span></span> 
  
> <span data-ttu-id="f897c-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="f897c-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="f897c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f897c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f897c-122">O sinalizador MAPI_UNICODE foi definido e o MAPI não dá suporte a Unicode, ou o MAPI_UNICODE não foi definido e o MAPI suporta apenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="f897c-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f897c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f897c-123">Remarks</span></span>

<span data-ttu-id="f897c-124">O método **IMAPISupport:: GetLastError** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="f897c-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="f897c-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f897c-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f897c-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f897c-126">Notes to callers</span></span>

<span data-ttu-id="f897c-127">Você pode usar o ponteiro para a estrutura **MAPIERROR** , se o MAPI fornecer um, no parâmetro _lppMAPIError_ somente se **GetLastError** retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="f897c-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="f897c-128">Às vezes, o MAPI não pode determinar qual é o último erro ou não tem mais a relatar sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="f897c-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="f897c-129">Nessa situação, _lppMAPIError_ retorna um ponteiro para NULL em vez disso.</span><span class="sxs-lookup"><span data-stu-id="f897c-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="f897c-130">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f897c-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="f897c-131">Para liberar toda a memória alocada por MAPI, chame a função [MAPIFreeBuffer](mapifreebuffer.md) da estrutura **MAPIERROR** retornada.</span><span class="sxs-lookup"><span data-stu-id="f897c-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f897c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f897c-132">See also</span></span>



[<span data-ttu-id="f897c-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f897c-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f897c-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f897c-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f897c-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f897c-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="f897c-136">Erros estendidos de MAPI</span><span class="sxs-lookup"><span data-stu-id="f897c-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

