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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426706"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="08b31-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="08b31-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="08b31-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08b31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08b31-105">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto form.</span><span class="sxs-lookup"><span data-stu-id="08b31-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="08b31-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08b31-106">Parameters</span></span>

 <span data-ttu-id="08b31-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="08b31-107">_hResult_</span></span>
  
> <span data-ttu-id="08b31-108">[in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="08b31-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="08b31-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08b31-109">_ulFlags_</span></span>
  
> <span data-ttu-id="08b31-110">[in] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="08b31-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="08b31-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="08b31-111">The following flag can be set:</span></span>
    
<span data-ttu-id="08b31-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08b31-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="08b31-113">As cadeias de caracteres na [estrutura MAPIERROR](mapierror.md) retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="08b31-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="08b31-114">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="08b31-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="08b31-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="08b31-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="08b31-116">[out] Um ponteiro para um ponteiro para uma **estrutura MAPIERROR** que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="08b31-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="08b31-117">O _parâmetro lppMAPIError_ pode ser definido como NULL se o formulário não puder fornecer informações apropriadas para uma **estrutura MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="08b31-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08b31-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="08b31-118">Return value</span></span>

<span data-ttu-id="08b31-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="08b31-119">S_OK</span></span> 
  
> <span data-ttu-id="08b31-120">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="08b31-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="08b31-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="08b31-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="08b31-122">O sinalizador MAPI_UNICODE de endereços foi definido e o provedor do address book não oferece suporte a Unicode ou MAPI_UNICODE não foi definido e o provedor de agendas oferece suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="08b31-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08b31-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="08b31-123">Remarks</span></span>

<span data-ttu-id="08b31-124">Os objetos de formulário implementam o método **IPersistMessage::GetLastError** para fornecer informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="08b31-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="08b31-125">Visualizadores de formulário podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da [estrutura MAPIERROR](mapierror.md) em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08b31-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="08b31-126">Uma chamada para **GetLastError** não afeta o estado do formulário.</span><span class="sxs-lookup"><span data-stu-id="08b31-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="08b31-127">Quando **GetLastError** retorna, o formulário permanece no estado em que estava antes da chamada ser feita.</span><span class="sxs-lookup"><span data-stu-id="08b31-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="08b31-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="08b31-128">Notes to callers</span></span>

<span data-ttu-id="08b31-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span><span class="sxs-lookup"><span data-stu-id="08b31-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="08b31-130">Às vezes, o formulário não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="08b31-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="08b31-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span><span class="sxs-lookup"><span data-stu-id="08b31-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="08b31-132">Para obter mais informações sobre **o método GetLastError,** consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="08b31-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08b31-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="08b31-133">See also</span></span>



[<span data-ttu-id="08b31-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="08b31-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="08b31-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="08b31-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="08b31-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08b31-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

