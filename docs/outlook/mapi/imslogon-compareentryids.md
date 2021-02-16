---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410130"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="1621d-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1621d-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="1621d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1621d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1621d-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="1621d-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="1621d-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span><span class="sxs-lookup"><span data-stu-id="1621d-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="1621d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1621d-107">Parameters</span></span>

 <span data-ttu-id="1621d-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1621d-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="1621d-109">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID1_  _._</span><span class="sxs-lookup"><span data-stu-id="1621d-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="1621d-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1621d-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="1621d-111">[in] Um ponteiro para o identificador da primeira entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="1621d-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1621d-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1621d-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="1621d-113">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID2_  _._</span><span class="sxs-lookup"><span data-stu-id="1621d-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="1621d-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1621d-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="1621d-115">[in] Um ponteiro para o segundo identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="1621d-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1621d-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1621d-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1621d-117">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1621d-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1621d-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="1621d-118">_lpulResult_</span></span>
  
> <span data-ttu-id="1621d-119">[out] Um ponteiro para o resultado retornado da comparação.</span><span class="sxs-lookup"><span data-stu-id="1621d-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="1621d-120">TRUE se os dois identificadores de entrada se referirem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="1621d-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1621d-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1621d-121">Return value</span></span>

<span data-ttu-id="1621d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1621d-122">S_OK</span></span> 
  
> <span data-ttu-id="1621d-123">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1621d-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1621d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1621d-124">Remarks</span></span>

<span data-ttu-id="1621d-125">Os provedores de armazenamento de mensagens implementam o método **IMSLogon::CompareEntryIDs** para comparar dois identificadores de entrada para uma determinada entrada em um armazenamento de mensagens para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="1621d-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="1621d-126">Se os dois identificadores de entrada se referirem ao mesmo objeto, **CompareEntryIDs** define o parâmetro  _lpulResult_ como TRUE; se eles se referirem a objetos diferentes, **CompareEntryIDs** define  _lpulResult_ como FALSE.</span><span class="sxs-lookup"><span data-stu-id="1621d-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="1621d-127">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="1621d-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="1621d-128">Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada.</span><span class="sxs-lookup"><span data-stu-id="1621d-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1621d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1621d-129">See also</span></span>



[<span data-ttu-id="1621d-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1621d-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

