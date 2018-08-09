---
title: Propriedade canônica PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769895"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="ecfd7-103">Propriedade canônica PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="ecfd7-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="ecfd7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecfd7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecfd7-105">Especifica um identificador exclusivo que do servidor de mensagens gera para cada regra quando a regra é criada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecfd7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ecfd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecfd7-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="ecfd7-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="ecfd7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ecfd7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecfd7-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="ecfd7-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="ecfd7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ecfd7-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecfd7-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="ecfd7-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="ecfd7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ecfd7-112">Area:</span></span>  <br/> |<span data-ttu-id="ecfd7-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="ecfd7-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecfd7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecfd7-114">Remarks</span></span>

<span data-ttu-id="ecfd7-115">O cliente não deve especificar essa propriedade ao criar uma nova regra, mas deve especificá-lo quando modificar ou excluir uma regra.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="ecfd7-116">Ao excluir uma regra, a única propriedade que o cliente deve passar é **PR_RULE_ID** e não deve passar em qualquer outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="ecfd7-117">O servidor deve ignorar propriedades que não seja essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="ecfd7-118">Ao adicionar uma regra, o cliente não deve passar em **PR_RULE_ID**, ele deve passar na **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) e **PR_RULE_PROVIDER** ([ PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) propriedades.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="ecfd7-119">Ao modificar uma regra, o cliente deve passar no **PR_RULE_ID** e deve passar o restante das propriedades que precisam ser modificados.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ecfd7-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecfd7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecfd7-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ecfd7-121">Protocol specifications</span></span>

<span data-ttu-id="ecfd7-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecfd7-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecfd7-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecfd7-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecfd7-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecfd7-125">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecfd7-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ecfd7-126">Header files</span></span>

<span data-ttu-id="ecfd7-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecfd7-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecfd7-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecfd7-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecfd7-129">Mapitags.h</span></span>
  
> <span data-ttu-id="ecfd7-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ecfd7-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecfd7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecfd7-131">See also</span></span>



[<span data-ttu-id="ecfd7-132">Propriedade canônica PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ecfd7-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="ecfd7-133">Propriedade canônica PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="ecfd7-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="ecfd7-134">Propriedade canônica PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="ecfd7-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="ecfd7-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ecfd7-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecfd7-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ecfd7-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecfd7-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ecfd7-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecfd7-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ecfd7-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

