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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f00418efa068ea81fab94605cbdfd139e24bb4a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767641"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="15054-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="15054-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="15054-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15054-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15054-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreram com o objeto de administração do provedor.</span><span class="sxs-lookup"><span data-stu-id="15054-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="15054-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15054-106">Parameters</span></span>

 <span data-ttu-id="15054-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="15054-107">_hResult_</span></span>
  
> <span data-ttu-id="15054-108">[in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="15054-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="15054-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15054-109">_ulFlags_</span></span>
  
> <span data-ttu-id="15054-110">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="15054-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="15054-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="15054-111">The following flag can be set:</span></span>
    
<span data-ttu-id="15054-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15054-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="15054-113">As cadeias de caracteres em **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="15054-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="15054-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="15054-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="15054-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="15054-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="15054-116">[out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="15054-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="15054-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhum **MAPIERROR** para retornar.</span><span class="sxs-lookup"><span data-stu-id="15054-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15054-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="15054-118">Return value</span></span>

<span data-ttu-id="15054-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="15054-119">S_OK</span></span> 
  
> <span data-ttu-id="15054-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="15054-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="15054-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="15054-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="15054-122">Tanto o sinalizador MAPI_UNICODE foi definido e **GetLastError** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="15054-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="15054-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="15054-123">Remarks</span></span>

<span data-ttu-id="15054-124">O método **IProviderAdmin::GetLastError** fornece informações sobre uma chamada de método anterior que falharam.</span><span class="sxs-lookup"><span data-stu-id="15054-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="15054-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro, incluindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15054-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="15054-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="15054-126">Notes to callers</span></span>

<span data-ttu-id="15054-127">Você pode usar a estrutura **MAPIERROR** , se o MAPI fornece um, se o parâmetro _lppMAPIError_ aponta para apenas se **GetLastError** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="15054-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="15054-128">Em alguns casos, MAPI não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="15054-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="15054-129">Nessa situação, um ponteiro como NULL é retornado em _lppMAPIError_ , em vez disso.</span><span class="sxs-lookup"><span data-stu-id="15054-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="15054-130">Para obter mais informações sobre o método **GetLastError** , consulte [Usando erros estendido](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="15054-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15054-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="15054-131">See also</span></span>



[<span data-ttu-id="15054-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="15054-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="15054-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="15054-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="15054-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15054-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

