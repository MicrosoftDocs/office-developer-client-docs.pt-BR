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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317084"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="1189c-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1189c-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="1189c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1189c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1189c-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu com um objeto de administração de perfil.</span><span class="sxs-lookup"><span data-stu-id="1189c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="1189c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1189c-106">Parameters</span></span>

 <span data-ttu-id="1189c-107">_And_</span><span class="sxs-lookup"><span data-stu-id="1189c-107">_hResult_</span></span>
  
> <span data-ttu-id="1189c-108">no Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="1189c-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="1189c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1189c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1189c-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="1189c-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="1189c-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="1189c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1189c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1189c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1189c-113">As cadeias de caracteres na estrutura [MAPIERROR](mapierror.md) retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1189c-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="1189c-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1189c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="1189c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1189c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1189c-116">bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="1189c-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="1189c-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="1189c-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1189c-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1189c-118">Return value</span></span>

<span data-ttu-id="1189c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1189c-119">S_OK</span></span> 
  
> <span data-ttu-id="1189c-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1189c-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1189c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1189c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1189c-122">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="1189c-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1189c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1189c-123">Remarks</span></span>

<span data-ttu-id="1189c-124">O método **IProfAdmin:: GetLastError** recupera informações sobre o último erro retornado de uma chamada de método para o objeto de administração de perfil.</span><span class="sxs-lookup"><span data-stu-id="1189c-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1189c-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1189c-125">Notes to callers</span></span>

<span data-ttu-id="1189c-126">Você pode usar a estrutura **MAPIERROR** , se MAPI fornecer um, indicado pelo parâmetro _lppMAPIError_ somente se GetLastError \*\*\*\* retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="1189c-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="1189c-127">Às vezes, o MAPI não pode determinar o que foi o último erro ou não faz mais para relatar o erro.</span><span class="sxs-lookup"><span data-stu-id="1189c-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="1189c-128">Nessa situação, um ponteiro para nulo é retornado em _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="1189c-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="1189c-129">Para liberar toda a memória alocada por MAPI para a estrutura **MAPIERROR** , chame a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1189c-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="1189c-130">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [usando erros estendidos](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="1189c-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1189c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1189c-131">See also</span></span>



[<span data-ttu-id="1189c-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1189c-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1189c-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1189c-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1189c-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1189c-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

