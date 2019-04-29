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
# <a name="imslogoncompareentryids"></a><span data-ttu-id="d3bb5-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="d3bb5-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="d3bb5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3bb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3bb5-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="d3bb5-106">O MAPI refere essa chamada a um provedor de serviços somente se os UIDs (identificadores exclusivos) em ambos os identificadores de entrada a serem comparados são tratados por esse provedor.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d3bb5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3bb5-107">Parameters</span></span>

 <span data-ttu-id="d3bb5-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d3bb5-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="d3bb5-109">no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="d3bb5-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="d3bb5-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d3bb5-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="d3bb5-111">no Um ponteiro para o primeiro identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="d3bb5-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d3bb5-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="d3bb5-113">no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="d3bb5-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="d3bb5-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d3bb5-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="d3bb5-115">no Um ponteiro para o segundo identificador de entrada ser comparado.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="d3bb5-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3bb5-116">_ulFlags_</span></span>
  
> <span data-ttu-id="d3bb5-117">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d3bb5-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="d3bb5-118">_lpulResult_</span></span>
  
> <span data-ttu-id="d3bb5-119">bota Um ponteiro para o resultado retornado da comparação.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="d3bb5-120">TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d3bb5-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d3bb5-121">Return value</span></span>

<span data-ttu-id="d3bb5-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3bb5-122">S_OK</span></span> 
  
> <span data-ttu-id="d3bb5-123">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3bb5-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3bb5-124">Remarks</span></span>

<span data-ttu-id="d3bb5-125">Os provedores de repositórios de mensagens implementam o método **IMSLogon:: CompareEntryIDs** para comparar dois identificadores de entrada de uma determinada entrada em um repositório de mensagens para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="d3bb5-126">Se os dois identificadores de entrada se referem ao mesmo objeto, **CompareEntryIDs** define o parâmetro _lpulResult_ como true; Se eles se referem a objetos diferentes, **CompareEntryIDs** define _lpulResult_ como false.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="d3bb5-127">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="d3bb5-128">Isso pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d3bb5-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3bb5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3bb5-129">See also</span></span>



[<span data-ttu-id="d3bb5-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3bb5-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

