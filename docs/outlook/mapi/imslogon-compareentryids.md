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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c2e6600af66f3dab8ff0fbb5442a1354687a3cbb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767530"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="2c27b-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2c27b-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="2c27b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c27b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c27b-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="2c27b-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="2c27b-106">MAPI refere-se essa chamada para um provedor de serviço somente se os identificadores exclusivos (UIDs) em ambos os identificadores de entrada a ser comparada são manipulados por esse provedor.</span><span class="sxs-lookup"><span data-stu-id="2c27b-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2c27b-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="2c27b-107">Parameters</span></span>

 <span data-ttu-id="2c27b-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2c27b-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="2c27b-109">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="2c27b-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="2c27b-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2c27b-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="2c27b-111">[in] Um ponteiro para o primeiro identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="2c27b-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2c27b-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2c27b-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="2c27b-113">[in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="2c27b-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="2c27b-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2c27b-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="2c27b-115">[in] Um ponteiro para o segundo identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="2c27b-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2c27b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c27b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="2c27b-117">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2c27b-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2c27b-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="2c27b-118">_lpulResult_</span></span>
  
> <span data-ttu-id="2c27b-119">[out] Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="2c27b-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="2c27b-120">TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="2c27b-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2c27b-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2c27b-121">Return value</span></span>

<span data-ttu-id="2c27b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c27b-122">S_OK</span></span> 
  
> <span data-ttu-id="2c27b-123">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="2c27b-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c27b-124">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="2c27b-124">Remarks</span></span>

<span data-ttu-id="2c27b-125">Provedores de armazenamento de mensagem implementam o método **IMSLogon::CompareEntryIDs** para comparar os dois identificadores de entrada para uma dada entrada em um armazenamento de mensagens para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="2c27b-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="2c27b-126">Se os identificadores de dois entrada se referir ao mesmo objeto, **CompareEntryIDs** define o parâmetro _lpulResult_ como TRUE; Se eles se referir a objetos diferentes, **CompareEntryIDs** define _lpulResult_ como FALSE.</span><span class="sxs-lookup"><span data-stu-id="2c27b-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="2c27b-127">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="2c27b-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="2c27b-128">Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada.</span><span class="sxs-lookup"><span data-stu-id="2c27b-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c27b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c27b-129">See also</span></span>



[<span data-ttu-id="2c27b-130">IMSLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c27b-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

