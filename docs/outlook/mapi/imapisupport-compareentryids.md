---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9dbf02fc94519d40431fb6bd493ef8e68df59d11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566541"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="59079-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="59079-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="59079-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59079-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59079-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="59079-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="59079-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59079-106">Parameters</span></span>

 <span data-ttu-id="59079-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="59079-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="59079-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="59079-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="59079-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="59079-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="59079-110">[in] Um ponteiro para o primeiro identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="59079-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="59079-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="59079-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="59079-112">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="59079-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="59079-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="59079-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="59079-114">[in] Um ponteiro para o segundo identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="59079-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="59079-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59079-115">_ulFlags_</span></span>
  
> <span data-ttu-id="59079-116">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="59079-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="59079-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="59079-117">_lpulResult_</span></span>
  
> <span data-ttu-id="59079-118">[out] Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="59079-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="59079-119">TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="59079-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59079-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="59079-120">Return value</span></span>

<span data-ttu-id="59079-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="59079-121">S_OK</span></span> 
  
> <span data-ttu-id="59079-122">A comparação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="59079-122">The comparison was successful.</span></span>
    
<span data-ttu-id="59079-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="59079-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="59079-124">Um ou ambos os identificadores de entrada especificados como parâmetros não fazem referência a objetos válidos, possivelmente porque eles estão atualmente não abertas e não está disponível.</span><span class="sxs-lookup"><span data-stu-id="59079-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59079-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="59079-125">Remarks</span></span>

<span data-ttu-id="59079-126">O método **IMAPISupport::CompareEntryIDs** é implementado para endereço livro e mensagem provedor suporte objetos store.</span><span class="sxs-lookup"><span data-stu-id="59079-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="59079-127">**CompareEntryIDs** compara dois identificadores de entrada que pertencem a um provedor de serviços único para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="59079-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="59079-128">MAPI extrai a parte [MAPIUID](mapiuid.md) de identificadores de entrada para determinar o responsável para os objetos do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="59079-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="59079-129">MAPI, em seguida, chama o método de **CompareEntryIDs** do seu objeto logon para realizar a comparação.</span><span class="sxs-lookup"><span data-stu-id="59079-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="59079-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="59079-130">Notes to callers</span></span>

 <span data-ttu-id="59079-131">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="59079-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="59079-132">Esta situação pode ocorrer, por exemplo, depois que uma nova versão de um provedor de serviço é instalada.</span><span class="sxs-lookup"><span data-stu-id="59079-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="59079-133">Se **CompareEntryIDs** retornará um erro, não terão qualquer ação baseada no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="59079-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="59079-134">Em vez disso, a abordagem mais conservadora levar possíveis.</span><span class="sxs-lookup"><span data-stu-id="59079-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="59079-135">**CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiverem uma estrutura inválida de **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="59079-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59079-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="59079-136">See also</span></span>



[<span data-ttu-id="59079-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="59079-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="59079-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="59079-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

