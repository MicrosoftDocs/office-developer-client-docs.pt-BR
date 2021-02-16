---
title: Propriedade canônica PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338609"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="07ec6-103">Propriedade canônica PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="07ec6-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="07ec6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07ec6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07ec6-105">Um valor interpretado como uma combinação de bitmask de sinalizadores que especificam o estado da regra.</span><span class="sxs-lookup"><span data-stu-id="07ec6-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07ec6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="07ec6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07ec6-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="07ec6-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="07ec6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="07ec6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07ec6-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="07ec6-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="07ec6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="07ec6-110">Data type:</span></span>  <br/> |<span data-ttu-id="07ec6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="07ec6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="07ec6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="07ec6-112">Area:</span></span>  <br/> |<span data-ttu-id="07ec6-113">Regras do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="07ec6-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07ec6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="07ec6-114">Remarks</span></span>

<span data-ttu-id="07ec6-115">A tabela a seguir define os valores possíveis dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="07ec6-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="07ec6-116">EN (ST_ENABLED, bitmask 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="07ec6-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="07ec6-117">A regra está habilitada para execução.</span><span class="sxs-lookup"><span data-stu-id="07ec6-117">The rule is enabled for execution.</span></span> <span data-ttu-id="07ec6-118">Se esse sinalizador não estiver definido, o servidor deverá ignorar essa regra ao avaliar as regras.</span><span class="sxs-lookup"><span data-stu-id="07ec6-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="07ec6-119">ER (ST_ERROR, máscara de 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="07ec6-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="07ec6-120">O servidor encontrou um erro ao processar a regra.</span><span class="sxs-lookup"><span data-stu-id="07ec6-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="07ec6-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="07ec6-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="07ec6-122">A regra é executada somente quando o usuário define o estado de Fora do Escritório (OOF) na caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="07ec6-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="07ec6-123">Esse sinalizador não deve ser definido em uma regra de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="07ec6-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="07ec6-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="07ec6-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="07ec6-125">Esse sinalizador não deve ser definido em uma regra de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="07ec6-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="07ec6-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="07ec6-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="07ec6-127">A avaliação de regra terminará após a execução dessa regra, exceto para a avaliação das regras de Desem posse.</span><span class="sxs-lookup"><span data-stu-id="07ec6-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="07ec6-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="07ec6-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="07ec6-129">A avaliação dessa regra pode ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="07ec6-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="07ec6-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="07ec6-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="07ec6-131">O servidor encontrou um erro ao analisar os dados de regra fornecidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="07ec6-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="07ec6-132">X</span><span class="sxs-lookup"><span data-stu-id="07ec6-132">X</span></span>
  
> <span data-ttu-id="07ec6-133">Não éusado por este protocolo.</span><span class="sxs-lookup"><span data-stu-id="07ec6-133">Unused by this protocol.</span></span> <span data-ttu-id="07ec6-134">Este bit não deve ser modificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="07ec6-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="07ec6-135">Observação sobre a interação entre ST_ONLY_WHEN_OOF e ST_EXIT_LEVEL sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="07ec6-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="07ec6-136">Quando o estado "Fora do Escritório" é definido na caixa de correio e uma condição de regra é avaliada como VERDADEIRO,</span><span class="sxs-lookup"><span data-stu-id="07ec6-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="07ec6-137">E:</span><span class="sxs-lookup"><span data-stu-id="07ec6-137">AND:</span></span>
  
- <span data-ttu-id="07ec6-138">A regra tem o ST_EXIT_LEVEL sinalizador definido e não tem ST_ONLY_WHEN_OOF sinalizador definido.</span><span class="sxs-lookup"><span data-stu-id="07ec6-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="07ec6-139">Em seguida, o servidor não deve avaliar as regras subsequentes que não têm um sinalizador ST_ONLY_WHEN_OOF definido e deve avaliar as regras subsequentes que ST_ONLY_WHEN_OOF sinalizador definido.</span><span class="sxs-lookup"><span data-stu-id="07ec6-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="07ec6-140">OU:</span><span class="sxs-lookup"><span data-stu-id="07ec6-140">OR:</span></span>
  
- <span data-ttu-id="07ec6-141">A regra tem os sinalizadores ST_EXIT_LEVEL e ST_ONLY_WHEN_OOF definidos.</span><span class="sxs-lookup"><span data-stu-id="07ec6-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="07ec6-142">Em seguida, o servidor não deve avaliar as regras subsequentes.</span><span class="sxs-lookup"><span data-stu-id="07ec6-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="07ec6-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="07ec6-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07ec6-144">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="07ec6-144">Protocol specifications</span></span>

<span data-ttu-id="07ec6-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07ec6-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07ec6-146">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="07ec6-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07ec6-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07ec6-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07ec6-148">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="07ec6-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07ec6-149">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="07ec6-149">Header files</span></span>

<span data-ttu-id="07ec6-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07ec6-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="07ec6-151">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="07ec6-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="07ec6-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="07ec6-152">Mapitags.h</span></span>
  
> <span data-ttu-id="07ec6-153">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="07ec6-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07ec6-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="07ec6-154">See also</span></span>



[<span data-ttu-id="07ec6-155">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="07ec6-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07ec6-156">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="07ec6-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07ec6-157">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="07ec6-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07ec6-158">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="07ec6-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

