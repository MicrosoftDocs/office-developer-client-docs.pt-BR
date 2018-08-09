---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766922"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="3b98c-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="3b98c-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="3b98c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b98c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b98c-105">Atualiza um objeto table MAPI.</span><span class="sxs-lookup"><span data-stu-id="3b98c-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="3b98c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b98c-106">Parameters</span></span>

 <span data-ttu-id="3b98c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3b98c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3b98c-108">[in] Use um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3b98c-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="3b98c-109">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="3b98c-109">0 (zero)</span></span>
  
> <span data-ttu-id="3b98c-110">Use o valor do membro **ulRowFlags** da estrutura [ROWENTRY](rowentry.md) .</span><span class="sxs-lookup"><span data-stu-id="3b98c-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="3b98c-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="3b98c-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="3b98c-112">Define o novos direitos.</span><span class="sxs-lookup"><span data-stu-id="3b98c-112">Sets new rights.</span></span>
    
<span data-ttu-id="3b98c-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="3b98c-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="3b98c-114">Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada das novas direitos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="3b98c-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="3b98c-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="3b98c-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="3b98c-116">Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição simple de novos direitos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="3b98c-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="3b98c-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="3b98c-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="3b98c-118">Substitua todas as linhas na tabela.</span><span class="sxs-lookup"><span data-stu-id="3b98c-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="3b98c-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="3b98c-119">_lpMods_</span></span>
  
> <span data-ttu-id="3b98c-120">[in] Aponta para uma estrutura [ROWLIST](rowlist.md) que contém as propriedades para o objeto table.</span><span class="sxs-lookup"><span data-stu-id="3b98c-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b98c-121">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3b98c-121">MFCMAPI reference</span></span>

<span data-ttu-id="3b98c-122">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b98c-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b98c-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="3b98c-123">**File**</span></span>|<span data-ttu-id="3b98c-124">**Function**</span><span class="sxs-lookup"><span data-stu-id="3b98c-124">**Function**</span></span>|<span data-ttu-id="3b98c-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3b98c-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b98c-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3b98c-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="3b98c-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="3b98c-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="3b98c-128">MFCMAPI usa o método **IExchangeModifyTable::ModifyTable** para gravar uma regra modificada de volta à tabela de regras.</span><span class="sxs-lookup"><span data-stu-id="3b98c-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b98c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b98c-129">See also</span></span>



[<span data-ttu-id="3b98c-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b98c-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="3b98c-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="3b98c-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="3b98c-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="3b98c-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="3b98c-133">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="3b98c-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

