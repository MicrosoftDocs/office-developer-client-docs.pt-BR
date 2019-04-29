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
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="e8fb0-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="e8fb0-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="e8fb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8fb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8fb0-105">Retorna um ponteiro para uma interface de um objeto MAPI da tabela.</span><span class="sxs-lookup"><span data-stu-id="e8fb0-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="e8fb0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8fb0-106">Parameters</span></span>

 <span data-ttu-id="e8fb0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8fb0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e8fb0-108">no Serve deve ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e8fb0-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="e8fb0-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="e8fb0-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="e8fb0-110">Define novos direitos.</span><span class="sxs-lookup"><span data-stu-id="e8fb0-110">Sets new rights.</span></span>
    
<span data-ttu-id="e8fb0-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="e8fb0-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="e8fb0-112">Quando o ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada dos novos direitos de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e8fb0-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="e8fb0-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="e8fb0-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="e8fb0-114">Quando o ACLTABLE_FREEBUSY é passado, fornece uma exibição simples de novos direitos de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e8fb0-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="e8fb0-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e8fb0-115">_lppTable_</span></span>
  
> <span data-ttu-id="e8fb0-116">bota Aponta para uma interface imApitable [: IUnknown](imapitableiunknown.md) contendo o objeto Table.</span><span class="sxs-lookup"><span data-stu-id="e8fb0-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e8fb0-117">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e8fb0-117">MFCMAPI reference</span></span>

<span data-ttu-id="e8fb0-118">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8fb0-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e8fb0-119">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e8fb0-119">**File**</span></span>|<span data-ttu-id="e8fb0-120">**Função**</span><span class="sxs-lookup"><span data-stu-id="e8fb0-120">**Function**</span></span>|<span data-ttu-id="e8fb0-121">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e8fb0-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8fb0-122">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="e8fb0-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="e8fb0-123">CRulesDlg:: OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="e8fb0-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="e8fb0-124">MFCMAPI usa o método **IExchangeModifyTable:: GetTable** para obter uma tabela de regras.</span><span class="sxs-lookup"><span data-stu-id="e8fb0-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8fb0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8fb0-125">See also</span></span>



[<span data-ttu-id="e8fb0-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8fb0-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="e8fb0-127">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e8fb0-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

