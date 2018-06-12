---
title: Propriedade canônico de PidTagRuleCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleCondition
api_type:
- COM
ms.assetid: 8a11e846-c62f-4c06-876f-94623d50cc3b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: f4eae388d51b0428d508a675681fa4cd1d94e46f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769897"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="a84d1-103">Propriedade canônico de PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="a84d1-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="a84d1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a84d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a84d1-105">A condição usada ao avaliar a regra.</span><span class="sxs-lookup"><span data-stu-id="a84d1-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a84d1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a84d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a84d1-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="a84d1-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="a84d1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a84d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a84d1-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="a84d1-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="a84d1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a84d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="a84d1-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="a84d1-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="a84d1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a84d1-112">Area:</span></span>  <br/> |<span data-ttu-id="a84d1-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="a84d1-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a84d1-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a84d1-114">Remarks</span></span>

<span data-ttu-id="a84d1-115">A condição é expressa como uma **restrição** e buffer **PropertyValue** contém a estrutura de **restrição** empacotada conforme especificado na [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a84d1-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a84d1-116">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a84d1-116">MFCMAPI reference</span></span>

<span data-ttu-id="a84d1-117">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a84d1-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a84d1-118">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a84d1-118">**File**</span></span>|<span data-ttu-id="a84d1-119">**Function**</span><span class="sxs-lookup"><span data-stu-id="a84d1-119">**Function**</span></span>|<span data-ttu-id="a84d1-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a84d1-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a84d1-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="a84d1-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="a84d1-122">PropCopyMore, HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="a84d1-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="a84d1-123">Essas funções demonstram como analisar uma propriedade **PT_SRESTRICTION** para fins de cópia para outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="a84d1-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a84d1-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a84d1-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a84d1-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a84d1-125">Protocol specifications</span></span>

<span data-ttu-id="a84d1-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a84d1-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a84d1-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a84d1-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a84d1-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a84d1-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a84d1-129">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="a84d1-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="a84d1-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a84d1-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a84d1-131">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="a84d1-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a84d1-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a84d1-132">Header files</span></span>

<span data-ttu-id="a84d1-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a84d1-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a84d1-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a84d1-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="a84d1-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a84d1-135">Mapitags.h</span></span>
  
> <span data-ttu-id="a84d1-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a84d1-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a84d1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a84d1-137">See also</span></span>



[<span data-ttu-id="a84d1-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a84d1-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a84d1-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a84d1-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a84d1-140">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a84d1-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a84d1-141">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="a84d1-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

