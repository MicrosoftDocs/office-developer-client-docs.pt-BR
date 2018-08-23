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
ms.openlocfilehash: eb91f4998f94ffafbc33b6024228945f7c91cf43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564987"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="702a8-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="702a8-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="702a8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="702a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="702a8-105">Compara dois de catálogo de endereços **entryIDs** com segurança em um perfil do Exchange vários.</span><span class="sxs-lookup"><span data-stu-id="702a8-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="702a8-106">Esta é uma função de substituição para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="702a8-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="702a8-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="702a8-107">Header file:</span></span>  <br/> |<span data-ttu-id="702a8-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="702a8-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="702a8-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="702a8-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="702a8-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="702a8-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="702a8-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="702a8-111">Called by:</span></span>  <br/> |<span data-ttu-id="702a8-112">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="702a8-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="702a8-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="702a8-113">Parameters</span></span>

 <span data-ttu-id="702a8-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="702a8-114">_pmsess_</span></span>
  
> <span data-ttu-id="702a8-115">[in] O conectado **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="702a8-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="702a8-116">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="702a8-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="702a8-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="702a8-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="702a8-118">[in] Um ponteiro para uma **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que esta função deve usar para exibir detalhes sobre o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="702a8-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="702a8-119">Se o identificador de entrada de entrada não é um identificador de entrada do provedor de catálogo de endereços do Exchange, esse parâmetro será ignorado e a chamada de função se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="702a8-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="702a8-120">Se esse parâmetro for NULL ou um zero MAPIUID, essa função se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="702a8-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="702a8-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="702a8-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="702a8-122">[in] O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="702a8-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="702a8-123">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="702a8-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="702a8-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="702a8-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="702a8-125">[in] A contagem de bytes do primeiro identificador de entrada especificada pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="702a8-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="702a8-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="702a8-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="702a8-127">[in] Um ponteiro para o primeiro identificador de entrada que representa a entrada do catálogo de endereços para comparar.</span><span class="sxs-lookup"><span data-stu-id="702a8-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="702a8-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="702a8-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="702a8-129">[in] A contagem de bytes do identificador da segunda entrada especificado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="702a8-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="702a8-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="702a8-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="702a8-131">[in] Um ponteiro para o segundo identificador de entrada utilizado na comparação que representa a entrada do catálogo de endereços para comparar.</span><span class="sxs-lookup"><span data-stu-id="702a8-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="702a8-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="702a8-132">_ulFlags_</span></span>
  
> <span data-ttu-id="702a8-133">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="702a8-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="702a8-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="702a8-134">_lpulResult_</span></span>
  
> <span data-ttu-id="702a8-135">[out] Um ponteiro para o local que contém os resultados da comparação.</span><span class="sxs-lookup"><span data-stu-id="702a8-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

