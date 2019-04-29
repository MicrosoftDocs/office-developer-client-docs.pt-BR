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
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418173"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="ebe1d-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="ebe1d-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="ebe1d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebe1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebe1d-105">Atualiza um objeto de tabela MAPI.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="ebe1d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebe1d-106">Parameters</span></span>

 <span data-ttu-id="ebe1d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ebe1d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ebe1d-108">no Use um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ebe1d-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="ebe1d-109">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="ebe1d-109">0 (zero)</span></span>
  
> <span data-ttu-id="ebe1d-110">Use o valor do membro **ulRowFlags** da estrutura de [transentry](rowentry.md) .</span><span class="sxs-lookup"><span data-stu-id="ebe1d-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="ebe1d-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="ebe1d-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="ebe1d-112">Define novos direitos.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-112">Sets new rights.</span></span>
    
<span data-ttu-id="ebe1d-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="ebe1d-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="ebe1d-114">Quando o ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada dos novos direitos de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="ebe1d-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="ebe1d-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="ebe1d-116">Quando o ACLTABLE_FREEBUSY é passado, fornece uma exibição simples de novos direitos de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="ebe1d-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="ebe1d-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="ebe1d-118">Substitua todas as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="ebe1d-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="ebe1d-119">_lpMods_</span></span>
  
> <span data-ttu-id="ebe1d-120">no Aponta para a estrutura de uma [lista](rowlist.md) que contém as propriedades do objeto Table.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ebe1d-121">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ebe1d-121">MFCMAPI reference</span></span>

<span data-ttu-id="ebe1d-122">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ebe1d-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ebe1d-123">**File**</span></span>|<span data-ttu-id="ebe1d-124">**Função**</span><span class="sxs-lookup"><span data-stu-id="ebe1d-124">**Function**</span></span>|<span data-ttu-id="ebe1d-125">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ebe1d-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebe1d-126">RulesDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="ebe1d-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="ebe1d-127">CRulesDlg:: OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="ebe1d-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="ebe1d-128">MFCMAPI usa o método **IExchangeModifyTable:: modifytable** para gravar uma regra modificada novamente no índice de regras.</span><span class="sxs-lookup"><span data-stu-id="ebe1d-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebe1d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebe1d-129">See also</span></span>



[<span data-ttu-id="ebe1d-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebe1d-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="ebe1d-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="ebe1d-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="ebe1d-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="ebe1d-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="ebe1d-133">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ebe1d-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

