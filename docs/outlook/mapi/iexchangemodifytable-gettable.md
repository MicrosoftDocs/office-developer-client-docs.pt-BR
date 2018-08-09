---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766934"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="2d03d-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="2d03d-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="2d03d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d03d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d03d-105">Retorna um ponteiro para uma interface para um objeto table MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d03d-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="2d03d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d03d-106">Parameters</span></span>

 <span data-ttu-id="2d03d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d03d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2d03d-108">[in] Reservado; deve ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2d03d-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="2d03d-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="2d03d-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="2d03d-110">Define o novos direitos.</span><span class="sxs-lookup"><span data-stu-id="2d03d-110">Sets new rights.</span></span>
    
<span data-ttu-id="2d03d-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="2d03d-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="2d03d-112">Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada das novas direitos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="2d03d-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="2d03d-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="2d03d-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="2d03d-114">Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição simple de novos direitos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="2d03d-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="2d03d-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="2d03d-115">_lppTable_</span></span>
  
> <span data-ttu-id="2d03d-116">[out] Aponta para um [IMAPITable: IUnknown](imapitableiunknown.md) interface que contém o objeto table.</span><span class="sxs-lookup"><span data-stu-id="2d03d-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2d03d-117">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2d03d-117">MFCMAPI reference</span></span>

<span data-ttu-id="2d03d-118">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d03d-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2d03d-119">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="2d03d-119">**File**</span></span>|<span data-ttu-id="2d03d-120">**Function**</span><span class="sxs-lookup"><span data-stu-id="2d03d-120">**Function**</span></span>|<span data-ttu-id="2d03d-121">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2d03d-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2d03d-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2d03d-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="2d03d-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="2d03d-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="2d03d-124">MFCMAPI usa o método **IExchangeModifyTable::GetTable** para obter uma tabela de regras.</span><span class="sxs-lookup"><span data-stu-id="2d03d-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d03d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d03d-125">See also</span></span>



[<span data-ttu-id="2d03d-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d03d-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="2d03d-127">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="2d03d-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

