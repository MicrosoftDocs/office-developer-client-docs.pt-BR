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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431040"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="2256c-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2256c-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="2256c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2256c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2256c-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="2256c-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="2256c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2256c-106">Parameters</span></span>

 <span data-ttu-id="2256c-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2256c-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="2256c-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="2256c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="2256c-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2256c-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="2256c-110">no Um ponteiro para o primeiro identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2256c-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2256c-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2256c-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="2256c-112">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="2256c-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="2256c-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2256c-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="2256c-114">no Um ponteiro para o segundo identificador de entrada ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2256c-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2256c-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2256c-115">_ulFlags_</span></span>
  
> <span data-ttu-id="2256c-116">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2256c-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2256c-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="2256c-117">_lpulResult_</span></span>
  
> <span data-ttu-id="2256c-118">bota Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="2256c-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="2256c-119">TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="2256c-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2256c-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2256c-120">Return value</span></span>

<span data-ttu-id="2256c-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="2256c-121">S_OK</span></span> 
  
> <span data-ttu-id="2256c-122">A comparação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2256c-122">The comparison was successful.</span></span>
    
<span data-ttu-id="2256c-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2256c-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2256c-124">Um ou ambos os identificadores de entrada especificados como parâmetros não se referem a objetos válidos, possivelmente porque estão atualmente não abertos e disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2256c-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2256c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2256c-125">Remarks</span></span>

<span data-ttu-id="2256c-126">O método **IMAPISupport:: CompareEntryIDs** é implementado para o catálogo de endereços e os objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2256c-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="2256c-127">**CompareEntryIDs** compara dois identificadores de entrada que pertencem a um único provedor de serviços para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="2256c-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="2256c-128">MAPI extrai a parte [MAPIUID](mapiuid.md) dos identificadores de entrada para determinar o provedor de serviços responsável pelos objetos.</span><span class="sxs-lookup"><span data-stu-id="2256c-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="2256c-129">Em seguida, o MAPI chama o método **CompareEntryIDs** do objeto logon para executar a comparação.</span><span class="sxs-lookup"><span data-stu-id="2256c-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2256c-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="2256c-130">Notes to callers</span></span>

 <span data-ttu-id="2256c-131">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="2256c-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="2256c-132">Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="2256c-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="2256c-133">Se **CompareEntryIDs** retornar um erro, não realize nenhuma ação com base no resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="2256c-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="2256c-134">Em vez disso, considere a abordagem mais conservadora possível.</span><span class="sxs-lookup"><span data-stu-id="2256c-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="2256c-135">**CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiverem uma estrutura **MAPIUID** inválida.</span><span class="sxs-lookup"><span data-stu-id="2256c-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2256c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2256c-136">See also</span></span>



[<span data-ttu-id="2256c-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2256c-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2256c-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2256c-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

