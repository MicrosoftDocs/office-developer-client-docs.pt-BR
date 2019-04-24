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
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286618"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="d5841-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d5841-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="d5841-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5841-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5841-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior.</span><span class="sxs-lookup"><span data-stu-id="d5841-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d5841-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5841-106">Parameters</span></span>

 <span data-ttu-id="d5841-107">_And_</span><span class="sxs-lookup"><span data-stu-id="d5841-107">_hResult_</span></span>
  
> <span data-ttu-id="d5841-108">no Um identificador para o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="d5841-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="d5841-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5841-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d5841-110">no Uma bitmask de sinalizadores que controla o tipo das cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="d5841-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="d5841-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="d5841-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d5841-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d5841-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d5841-113">As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5841-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="d5841-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d5841-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d5841-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d5841-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d5841-116">bota Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="d5841-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d5841-117">O parâmetro _lppMAPIError_ pode ser definido como nulo se o provedor não puder fornecer uma estrutura **MAPIERROR** com as informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d5841-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d5841-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d5841-118">Return value</span></span>

<span data-ttu-id="d5841-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5841-119">S_OK</span></span> 
  
> <span data-ttu-id="d5841-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d5841-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d5841-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d5841-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d5841-122">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5841-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5841-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5841-123">Remarks</span></span>

<span data-ttu-id="d5841-124">Os provedores de serviços implementam o método **IMAPIControl:: GetLastError** para fornecer informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="d5841-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="d5841-125">O MAPI pode fornecer aos usuários informações detalhadas sobre o erro exibindo os dados da estrutura **MAPIERROR** em uma mensagem ou caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d5841-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d5841-126">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="d5841-126">Notes to implementers</span></span>

<span data-ttu-id="d5841-127">Você não precisa ter as informações a serem incluídas na estrutura **MAPIERROR** para cada erro.</span><span class="sxs-lookup"><span data-stu-id="d5841-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="d5841-128">Talvez não seja possível determinar o que ocorreu o erro anterior.</span><span class="sxs-lookup"><span data-stu-id="d5841-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="d5841-129">Se você tiver informações, retorne S_OK e os dados apropriados na estrutura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="d5841-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="d5841-130">Se nenhuma informação estiver disponível, retorne S_OK e um ponteiro para nulo para o parâmetro _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="d5841-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="d5841-131">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d5841-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5841-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5841-132">See also</span></span>



[<span data-ttu-id="d5841-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d5841-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d5841-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d5841-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d5841-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5841-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

