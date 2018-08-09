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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767559"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="6cd38-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6cd38-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="6cd38-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6cd38-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6cd38-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cd38-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="6cd38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cd38-106">Parameters</span></span>

 <span data-ttu-id="6cd38-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="6cd38-107">_hResult_</span></span>
  
> <span data-ttu-id="6cd38-108">[in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior para o objeto de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cd38-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="6cd38-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6cd38-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6cd38-110">[in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="6cd38-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="6cd38-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6cd38-111">The following flag can be set:</span></span>
    
<span data-ttu-id="6cd38-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6cd38-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6cd38-113">As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6cd38-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="6cd38-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6cd38-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6cd38-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="6cd38-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="6cd38-116">[out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="6cd38-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="6cd38-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhum **MAPIERROR** para retornar.</span><span class="sxs-lookup"><span data-stu-id="6cd38-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6cd38-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6cd38-118">Return value</span></span>

<span data-ttu-id="6cd38-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6cd38-119">S_OK</span></span> 
  
> <span data-ttu-id="6cd38-120">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="6cd38-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6cd38-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6cd38-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6cd38-122">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="6cd38-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6cd38-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cd38-123">Remarks</span></span>

<span data-ttu-id="6cd38-124">Use o método **IMSLogon::GetLastError** para recuperar informações a serem exibidas em uma mensagem ao usuário sobre o último erro retornado de uma chamada de método do objeto de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cd38-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="6cd38-125">Para liberar toda a memória alocada pelo MAPI para a estrutura **MAPIERROR** retornada, aplicativos cliente precisará chamar apenas a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6cd38-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="6cd38-126">O valor de retorno de **GetLastError** deve ser S_OK para um aplicativo para usar o **MAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="6cd38-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="6cd38-127">Mesmo se o valor de retorno é S_OK, um **MAPIERROR** não pode ser retornado.</span><span class="sxs-lookup"><span data-stu-id="6cd38-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="6cd38-128">Se a implementação não puder determinar qual foi o último erro, ou se um **MAPIERROR** não está disponível para que o erro, **GetLastError** retorna um ponteiro como NULL em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6cd38-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6cd38-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cd38-129">See also</span></span>



[<span data-ttu-id="6cd38-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6cd38-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6cd38-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6cd38-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6cd38-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6cd38-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

