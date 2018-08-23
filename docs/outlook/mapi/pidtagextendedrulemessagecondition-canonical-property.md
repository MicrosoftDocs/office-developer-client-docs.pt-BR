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
ms.openlocfilehash: 92008a387bb0130207af012df209a3aa6881d40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593169"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="1cec1-103">Propriedade canônica PidTagExtendedRuleMessageCondition</span><span class="sxs-lookup"><span data-stu-id="1cec1-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="1cec1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cec1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cec1-105">Contém informações sobre todas as propriedades nomeadas que está contido dentro de condições de regra estendido.</span><span class="sxs-lookup"><span data-stu-id="1cec1-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cec1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1cec1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cec1-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="1cec1-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="1cec1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1cec1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cec1-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="1cec1-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="1cec1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1cec1-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cec1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1cec1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1cec1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1cec1-112">Area:</span></span>  <br/> |<span data-ttu-id="1cec1-113">Rules</span><span class="sxs-lookup"><span data-stu-id="1cec1-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cec1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cec1-114">Remarks</span></span>

<span data-ttu-id="1cec1-115">Esta propriedade deve ser definida em uma mensagem FAI.</span><span class="sxs-lookup"><span data-stu-id="1cec1-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="1cec1-116">Ele tem a mesma finalidade como **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), mas contém informações adicionais sobre as propriedades nomeadas usado.</span><span class="sxs-lookup"><span data-stu-id="1cec1-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="1cec1-117">Todos os valores de cadeia de caracteres contidos em qualquer parte desse valor de propriedade de condição devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1cec1-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="1cec1-118">Para obter informações sobre o formato dessa propriedade binários, consulte [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1cec1-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1cec1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cec1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cec1-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1cec1-120">Protocol specifications</span></span>

<span data-ttu-id="1cec1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cec1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cec1-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1cec1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cec1-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cec1-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cec1-124">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="1cec1-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cec1-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1cec1-125">Header files</span></span>

<span data-ttu-id="1cec1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cec1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cec1-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1cec1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cec1-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1cec1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1cec1-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1cec1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cec1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cec1-130">See also</span></span>



[<span data-ttu-id="1cec1-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1cec1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cec1-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1cec1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cec1-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1cec1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cec1-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1cec1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

