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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766843"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="6e083-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6e083-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="6e083-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e083-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e083-105">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="6e083-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="6e083-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6e083-106">Parameters</span></span>

 <span data-ttu-id="6e083-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="6e083-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="6e083-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="6e083-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="6e083-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="6e083-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="6e083-110">[in] Um ponteiro para o primeiro identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="6e083-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="6e083-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="6e083-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="6e083-112">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="6e083-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="6e083-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="6e083-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="6e083-114">[in] Um ponteiro para o segundo identificador de entrada a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="6e083-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="6e083-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6e083-115">_ulFlags_</span></span>
  
> <span data-ttu-id="6e083-116">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6e083-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6e083-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="6e083-117">_lpulRet_</span></span>
  
> <span data-ttu-id="6e083-118">[out] Um ponteiro para o resultado da comparação.</span><span class="sxs-lookup"><span data-stu-id="6e083-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="6e083-119">TRUE para indicar que os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="6e083-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e083-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6e083-120">Return value</span></span>

<span data-ttu-id="6e083-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e083-121">S_OK</span></span> 
  
> <span data-ttu-id="6e083-122">Os identificadores de entrada foram comparados com êxito.</span><span class="sxs-lookup"><span data-stu-id="6e083-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="6e083-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6e083-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="6e083-124">O provedor de catálogo de endereços não fazem parte de um ou ambos os identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="6e083-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e083-125">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6e083-125">Remarks</span></span>

<span data-ttu-id="6e083-126">Provedores de catálogo de endereços implementam o método **CompareEntryIDs** para comparar os dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="6e083-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="6e083-127">**CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida; Essa situação pode ocorrer, por exemplo, quando você comparar um identificador curto prazo de entrada com um identificador de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="6e083-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="6e083-128">Para obter mais informações sobre como criar os identificadores de entrada, consulte [Identificadores de entrada de MAPI](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="6e083-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e083-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e083-129">See also</span></span>



[<span data-ttu-id="6e083-130">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e083-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

