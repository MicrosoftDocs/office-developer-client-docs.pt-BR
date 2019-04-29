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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424256"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="78516-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="78516-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="78516-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78516-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78516-105">Compara dois identificadores de entrada que pertencem a um determinado provedor de catálogo de endereços para determinar se eles se referem ao mesmo objeto de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="78516-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="78516-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78516-106">Parameters</span></span>

 <span data-ttu-id="78516-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="78516-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="78516-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="78516-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="78516-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="78516-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="78516-110">no Um ponteiro para o primeiro identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="78516-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="78516-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="78516-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="78516-112">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="78516-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="78516-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="78516-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="78516-114">no Um ponteiro para o segundo identificador de entrada ser comparado.</span><span class="sxs-lookup"><span data-stu-id="78516-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="78516-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78516-115">_ulFlags_</span></span>
  
> <span data-ttu-id="78516-116">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="78516-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="78516-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="78516-117">_lpulResult_</span></span>
  
> <span data-ttu-id="78516-118">bota Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="78516-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="78516-119">O conteúdo de _lpulResult_ é definido como true se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, o conteúdo será definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="78516-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="78516-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="78516-120">Return value</span></span>

<span data-ttu-id="78516-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="78516-121">S_OK</span></span> 
  
> <span data-ttu-id="78516-122">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="78516-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="78516-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="78516-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="78516-124">Um ou ambos os identificadores de entrada passados com os parâmetros _lpEntryID1_ ou _lpEntryID2_ não são reconhecidos por qualquer provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="78516-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="78516-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="78516-125">Remarks</span></span>

<span data-ttu-id="78516-126">Aplicativos cliente e provedores de serviços chamam o método **CompareEntryIDs** para comparar dois identificadores de entrada que pertencem a um único provedor de catálogo de endereços para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="78516-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="78516-127">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="78516-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="78516-128">Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="78516-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="78516-129">O MAPI passa essa chamada para o provedor de catálogo de endereços responsável pelos identificadores de entrada, determinando o provedor apropriado, combinando a estrutura [MAPIUID](mapiuid.md) nos identificadores de entrada com a estrutura **MAPIUID** registrada pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="78516-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="78516-130">Se os dois identificadores de entrada se referem ao mesmo objeto, **CompareEntryIDs** define o conteúdo do parâmetro _lpulResult_ como true; Se eles se referem a objetos diferentes, o **CompareEntryIDs** define o conteúdo como false.</span><span class="sxs-lookup"><span data-stu-id="78516-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="78516-131">Em ambos os casos, **CompareEntryIDs** retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="78516-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="78516-132">Se **CompareEntryIDs** retornar um erro, que pode ocorrer se nenhum provedor de catálogo de endereços tiver registrado uma estrutura **MAPIUID** que coincida com a do identificador de entrada, os clientes e provedores não deverão realizar nenhuma ação com base no resultado da diagrama.</span><span class="sxs-lookup"><span data-stu-id="78516-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="78516-133">Em vez disso, eles devem adotar a abordagem mais conservadora para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="78516-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78516-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="78516-134">See also</span></span>



[<span data-ttu-id="78516-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="78516-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

