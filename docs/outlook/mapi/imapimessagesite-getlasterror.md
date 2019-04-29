---
title: IMAPIMessageSiteGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetLastError
api_type:
- COM
ms.assetid: 7ea282d7-388a-4f05-9780-f8dbc5c5d395
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cc4de8aa21d4b3b27bf757389b663ebeff69a9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420735"
---
# <a name="imapimessagesitegetlasterror"></a><span data-ttu-id="ee66c-103">IMAPIMessageSite::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ee66c-103">IMAPIMessageSite::GetLastError</span></span>

  
  
<span data-ttu-id="ee66c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee66c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee66c-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto site da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ee66c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ee66c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee66c-106">Parameters</span></span>

 <span data-ttu-id="ee66c-107">_And_</span><span class="sxs-lookup"><span data-stu-id="ee66c-107">_hResult_</span></span>
  
> <span data-ttu-id="ee66c-108">no Um HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="ee66c-108">[in] An HRESULT that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="ee66c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee66c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ee66c-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="ee66c-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ee66c-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="ee66c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ee66c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee66c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ee66c-113">As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ee66c-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ee66c-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ee66c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ee66c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ee66c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ee66c-116">bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="ee66c-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ee66c-117">Esse parâmetro pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="ee66c-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee66c-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ee66c-118">Return value</span></span>

<span data-ttu-id="ee66c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee66c-119">S_OK</span></span>
  
> <span data-ttu-id="ee66c-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="ee66c-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ee66c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ee66c-121">MAPI_E_BAD_CHARWIDTH</span></span>
  
> <span data-ttu-id="ee66c-122">O sinalizador MAPI_UNICODE foi definido e getLastError não tem suporte para Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** oferece suporte somente para Unicode. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ee66c-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ee66c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee66c-123">Remarks</span></span>

<span data-ttu-id="ee66c-124">O método **IMAPIMessageSite:: GetLastError** fornece informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="ee66c-124">The **IMAPIMessageSite::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="ee66c-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee66c-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee66c-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ee66c-126">Notes to callers</span></span>

<span data-ttu-id="ee66c-127">Você pode usar a estrutura **MAPIERROR** indicada pelo parâmetro _LPPMAPIERROR_ se a MAPI fornecer somente um se GetLastError retornar \*\*\*\* S_OK.</span><span class="sxs-lookup"><span data-stu-id="ee66c-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="ee66c-128">Às vezes, o MAPI não pode determinar qual é o último erro ou não tem mais a relatar sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="ee66c-128">Sometimes MAPI cannot determine what the last error was, or has nothing more to report about the error.</span></span> <span data-ttu-id="ee66c-129">Nessa situação, um ponteiro para nulo é retornado em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ee66c-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="ee66c-130">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [usando erros estendidos](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="ee66c-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee66c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee66c-131">See also</span></span>



[<span data-ttu-id="ee66c-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ee66c-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ee66c-133">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee66c-133">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)

