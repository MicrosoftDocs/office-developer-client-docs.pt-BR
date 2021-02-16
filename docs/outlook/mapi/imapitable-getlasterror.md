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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418999"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="64cf1-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="64cf1-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="64cf1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64cf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64cf1-105">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior na tabela.</span><span class="sxs-lookup"><span data-stu-id="64cf1-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="64cf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64cf1-106">Parameters</span></span>

 <span data-ttu-id="64cf1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="64cf1-107">_hResult_</span></span>
  
> <span data-ttu-id="64cf1-108">[in] HRESULT que contém o erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="64cf1-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="64cf1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="64cf1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="64cf1-110">[in] Máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="64cf1-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="64cf1-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="64cf1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="64cf1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64cf1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="64cf1-113">As cadeias de caracteres na **estrutura MAPIERROR** retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="64cf1-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="64cf1-114">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="64cf1-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="64cf1-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="64cf1-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="64cf1-116">[out] Ponteiro para um ponteiro para a **estrutura MAPIERROR** retornada contendo informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="64cf1-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="64cf1-117">O  _parâmetro lppMAPIError_ pode ser definido como NULL se uma estrutura **MAPIERROR** com informações apropriadas não puder ser fornecida.</span><span class="sxs-lookup"><span data-stu-id="64cf1-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="64cf1-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="64cf1-118">Return value</span></span>

<span data-ttu-id="64cf1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="64cf1-119">S_OK</span></span> 
  
> <span data-ttu-id="64cf1-120">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="64cf1-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="64cf1-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="64cf1-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="64cf1-122">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação só dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="64cf1-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64cf1-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="64cf1-123">Remarks</span></span>

<span data-ttu-id="64cf1-124">O **método IMAPITable::GetLastError** retorna informações detalhadas, se disponíveis, sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="64cf1-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="64cf1-125">Essas informações podem ser exibidas em uma mensagem ou em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="64cf1-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="64cf1-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="64cf1-126">Notes to callers</span></span>

<span data-ttu-id="64cf1-127">Chame **GetLastError** sempre que precisar exibir informações sobre um erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="64cf1-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="64cf1-128">Você pode usar a estrutura [MAPIERROR](mapierror.md) apontada pelo parâmetro  _lppMAPIError_ se o objeto table fornece um somente se **GetLastError** retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="64cf1-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="64cf1-129">Às vezes, a implementação da tabela não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="64cf1-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="64cf1-130">Nessa situação, o ponteiro em  _lppMAPIError_ é definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="64cf1-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="64cf1-131">Para liberar toda a memória alocada para a **estrutura MAPIERROR,** chame a [função MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="64cf1-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="64cf1-132">Para obter mais informações sobre **o método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="64cf1-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="64cf1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="64cf1-133">See also</span></span>



[<span data-ttu-id="64cf1-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="64cf1-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="64cf1-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="64cf1-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="64cf1-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="64cf1-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

