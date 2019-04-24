---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328995"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="1d9f7-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1d9f7-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="1d9f7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d9f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d9f7-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior na tabela.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="1d9f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d9f7-106">Parameters</span></span>

 <span data-ttu-id="1d9f7-107">_And_</span><span class="sxs-lookup"><span data-stu-id="1d9f7-107">_hResult_</span></span>
  
> <span data-ttu-id="1d9f7-108">no HRESULT contendo o erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="1d9f7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d9f7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1d9f7-110">no Bitmask dos sinalizadores que controlam o tipo das cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="1d9f7-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="1d9f7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1d9f7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d9f7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1d9f7-113">As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="1d9f7-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="1d9f7-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1d9f7-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1d9f7-116">bota Ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada contendo a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="1d9f7-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não for possível fornecer uma estrutura **MAPIERROR** com as informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d9f7-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1d9f7-118">Return value</span></span>

<span data-ttu-id="1d9f7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d9f7-119">S_OK</span></span> 
  
> <span data-ttu-id="1d9f7-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1d9f7-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1d9f7-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1d9f7-122">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d9f7-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d9f7-123">Remarks</span></span>

<span data-ttu-id="1d9f7-124">O método imApitable **:: GetLastError** retorna informações detalhadas, se disponíveis, sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="1d9f7-125">Essas informações podem ser exibidas em uma mensagem ou em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1d9f7-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1d9f7-126">Notes to callers</span></span>

<span data-ttu-id="1d9f7-127">Chame **GetLastError** sempre que precisar exibir informações sobre um erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="1d9f7-128">Você pode usar a estrutura [MAPIERROR](mapierror.md) apontada pelo parâmetro _lppMAPIError_ se o objeto Table fornecer um somente se GetLastError retornar \*\*\*\* S_OK.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="1d9f7-129">Às vezes, a implementação de tabela não pode determinar qual é o último erro ou não é mais relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="1d9f7-130">Nessa situação, o ponteiro em _lppMAPIError_ é definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="1d9f7-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="1d9f7-131">Para liberar toda a memória alocada para a estrutura **MAPIERROR** , chame a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1d9f7-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="1d9f7-132">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="1d9f7-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d9f7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d9f7-133">See also</span></span>



[<span data-ttu-id="1d9f7-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1d9f7-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1d9f7-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1d9f7-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1d9f7-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d9f7-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

