---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439846"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="97f64-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="97f64-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="97f64-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97f64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97f64-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu com o objeto de administração de provedor.</span><span class="sxs-lookup"><span data-stu-id="97f64-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="97f64-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97f64-106">Parameters</span></span>

 <span data-ttu-id="97f64-107">_And_</span><span class="sxs-lookup"><span data-stu-id="97f64-107">_hResult_</span></span>
  
> <span data-ttu-id="97f64-108">no Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="97f64-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="97f64-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97f64-109">_ulFlags_</span></span>
  
> <span data-ttu-id="97f64-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="97f64-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="97f64-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="97f64-111">The following flag can be set:</span></span>
    
<span data-ttu-id="97f64-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97f64-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="97f64-113">As cadeias de caracteres no **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="97f64-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="97f64-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="97f64-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="97f64-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="97f64-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="97f64-116">bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="97f64-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="97f64-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhum **MAPIERROR** a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="97f64-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97f64-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="97f64-118">Return value</span></span>

<span data-ttu-id="97f64-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="97f64-119">S_OK</span></span> 
  
> <span data-ttu-id="97f64-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="97f64-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="97f64-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="97f64-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="97f64-122">O sinalizador MAPI_UNICODE foi definido e getLastError não tem suporte para Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** oferece suporte somente para Unicode. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="97f64-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="97f64-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="97f64-123">Remarks</span></span>

<span data-ttu-id="97f64-124">O método **IProviderAdmin:: GetLastError** fornece informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="97f64-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="97f64-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="97f64-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="97f64-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="97f64-126">Notes to callers</span></span>

<span data-ttu-id="97f64-127">Você pode usar a estrutura **MAPIERROR** , se MAPI fornecer um, que o parâmetro _lppMAPIError_ aponta apenas se GetLastError retornar S_OK. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="97f64-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="97f64-128">Às vezes, o MAPI não pode determinar o que foi o último erro ou não faz mais para relatar o erro.</span><span class="sxs-lookup"><span data-stu-id="97f64-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="97f64-129">Nessa situação, um ponteiro para nulo é retornado em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="97f64-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="97f64-130">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [usando erros estendidos](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="97f64-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97f64-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="97f64-131">See also</span></span>



[<span data-ttu-id="97f64-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="97f64-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="97f64-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="97f64-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="97f64-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97f64-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

