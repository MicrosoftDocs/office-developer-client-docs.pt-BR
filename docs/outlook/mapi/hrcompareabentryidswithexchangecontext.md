---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436430"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="4a801-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="4a801-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="4a801-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a801-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a801-105">Compara duas **entryIDs** do livro de endereços com segurança em um perfil do Exchange múltiplo.</span><span class="sxs-lookup"><span data-stu-id="4a801-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="4a801-106">Esta função é uma função de substituição para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="4a801-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a801-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4a801-107">Header file:</span></span>  <br/> |<span data-ttu-id="4a801-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="4a801-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="4a801-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4a801-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a801-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a801-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="4a801-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="4a801-111">Called by:</span></span>  <br/> |<span data-ttu-id="4a801-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="4a801-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="4a801-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a801-113">Parameters</span></span>

 <span data-ttu-id="4a801-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="4a801-114">_pmsess_</span></span>
  
> <span data-ttu-id="4a801-115">[in] O **IMAPISession conectado.**</span><span class="sxs-lookup"><span data-stu-id="4a801-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="4a801-116">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="4a801-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4a801-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="4a801-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="4a801-118">[in] Um ponteiro para **um emsmdbUID** que identifica o Serviço do Exchange que contém o Exchange Address Book Provider que essa função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4a801-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="4a801-119">Se o identificador de entrada de entrada não for um identificador de entrada do Exchange Address Book Provider, esse parâmetro será ignorado e a chamada de função se comportará como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="4a801-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="4a801-120">Se esse parâmetro for NULL ou zero MAPIUID, essa função se comportará como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="4a801-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="4a801-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="4a801-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="4a801-122">[in] O livro de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4a801-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="4a801-123">Não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="4a801-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4a801-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4a801-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="4a801-125">[in] A contagem de byte do primeiro identificador de entrada especificado pelo parâmetro _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="4a801-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="4a801-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4a801-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="4a801-127">[in] Um ponteiro para o identificador da primeira entrada que representa a entrada do livro de endereços a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4a801-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="4a801-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4a801-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="4a801-129">[in] A contagem de byte do segundo identificador de entrada especificado pelo parâmetro _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="4a801-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="4a801-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4a801-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="4a801-131">[in] Um ponteiro para o segundo identificador de entrada usado na comparação que representa a entrada do livro de endereços a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4a801-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="4a801-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4a801-132">_ulFlags_</span></span>
  
> <span data-ttu-id="4a801-133">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4a801-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4a801-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="4a801-134">_lpulResult_</span></span>
  
> <span data-ttu-id="4a801-135">[out] Um ponteiro para o local que contém os resultados da comparação.</span><span class="sxs-lookup"><span data-stu-id="4a801-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

