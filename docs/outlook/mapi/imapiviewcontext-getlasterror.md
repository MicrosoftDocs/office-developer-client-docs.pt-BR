---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424424"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="09ade-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="09ade-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="09ade-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09ade-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09ade-105">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior ocorrendo no objeto de contexto de exibição.</span><span class="sxs-lookup"><span data-stu-id="09ade-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="09ade-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09ade-106">Parameters</span></span>

 <span data-ttu-id="09ade-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="09ade-107">_hResult_</span></span>
  
> <span data-ttu-id="09ade-108">[in] Tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="09ade-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="09ade-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09ade-109">_ulFlags_</span></span>
  
> <span data-ttu-id="09ade-110">[in] Máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="09ade-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="09ade-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="09ade-111">The following flag can be set:</span></span>
    
<span data-ttu-id="09ade-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09ade-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="09ade-113">As cadeias de caracteres na **estrutura MAPIERROR** retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="09ade-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="09ade-114">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="09ade-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="09ade-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="09ade-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="09ade-116">[out] Ponteiro para um ponteiro para a **estrutura MAPIERROR** retornada que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="09ade-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="09ade-117">Esse parâmetro pode ser definido como NULL se não houver **estrutura MAPIERROR** a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="09ade-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09ade-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="09ade-118">Return value</span></span>

<span data-ttu-id="09ade-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="09ade-119">S_OK</span></span> 
  
> <span data-ttu-id="09ade-120">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="09ade-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="09ade-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="09ade-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="09ade-122">O sinalizador MAPI_UNICODE foi definido e **GetLastError** não dá suporte a Unicode ou MAPI_UNICODE não foi definido e **GetLastError** só dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="09ade-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09ade-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="09ade-123">Remarks</span></span>

<span data-ttu-id="09ade-124">O **método IMAPIViewContext::GetLastError** fornece informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="09ade-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="09ade-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da **estrutura MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="09ade-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="09ade-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="09ade-126">Notes to callers</span></span>

<span data-ttu-id="09ade-127">Você pode usar a estrutura **MAPIERROR** apontada pelo parâmetro  _lppMAPIError_ se MAPI fornece um somente se **GetLastError** retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="09ade-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="09ade-128">Às vezes, o MAPI não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="09ade-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="09ade-129">Nessa situação, um ponteiro para NULL é retornado _em lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="09ade-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="09ade-130">Para obter mais informações sobre o **método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="09ade-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09ade-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="09ade-131">See also</span></span>



[<span data-ttu-id="09ade-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="09ade-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="09ade-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="09ade-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="09ade-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09ade-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

