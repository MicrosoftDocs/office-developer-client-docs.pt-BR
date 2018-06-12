---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 807e592cf535ac060fd275075035ae8beb7d6e78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766853"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="52ab8-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="52ab8-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="52ab8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52ab8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52ab8-105">Compara dois identificadores de entrada que pertencem a um provedor de catálogo de endereço específico para determinar se eles se referem ao mesmo objeto de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="52ab8-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="52ab8-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="52ab8-106">Parameters</span></span>

 <span data-ttu-id="52ab8-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="52ab8-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="52ab8-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="52ab8-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="52ab8-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="52ab8-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="52ab8-110">[in] Um ponteiro para o primeiro identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="52ab8-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="52ab8-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="52ab8-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="52ab8-112">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="52ab8-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="52ab8-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="52ab8-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="52ab8-114">[in] Um ponteiro para o segundo identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="52ab8-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="52ab8-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52ab8-115">_ulFlags_</span></span>
  
> <span data-ttu-id="52ab8-116">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="52ab8-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="52ab8-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="52ab8-117">_lpulResult_</span></span>
  
> <span data-ttu-id="52ab8-118">[out] Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="52ab8-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="52ab8-119">O conteúdo de _lpulResult_ estiverem definido como TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, o conteúdo estiver definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="52ab8-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="52ab8-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="52ab8-120">Return value</span></span>

<span data-ttu-id="52ab8-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="52ab8-121">S_OK</span></span> 
  
> <span data-ttu-id="52ab8-122">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="52ab8-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="52ab8-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="52ab8-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="52ab8-124">Um ou ambos os identificadores de entrada passados com os parâmetros _lpEntryID1_ ou _lpEntryID2_ não são reconhecidos pelas qualquer provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="52ab8-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="52ab8-125">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="52ab8-125">Remarks</span></span>

<span data-ttu-id="52ab8-126">Aplicativos cliente e o serviço provedores chamada do método **CompareEntryIDs** para comparar os dois identificadores de entrada que pertence a um provedor de catálogo de endereço para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="52ab8-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="52ab8-127">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="52ab8-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="52ab8-128">Essa situação poderá ocorrer, por exemplo, depois que uma nova versão de um provedor de catálogo de endereços é instalada.</span><span class="sxs-lookup"><span data-stu-id="52ab8-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="52ab8-129">MAPI passa essa chamada para o endereço provedor de catálogo que é responsável pelos identificadores de entrada, determinando o provedor apropriado combinando a estrutura [MAPIUID](mapiuid.md) em identificadores de entrada com a estrutura **MAPIUID** registrada pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="52ab8-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="52ab8-130">Se os identificadores de dois entrada se referir ao mesmo objeto, **CompareEntryIDs** define o conteúdo do parâmetro _lpulResult_ como TRUE; Se eles se referir a objetos diferentes, **CompareEntryIDs** define o conteúdo como FALSE.</span><span class="sxs-lookup"><span data-stu-id="52ab8-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="52ab8-131">Em ambos os casos, **CompareEntryIDs** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="52ab8-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="52ab8-132">Se **CompareEntryIDs** retornará um erro, que pode ocorrer se nenhum provedor de catálogo de endereços registrou uma estrutura **MAPIUID** que coincida com a pessoa nos identificadores de entrada, clientes e provedores não devem levar qualquer ação com base no resultado do comparação.</span><span class="sxs-lookup"><span data-stu-id="52ab8-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="52ab8-133">Em vez disso, eles devem levar a abordagem mais conservadora à ação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="52ab8-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52ab8-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="52ab8-134">See also</span></span>



[<span data-ttu-id="52ab8-135">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="52ab8-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

