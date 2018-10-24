---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ef5fee7a2e84133f88a00703f7602831d26e3d3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594723"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="ef944-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ef944-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="ef944-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef944-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef944-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior.</span><span class="sxs-lookup"><span data-stu-id="ef944-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ef944-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef944-106">Parameters</span></span>

 <span data-ttu-id="ef944-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ef944-107">_hResult_</span></span>
  
> <span data-ttu-id="ef944-108">[in] Um identificador para o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="ef944-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="ef944-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ef944-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ef944-110">[in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="ef944-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="ef944-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="ef944-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ef944-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ef944-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ef944-113">As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef944-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ef944-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ef944-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ef944-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ef944-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ef944-116">[out] Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="ef944-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ef944-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se o provedor não pode fornecer uma estrutura **MAPIERROR** com as informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ef944-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ef944-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ef944-118">Return value</span></span>

<span data-ttu-id="ef944-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef944-119">S_OK</span></span> 
  
> <span data-ttu-id="ef944-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ef944-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ef944-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ef944-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ef944-122">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef944-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef944-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef944-123">Remarks</span></span>

<span data-ttu-id="ef944-124">Provedores de serviços de implementam o método **IMAPIControl::GetLastError** para fornecer informações sobre uma chamada de método anterior que falharam.</span><span class="sxs-lookup"><span data-stu-id="ef944-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="ef944-125">MAPI pode dar obter informações detalhadas sobre o erro usuários exibindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo ou de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ef944-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ef944-126">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ef944-126">Notes to implementers</span></span>

<span data-ttu-id="ef944-127">Você não precisará ter informações a serem incluídas na estrutura de **MAPIERROR** para cada erro.</span><span class="sxs-lookup"><span data-stu-id="ef944-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="ef944-128">Não é possível determinar qual foi o erro anterior.</span><span class="sxs-lookup"><span data-stu-id="ef944-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="ef944-129">Se você tiver informações, retorne S_OK e os dados apropriados na estrutura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="ef944-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="ef944-130">Se nenhuma informação estiver disponível, retornam S_OK e um ponteiro como NULL para o parâmetro _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="ef944-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="ef944-131">Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="ef944-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef944-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef944-132">See also</span></span>



[<span data-ttu-id="ef944-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ef944-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ef944-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ef944-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ef944-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef944-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

