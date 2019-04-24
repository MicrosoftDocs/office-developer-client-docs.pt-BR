---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317294"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="6c8d5-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6c8d5-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="6c8d5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c8d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c8d5-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="6c8d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c8d5-106">Parameters</span></span>

 <span data-ttu-id="6c8d5-107">_And_</span><span class="sxs-lookup"><span data-stu-id="6c8d5-107">_hResult_</span></span>
  
> <span data-ttu-id="6c8d5-108">no Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior para o objeto do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="6c8d5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c8d5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6c8d5-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="6c8d5-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6c8d5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="6c8d5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c8d5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6c8d5-113">As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="6c8d5-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6c8d5-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="6c8d5-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="6c8d5-116">bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="6c8d5-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhum **MAPIERROR** a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6c8d5-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6c8d5-118">Return value</span></span>

<span data-ttu-id="6c8d5-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c8d5-119">S_OK</span></span> 
  
> <span data-ttu-id="6c8d5-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6c8d5-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6c8d5-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6c8d5-122">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c8d5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c8d5-123">Remarks</span></span>

<span data-ttu-id="6c8d5-124">Use o método **IMSLogon:: GetLastError** para recuperar informações a serem exibidas em uma mensagem para o usuário sobre o último erro retornado de uma chamada de método para o objeto do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="6c8d5-125">Para liberar todas as memórias alocadas por MAPI para a estrutura **MAPIERROR** retornada, os aplicativos clientes precisam chamar somente a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6c8d5-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="6c8d5-126">O valor de retorno \*\*\*\* de GetLastError deve ser S_OK para que um aplicativo use o **MAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="6c8d5-127">Mesmo que o valor de retorno seja S_OK, um **MAPIERROR** pode não ser retornado.</span><span class="sxs-lookup"><span data-stu-id="6c8d5-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="6c8d5-128">Se a implementação não puder determinar o último erro, ou se um **MAPIERROR** não estiver disponível para esse erro, GetLastError retornará um ponteiro para NULL em _lppMAPIError_ em vez disso. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6c8d5-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c8d5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c8d5-129">See also</span></span>



[<span data-ttu-id="6c8d5-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6c8d5-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6c8d5-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6c8d5-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6c8d5-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c8d5-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

