---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a39deb57a24b3a89ee10020a6442bcb1bca612a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575305"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="87f07-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="87f07-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="87f07-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87f07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87f07-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto form.</span><span class="sxs-lookup"><span data-stu-id="87f07-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="87f07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87f07-106">Parameters</span></span>

 <span data-ttu-id="87f07-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="87f07-107">_hResult_</span></span>
  
> <span data-ttu-id="87f07-108">[in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="87f07-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="87f07-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87f07-109">_ulFlags_</span></span>
  
> <span data-ttu-id="87f07-110">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="87f07-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="87f07-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="87f07-111">The following flag can be set:</span></span>
    
<span data-ttu-id="87f07-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87f07-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="87f07-113">As cadeias de caracteres na estrutura [MAPIERROR](mapierror.md) retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="87f07-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="87f07-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="87f07-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="87f07-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="87f07-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="87f07-116">[out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="87f07-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="87f07-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se o formulário será possível fornecer informações apropriadas para uma estrutura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="87f07-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="87f07-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="87f07-118">Return value</span></span>

<span data-ttu-id="87f07-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="87f07-119">S_OK</span></span> 
  
> <span data-ttu-id="87f07-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="87f07-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="87f07-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="87f07-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="87f07-122">Tanto o sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e o provedor de catálogo de endereços suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="87f07-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87f07-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="87f07-123">Remarks</span></span>

<span data-ttu-id="87f07-124">Objetos de formulário implementar o método **IPersistMessage::GetLastError** para fornecer informações sobre uma chamada de método anterior que falharam.</span><span class="sxs-lookup"><span data-stu-id="87f07-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="87f07-125">Visualizadores de formulário podem fornecer seus usuários com informações detalhadas sobre o erro, incluindo os dados da estrutura de [MAPIERROR](mapierror.md) em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="87f07-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="87f07-126">Uma chamada para **GetLastError** não afeta o estado do formulário.</span><span class="sxs-lookup"><span data-stu-id="87f07-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="87f07-127">Quando **GetLastError** retorna, o formulário permanece no estado em que estava antes que a chamada foi feita.</span><span class="sxs-lookup"><span data-stu-id="87f07-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="87f07-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="87f07-128">Notes to callers</span></span>

<span data-ttu-id="87f07-129">Você pode usar a estrutura **MAPIERROR** , se o formulário fornece um, que é apontado pelo parâmetro _lppMAPIError_ somente se **GetLastError** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="87f07-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="87f07-130">Em alguns casos, o formulário não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="87f07-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="87f07-131">Nessa situação, o formulário retorna um ponteiro como NULL em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="87f07-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="87f07-132">Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="87f07-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87f07-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="87f07-133">See also</span></span>



[<span data-ttu-id="87f07-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="87f07-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="87f07-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="87f07-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="87f07-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87f07-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

