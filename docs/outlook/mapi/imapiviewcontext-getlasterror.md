---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e373a4abd5e2435d08fc263316ff6ebf650410ef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568095"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="3012f-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3012f-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="3012f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3012f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3012f-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto view contexto.</span><span class="sxs-lookup"><span data-stu-id="3012f-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="3012f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3012f-106">Parameters</span></span>

 <span data-ttu-id="3012f-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="3012f-107">_hResult_</span></span>
  
> <span data-ttu-id="3012f-108">[in] Tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="3012f-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="3012f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3012f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3012f-110">[in] Bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="3012f-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="3012f-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="3012f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3012f-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3012f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3012f-113">As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3012f-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="3012f-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3012f-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="3012f-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="3012f-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="3012f-116">[out] Ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="3012f-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="3012f-117">Este parâmetro pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar.</span><span class="sxs-lookup"><span data-stu-id="3012f-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3012f-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3012f-118">Return value</span></span>

<span data-ttu-id="3012f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3012f-119">S_OK</span></span> 
  
> <span data-ttu-id="3012f-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="3012f-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3012f-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3012f-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3012f-122">Tanto o sinalizador MAPI_UNICODE foi definido e **GetLastError** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** só oferece suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="3012f-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3012f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3012f-123">Remarks</span></span>

<span data-ttu-id="3012f-124">O método **IMAPIViewContext::GetLastError** fornece informações sobre uma chamada de método anterior que falharam.</span><span class="sxs-lookup"><span data-stu-id="3012f-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="3012f-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro, incluindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3012f-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3012f-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="3012f-126">Notes to callers</span></span>

<span data-ttu-id="3012f-127">Você pode fazer uso do **MAPIERROR** estrutura apontado pelo parâmetro _lppMAPIError_ se MAPI fornece um somente se **GetLastError** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="3012f-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="3012f-128">Em alguns casos, MAPI não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="3012f-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="3012f-129">Nessa situação, um ponteiro como NULL é retornado em _lppMAPIError_ , em vez disso.</span><span class="sxs-lookup"><span data-stu-id="3012f-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="3012f-130">Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3012f-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3012f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3012f-131">See also</span></span>



[<span data-ttu-id="3012f-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3012f-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="3012f-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3012f-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3012f-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3012f-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

