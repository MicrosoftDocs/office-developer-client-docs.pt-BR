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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593813"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="02d26-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="02d26-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="02d26-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02d26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02d26-105">Retorna uma estrutura [MAPIERROR](mapierror.md) contendo informações sobre o erro anterior na tabela.</span><span class="sxs-lookup"><span data-stu-id="02d26-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="02d26-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02d26-106">Parameters</span></span>

 <span data-ttu-id="02d26-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="02d26-107">_hResult_</span></span>
  
> <span data-ttu-id="02d26-108">[in] HRESULT que contém o erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="02d26-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="02d26-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="02d26-109">_ulFlags_</span></span>
  
> <span data-ttu-id="02d26-110">[in] Bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="02d26-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="02d26-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="02d26-111">The following flag can be set:</span></span>
    
<span data-ttu-id="02d26-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="02d26-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="02d26-113">As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="02d26-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="02d26-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="02d26-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="02d26-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="02d26-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="02d26-116">[out] Ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado contendo informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="02d26-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="02d26-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não pode ser fornecida uma estrutura **MAPIERROR** com as informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="02d26-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="02d26-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="02d26-118">Return value</span></span>

<span data-ttu-id="02d26-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="02d26-119">S_OK</span></span> 
  
> <span data-ttu-id="02d26-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="02d26-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="02d26-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="02d26-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="02d26-122">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="02d26-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02d26-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="02d26-123">Remarks</span></span>

<span data-ttu-id="02d26-124">O método **IMAPITable::GetLastError** retorna informações detalhadas, se estiver disponível, sobre uma chamada de método anterior que falharam.</span><span class="sxs-lookup"><span data-stu-id="02d26-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="02d26-125">Essas informações podem ser exibidas em uma mensagem ou uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="02d26-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="02d26-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="02d26-126">Notes to callers</span></span>

<span data-ttu-id="02d26-127">Chame **GetLastError** sempre que for necessário exibir informações sobre um erro ao usuário.</span><span class="sxs-lookup"><span data-stu-id="02d26-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="02d26-128">Você pode fazer uso do [MAPIERROR](mapierror.md) estrutura apontado pelo parâmetro _lppMAPIError_ se o objeto table fornece um somente se **GetLastError** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="02d26-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="02d26-129">Em alguns casos, a implementação de tabela não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="02d26-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="02d26-130">Nessa situação, o ponteiro do _lppMAPIError_ é definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="02d26-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="02d26-131">Para liberar toda a memória alocada para a estrutura **MAPIERROR** , chame a função de [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="02d26-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="02d26-132">Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="02d26-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="02d26-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="02d26-133">See also</span></span>



[<span data-ttu-id="02d26-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="02d26-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="02d26-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="02d26-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="02d26-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02d26-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

