---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 34de52693d8484abb28d2ee2f7b86f15e8bd037b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574095"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="93960-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="93960-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="93960-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93960-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93960-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de sessão anterior.</span><span class="sxs-lookup"><span data-stu-id="93960-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="93960-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93960-106">Parameters</span></span>

 <span data-ttu-id="93960-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="93960-107">_hResult_</span></span>
  
> <span data-ttu-id="93960-108">[in] Um identificador para o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="93960-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="93960-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="93960-109">_ulFlags_</span></span>
  
> <span data-ttu-id="93960-110">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="93960-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="93960-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="93960-111">The following flag can be set:</span></span>
    
<span data-ttu-id="93960-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93960-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="93960-113">As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="93960-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="93960-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="93960-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="93960-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="93960-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="93960-116">[out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="93960-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="93960-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se o MAPI, será possível fornecer informações apropriadas para uma estrutura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="93960-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93960-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="93960-118">Return value</span></span>

<span data-ttu-id="93960-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="93960-119">S_OK</span></span> 
  
> <span data-ttu-id="93960-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="93960-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="93960-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="93960-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="93960-122">O sinalizador MAPI_UNICODE foi definido e a sessão não dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="93960-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93960-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="93960-123">Remarks</span></span>

<span data-ttu-id="93960-124">O método **IMAPISession::GetLastError** recupera informações sobre o último erro que foi retornado por uma chamada de método **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="93960-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="93960-125">Clientes podem fornecer aos usuários informações detalhadas sobre o erro, incluindo essas informações em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="93960-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="93960-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="93960-126">Notes to callers</span></span>

<span data-ttu-id="93960-127">Você pode usar a estrutura **MAPIERROR** , se o MAPI fornece um, apontado pela _lppMAPIError_ parâmetro se **GetLastError** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="93960-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="93960-128">Em alguns casos, MAPI não pode determinar qual foi o último erro ou não tem nada mais a ser relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="93960-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="93960-129">Nessa situação, **GetLastError** retorna um ponteiro como NULL em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="93960-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="93960-130">Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="93960-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93960-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="93960-131">See also</span></span>



[<span data-ttu-id="93960-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="93960-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="93960-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="93960-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="93960-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="93960-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="93960-135">MAPI estendido erros</span><span class="sxs-lookup"><span data-stu-id="93960-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

