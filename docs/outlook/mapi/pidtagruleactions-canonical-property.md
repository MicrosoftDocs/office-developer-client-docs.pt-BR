---
title: Propriedade canônica PidTagRuleActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleActions
api_type:
- COM
ms.assetid: 3ec4259a-8fe9-46c3-82b8-42c6907b8515
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ab246414f7caaf76f462d9b80e762fe614c77c21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390006"
---
# <a name="pidtagruleactions-canonical-property"></a><span data-ttu-id="3305a-103">Propriedade canônica PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="3305a-103">PidTagRuleActions Canonical Property</span></span>

  
  
<span data-ttu-id="3305a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3305a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3305a-105">Contém o conjunto de ações associadas à regra.</span><span class="sxs-lookup"><span data-stu-id="3305a-105">Contains the set of actions associated with the rule.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3305a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3305a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3305a-107">PR_RULE_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="3305a-107">PR_RULE_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="3305a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3305a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3305a-109">0x6680</span><span class="sxs-lookup"><span data-stu-id="3305a-109">0x6680</span></span>  <br/> |
|<span data-ttu-id="3305a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3305a-110">Data type:</span></span>  <br/> |<span data-ttu-id="3305a-111">PT_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="3305a-111">PT_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="3305a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3305a-112">Area:</span></span>  <br/> |<span data-ttu-id="3305a-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="3305a-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3305a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3305a-114">Remarks</span></span>

<span data-ttu-id="3305a-115">As ações são expressas como uma ação de regra e o buffer de valor de propriedade contém a estrutura do buffer de dados de ação regra empacotada conforme especificado na [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3305a-115">The actions are expressed as a rule action and the property value buffer contains the rule action data buffer structure packaged as specified in [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3305a-116">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3305a-116">MFCMAPI reference</span></span>

<span data-ttu-id="3305a-117">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3305a-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3305a-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="3305a-118">**File**</span></span>|<span data-ttu-id="3305a-119">**Função**</span><span class="sxs-lookup"><span data-stu-id="3305a-119">**Function**</span></span>|<span data-ttu-id="3305a-120">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="3305a-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3305a-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="3305a-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="3305a-122">PropCopyMore, HrCopyActions</span><span class="sxs-lookup"><span data-stu-id="3305a-122">PropCopyMore, HrCopyActions</span></span>  <br/> |<span data-ttu-id="3305a-123">Essas funções demonstram como analisar uma propriedade PT_ACTIONS para fins de cópia para outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="3305a-123">These functions demonstrate how to parse a PT_ACTIONS property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3305a-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3305a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3305a-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3305a-125">Protocol specifications</span></span>

<span data-ttu-id="3305a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3305a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3305a-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3305a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3305a-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3305a-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3305a-129">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="3305a-129">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3305a-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3305a-130">Header files</span></span>

<span data-ttu-id="3305a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3305a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="3305a-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3305a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="3305a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3305a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="3305a-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3305a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3305a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3305a-135">See also</span></span>



[<span data-ttu-id="3305a-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3305a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3305a-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3305a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3305a-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3305a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3305a-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3305a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

