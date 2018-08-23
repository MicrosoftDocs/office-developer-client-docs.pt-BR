---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 65bf7debcae1367ccad9e109242fd4a72839a94e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584923"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="1b9b1-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b9b1-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="1b9b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b9b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b9b1-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreram com um objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="1b9b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b9b1-106">Parameters</span></span>

 <span data-ttu-id="1b9b1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="1b9b1-107">_hResult_</span></span>
  
> <span data-ttu-id="1b9b1-108">[in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="1b9b1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b9b1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1b9b1-110">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="1b9b1-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="1b9b1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1b9b1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b9b1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1b9b1-113">As cadeias de caracteres na estrutura [MAPIERROR](mapierror.md) retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="1b9b1-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="1b9b1-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1b9b1-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1b9b1-116">[out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="1b9b1-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b9b1-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1b9b1-118">Return value</span></span>

<span data-ttu-id="1b9b1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b9b1-119">S_OK</span></span> 
  
> <span data-ttu-id="1b9b1-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1b9b1-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1b9b1-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1b9b1-122">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b9b1-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b9b1-123">Remarks</span></span>

<span data-ttu-id="1b9b1-124">O método **IProfAdmin::GetLastError** recupera informações sobre o último erro retornado de uma chamada de método do objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b9b1-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1b9b1-125">Notes to callers</span></span>

<span data-ttu-id="1b9b1-126">Você pode usar a estrutura **MAPIERROR** , se o MAPI fornece um, apontado pela _lppMAPIError_ parâmetro se **GetLastError** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="1b9b1-127">Em alguns casos, MAPI não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="1b9b1-128">Nessa situação, é retornado um ponteiro como NULL no _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="1b9b1-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="1b9b1-129">Para liberar toda a memória alocada pelo MAPI para a estrutura **MAPIERROR** , chame a função de [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1b9b1-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="1b9b1-130">Para obter mais informações sobre o método **GetLastError** , consulte [Usando erros estendido](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="1b9b1-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b9b1-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b9b1-131">See also</span></span>



[<span data-ttu-id="1b9b1-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1b9b1-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1b9b1-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1b9b1-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1b9b1-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b9b1-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

