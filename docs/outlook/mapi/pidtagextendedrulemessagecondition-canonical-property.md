---
title: Propriedade canônica PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316328"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="0ea9b-103">Propriedade canônica PidTagExtendedRuleMessageCondition</span><span class="sxs-lookup"><span data-stu-id="0ea9b-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="0ea9b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ea9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ea9b-105">Contém informações sobre quaisquer propriedades nomeadas que estão contidas dentro de condições de regra estendida.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ea9b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0ea9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ea9b-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="0ea9b-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="0ea9b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0ea9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ea9b-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="0ea9b-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="0ea9b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0ea9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ea9b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ea9b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0ea9b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0ea9b-112">Area:</span></span>  <br/> |<span data-ttu-id="0ea9b-113">Rules</span><span class="sxs-lookup"><span data-stu-id="0ea9b-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ea9b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ea9b-114">Remarks</span></span>

<span data-ttu-id="0ea9b-115">Essa propriedade deve ser definida em uma mensagem FAI.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="0ea9b-116">Ele serve à mesma finalidade que **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), mas contém informações adicionais sobre as propriedades nomeadas usadas.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="0ea9b-117">Todos os valores de cadeia de caracteres contidos em qualquer parte desse valor de propriedade de condição devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="0ea9b-118">Para obter informações sobre o formato dessa propriedade binária, consulte [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0ea9b-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0ea9b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ea9b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ea9b-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0ea9b-120">Protocol specifications</span></span>

<span data-ttu-id="0ea9b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea9b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ea9b-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ea9b-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ea9b-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ea9b-124">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ea9b-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="0ea9b-125">Header files</span></span>

<span data-ttu-id="0ea9b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ea9b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ea9b-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ea9b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ea9b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0ea9b-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0ea9b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ea9b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ea9b-130">See also</span></span>



[<span data-ttu-id="0ea9b-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea9b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ea9b-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea9b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ea9b-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0ea9b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ea9b-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0ea9b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

