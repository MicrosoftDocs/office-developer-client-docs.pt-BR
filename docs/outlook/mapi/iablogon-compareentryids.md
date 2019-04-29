---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438369"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="ee344-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ee344-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="ee344-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee344-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee344-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="ee344-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a><span data-ttu-id="ee344-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee344-106">Parameters</span></span>

 <span data-ttu-id="ee344-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ee344-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="ee344-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="ee344-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="ee344-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="ee344-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="ee344-110">no Um ponteiro para o primeiro identificador de entrada a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ee344-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ee344-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ee344-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="ee344-112">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="ee344-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="ee344-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="ee344-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="ee344-114">no Um ponteiro para o segundo identificador de entrada ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ee344-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="ee344-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee344-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ee344-116">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ee344-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ee344-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="ee344-117">_lpulRet_</span></span>
  
> <span data-ttu-id="ee344-118">bota Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="ee344-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="ee344-119">TRUE para indicar que os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="ee344-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee344-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ee344-120">Return value</span></span>

<span data-ttu-id="ee344-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee344-121">S_OK</span></span> 
  
> <span data-ttu-id="ee344-122">Os identificadores de entrada foram comparados com êxito.</span><span class="sxs-lookup"><span data-stu-id="ee344-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="ee344-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ee344-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="ee344-124">Um ou ambos os identificadores de entrada não pertencem ao provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="ee344-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee344-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee344-125">Remarks</span></span>

<span data-ttu-id="ee344-126">Os provedores de catálogos de endereços implementam o método **CompareEntryIDs** para comparar dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="ee344-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="ee344-127">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido; tal situação pode ocorrer, por exemplo, quando você compara um identificador de entrada de curto prazo com um identificador de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="ee344-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="ee344-128">Para obter mais informações sobre como criar identificadores de entrada, confira identificadores de [entrada MAPI](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="ee344-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee344-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee344-129">See also</span></span>



[<span data-ttu-id="ee344-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee344-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

