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
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436241"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="b9b8f-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="b9b8f-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="b9b8f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9b8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9b8f-105">Retorna um ponteiro para uma interface para um objeto de tabela MAPI.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="b9b8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9b8f-106">Parameters</span></span>

 <span data-ttu-id="b9b8f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9b8f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b9b8f-108">[in] Reservado; deve ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b9b8f-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="b9b8f-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="b9b8f-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="b9b8f-110">Define novos direitos.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-110">Sets new rights.</span></span>
    
<span data-ttu-id="b9b8f-111">freeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="b9b8f-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="b9b8f-112">Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada dos novos direitos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="b9b8f-113">freeBusySimple</span><span class="sxs-lookup"><span data-stu-id="b9b8f-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="b9b8f-114">Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição simples de novos direitos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="b9b8f-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="b9b8f-115">_lppTable_</span></span>
  
> <span data-ttu-id="b9b8f-116">[out] Aponta para [uma IMAPITable : interface IUnknown](imapitableiunknown.md) que contém o objeto table.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="b9b8f-117">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b9b8f-117">MFCMAPI reference</span></span>

<span data-ttu-id="b9b8f-118">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b9b8f-119">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b9b8f-119">**File**</span></span>|<span data-ttu-id="b9b8f-120">**Função**</span><span class="sxs-lookup"><span data-stu-id="b9b8f-120">**Function**</span></span>|<span data-ttu-id="b9b8f-121">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b9b8f-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b9b8f-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b9b8f-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="b9b8f-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="b9b8f-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="b9b8f-124">MFCMAPI usa o **método IExchangeModifyTable::GetTable** para obter uma tabela de regras.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9b8f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9b8f-125">See also</span></span>



[<span data-ttu-id="b9b8f-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9b8f-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="b9b8f-127">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b9b8f-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

