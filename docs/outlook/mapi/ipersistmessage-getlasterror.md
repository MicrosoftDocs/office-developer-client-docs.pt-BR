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
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317161"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="69aca-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="69aca-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="69aca-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69aca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69aca-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto Form.</span><span class="sxs-lookup"><span data-stu-id="69aca-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="69aca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69aca-106">Parameters</span></span>

 <span data-ttu-id="69aca-107">_And_</span><span class="sxs-lookup"><span data-stu-id="69aca-107">_hResult_</span></span>
  
> <span data-ttu-id="69aca-108">no Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="69aca-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="69aca-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69aca-109">_ulFlags_</span></span>
  
> <span data-ttu-id="69aca-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="69aca-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="69aca-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="69aca-111">The following flag can be set:</span></span>
    
<span data-ttu-id="69aca-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="69aca-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="69aca-113">As cadeias de caracteres na estrutura [MAPIERROR](mapierror.md) retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="69aca-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="69aca-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="69aca-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="69aca-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="69aca-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="69aca-116">bota Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="69aca-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="69aca-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se o formulário não puder fornecer as informações apropriadas para uma estrutura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="69aca-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="69aca-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="69aca-118">Return value</span></span>

<span data-ttu-id="69aca-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="69aca-119">S_OK</span></span> 
  
> <span data-ttu-id="69aca-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="69aca-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="69aca-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="69aca-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="69aca-122">O sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não é compatível com Unicode, ou o MAPI_UNICODE não foi definido e o provedor de catálogo de endereços oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="69aca-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69aca-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="69aca-123">Remarks</span></span>

<span data-ttu-id="69aca-124">Os objetos Form implementam o método **IPersistMessage:: GetLastError** para fornecer informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="69aca-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="69aca-125">Os visualizadores de formulários podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura [MAPIERROR](mapierror.md) em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="69aca-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="69aca-126">Uma chamada para **GetLastError** não afeta o estado do formulário.</span><span class="sxs-lookup"><span data-stu-id="69aca-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="69aca-127">Quando **GetLastError** retorna, o formulário permanece no estado em que estava antes da chamada ser feita.</span><span class="sxs-lookup"><span data-stu-id="69aca-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="69aca-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="69aca-128">Notes to callers</span></span>

<span data-ttu-id="69aca-129">Você pode usar a estrutura **MAPIERROR** , se o formulário fornecer um, que será apontado pelo parâmetro _lppMAPIError_ somente se GetLastError retornar S_OK. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="69aca-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="69aca-130">Às vezes, o formulário não pode determinar o que foi o último erro ou não faz mais para relatar o erro.</span><span class="sxs-lookup"><span data-stu-id="69aca-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="69aca-131">Nessa situação, o formulário retorna um ponteiro para nulo em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="69aca-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="69aca-132">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="69aca-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69aca-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="69aca-133">See also</span></span>



[<span data-ttu-id="69aca-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="69aca-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="69aca-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="69aca-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="69aca-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69aca-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

