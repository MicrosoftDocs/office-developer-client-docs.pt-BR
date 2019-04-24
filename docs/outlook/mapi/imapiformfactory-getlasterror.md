---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342144"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="211df-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="211df-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="211df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="211df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="211df-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto Factory de formulários.</span><span class="sxs-lookup"><span data-stu-id="211df-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="211df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="211df-106">Parameters</span></span>

 <span data-ttu-id="211df-107">_And_</span><span class="sxs-lookup"><span data-stu-id="211df-107">_hResult_</span></span>
  
> <span data-ttu-id="211df-108">no Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="211df-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="211df-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="211df-109">_ulFlags_</span></span>
  
> <span data-ttu-id="211df-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="211df-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="211df-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="211df-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="211df-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="211df-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="211df-113">As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="211df-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="211df-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="211df-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="211df-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="211df-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="211df-116">bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="211df-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="211df-117">Esse parâmetro pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="211df-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="211df-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="211df-118">Return value</span></span>

<span data-ttu-id="211df-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="211df-119">S_OK</span></span> 
  
> <span data-ttu-id="211df-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="211df-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="211df-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="211df-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="211df-122">O sinalizador MAPI_UNICODE foi definido e getLastError não tem suporte para Unicode, ou MAPI_UNICODE não foi definido e **GetLastError** oferece suporte somente para Unicode. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="211df-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="211df-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="211df-123">Remarks</span></span>

<span data-ttu-id="211df-124">O método **IMAPIFormFactory:: GetLastError** fornece informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="211df-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="211df-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="211df-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="211df-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="211df-126">Notes to callers</span></span>

<span data-ttu-id="211df-127">Você pode usar a estrutura **MAPIERROR** indicada pelo parâmetro _LPPMAPIERROR_ se a MAPI fornecer somente um se GetLastError retornar \*\*\*\* S_OK.</span><span class="sxs-lookup"><span data-stu-id="211df-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="211df-128">Às vezes, o MAPI não pode determinar o que foi o último erro ou não faz mais para relatar o erro.</span><span class="sxs-lookup"><span data-stu-id="211df-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="211df-129">Nessa situação, um ponteiro para nulo é retornado em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="211df-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="211df-130">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [usando erros estendidos](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="211df-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="211df-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="211df-131">See also</span></span>



[<span data-ttu-id="211df-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="211df-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="211df-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="211df-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="211df-134">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="211df-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

