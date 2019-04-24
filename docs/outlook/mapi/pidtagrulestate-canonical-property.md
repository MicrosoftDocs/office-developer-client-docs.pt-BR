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
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="93fb5-103">Propriedade canônica PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="93fb5-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="93fb5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93fb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93fb5-105">Um valor interpretado como uma combinação de bitmask de sinalizadores que especificam o estado da regra.</span><span class="sxs-lookup"><span data-stu-id="93fb5-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93fb5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="93fb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93fb5-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="93fb5-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="93fb5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="93fb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93fb5-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="93fb5-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="93fb5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="93fb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="93fb5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="93fb5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="93fb5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="93fb5-112">Area:</span></span>  <br/> |<span data-ttu-id="93fb5-113">Regras no servidor</span><span class="sxs-lookup"><span data-stu-id="93fb5-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93fb5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="93fb5-114">Remarks</span></span>

<span data-ttu-id="93fb5-115">A tabela a seguir define os valores possíveis dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="93fb5-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="93fb5-116">EN (ST_ENABLED, bitmask 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="93fb5-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="93fb5-117">A regra está habilitada para execução.</span><span class="sxs-lookup"><span data-stu-id="93fb5-117">The rule is enabled for execution.</span></span> <span data-ttu-id="93fb5-118">Se esse sinalizador não for definido, o servidor deverá ignorar essa regra ao avaliar as regras.</span><span class="sxs-lookup"><span data-stu-id="93fb5-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="93fb5-119">ER (ST_ERROR, bitmask 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="93fb5-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="93fb5-120">O servidor encontrou um erro ao processar a regra.</span><span class="sxs-lookup"><span data-stu-id="93fb5-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="93fb5-121">DE (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="93fb5-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="93fb5-122">A regra é executada somente quando o usuário define o estado de ausência temporária (OOF) na caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="93fb5-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="93fb5-123">Este sinalizador não deve ser definido em uma regra de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="93fb5-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="93fb5-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="93fb5-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="93fb5-125">Este sinalizador não deve ser definido em uma regra de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="93fb5-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="93fb5-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="93fb5-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="93fb5-127">A avaliação da regra será finalizada após a execução dessa regra, exceto a avaliação de regras de ausência temporária.</span><span class="sxs-lookup"><span data-stu-id="93fb5-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="93fb5-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="93fb5-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="93fb5-129">A avaliação dessa regra pode ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="93fb5-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="93fb5-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="93fb5-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="93fb5-131">O servidor encontrou um erro ao analisar os dados da regra fornecidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="93fb5-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="93fb5-132">X</span><span class="sxs-lookup"><span data-stu-id="93fb5-132">X</span></span>
  
> <span data-ttu-id="93fb5-133">Não usado por este protocolo.</span><span class="sxs-lookup"><span data-stu-id="93fb5-133">Unused by this protocol.</span></span> <span data-ttu-id="93fb5-134">Este bit não deve ser modificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="93fb5-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="93fb5-135">Observe a interação entre os sinalizadores ST_ONLY_WHEN_OOF e ST_EXIT_LEVEL:</span><span class="sxs-lookup"><span data-stu-id="93fb5-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="93fb5-136">Quando o estado "fora do escritório" é definido na caixa de correio e uma condição de regra é avaliada como TRUE,</span><span class="sxs-lookup"><span data-stu-id="93fb5-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="93fb5-137">E</span><span class="sxs-lookup"><span data-stu-id="93fb5-137">AND:</span></span>
  
- <span data-ttu-id="93fb5-138">A regra tem o sinalizador ST_EXIT_LEVEL definido e não tem o sinalizador ST_ONLY_WHEN_OOF definido.</span><span class="sxs-lookup"><span data-stu-id="93fb5-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="93fb5-139">Em seguida, o servidor não deve avaliar as regras subsequentes que não têm o sinalizador ST_ONLY_WHEN_OOF definido e deve avaliar as regras subsequentes que têm o sinalizador ST_ONLY_WHEN_OOF definido.</span><span class="sxs-lookup"><span data-stu-id="93fb5-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="93fb5-140">OU</span><span class="sxs-lookup"><span data-stu-id="93fb5-140">OR:</span></span>
  
- <span data-ttu-id="93fb5-141">A regra tem os sinalizadores ST_EXIT_LEVEL e ST_ONLY_WHEN_OOF definidos.</span><span class="sxs-lookup"><span data-stu-id="93fb5-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="93fb5-142">Em seguida, o servidor não deve avaliar nenhuma regra subsequente.</span><span class="sxs-lookup"><span data-stu-id="93fb5-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="93fb5-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="93fb5-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93fb5-144">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="93fb5-144">Protocol specifications</span></span>

<span data-ttu-id="93fb5-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93fb5-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93fb5-146">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="93fb5-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93fb5-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93fb5-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93fb5-148">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="93fb5-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93fb5-149">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="93fb5-149">Header files</span></span>

<span data-ttu-id="93fb5-150">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="93fb5-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="93fb5-151">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="93fb5-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="93fb5-152">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="93fb5-152">Mapitags.h</span></span>
  
> <span data-ttu-id="93fb5-153">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="93fb5-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93fb5-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="93fb5-154">See also</span></span>



[<span data-ttu-id="93fb5-155">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="93fb5-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93fb5-156">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="93fb5-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93fb5-157">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="93fb5-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93fb5-158">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="93fb5-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

