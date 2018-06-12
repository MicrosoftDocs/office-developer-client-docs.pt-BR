---
title: Propriedade canônico de PidTagRuleId
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769895"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="6166f-103">Propriedade canônico de PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="6166f-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="6166f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6166f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6166f-105">Especifica um identificador exclusivo que do servidor de mensagens gera para cada regra quando a regra é criada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="6166f-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6166f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6166f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6166f-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="6166f-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="6166f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6166f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6166f-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="6166f-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="6166f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6166f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6166f-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="6166f-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="6166f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6166f-112">Area:</span></span>  <br/> |<span data-ttu-id="6166f-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="6166f-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6166f-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6166f-114">Remarks</span></span>

<span data-ttu-id="6166f-115">O cliente não deve especificar essa propriedade ao criar uma nova regra, mas deve especificá-lo quando modificar ou excluir uma regra.</span><span class="sxs-lookup"><span data-stu-id="6166f-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="6166f-116">Ao excluir uma regra, a única propriedade que o cliente deve passar é **PR_RULE_ID** e não deve passar em qualquer outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="6166f-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="6166f-117">O servidor deve ignorar propriedades que não seja essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6166f-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="6166f-118">Ao adicionar uma regra, o cliente não deve passar em **PR_RULE_ID**, ele deve passar na **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) e **PR_RULE_PROVIDER** ([ PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) propriedades.</span><span class="sxs-lookup"><span data-stu-id="6166f-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="6166f-119">Ao modificar uma regra, o cliente deve passar no **PR_RULE_ID** e deve passar o restante das propriedades que precisam ser modificados.</span><span class="sxs-lookup"><span data-stu-id="6166f-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6166f-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6166f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6166f-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6166f-121">Protocol specifications</span></span>

<span data-ttu-id="6166f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6166f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6166f-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6166f-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6166f-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6166f-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6166f-125">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="6166f-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6166f-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6166f-126">Header files</span></span>

<span data-ttu-id="6166f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6166f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6166f-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6166f-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6166f-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6166f-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6166f-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6166f-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6166f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6166f-131">See also</span></span>



[<span data-ttu-id="6166f-132">Propriedade canônico de PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="6166f-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="6166f-133">Propriedade canônico de PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="6166f-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="6166f-134">Propriedade canônico de PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="6166f-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="6166f-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6166f-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6166f-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6166f-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6166f-137">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6166f-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6166f-138">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="6166f-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

