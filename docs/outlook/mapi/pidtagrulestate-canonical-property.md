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
ms.openlocfilehash: 519ee2b91275e4253845afa35a9a80470071966d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769920"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="08ec2-103">Propriedade canônica PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="08ec2-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="08ec2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08ec2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08ec2-105">Um valor interpretado como uma combinação de bitmask de sinalizadores que especificam o estado da regra.</span><span class="sxs-lookup"><span data-stu-id="08ec2-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08ec2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="08ec2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08ec2-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="08ec2-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="08ec2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="08ec2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08ec2-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="08ec2-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="08ec2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="08ec2-110">Data type:</span></span>  <br/> |<span data-ttu-id="08ec2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="08ec2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="08ec2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="08ec2-112">Area:</span></span>  <br/> |<span data-ttu-id="08ec2-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="08ec2-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08ec2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="08ec2-114">Remarks</span></span>

<span data-ttu-id="08ec2-115">A tabela a seguir define os possíveis valores dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="08ec2-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="08ec2-116">EN (ST_ENABLED, bitmask 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="08ec2-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="08ec2-117">A regra está habilitada para execução.</span><span class="sxs-lookup"><span data-stu-id="08ec2-117">The rule is enabled for execution.</span></span> <span data-ttu-id="08ec2-118">Se esse sinalizador não estiver definida, o servidor deve pular esta regra ao avaliar regras.</span><span class="sxs-lookup"><span data-stu-id="08ec2-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="08ec2-119">ER (ST_ERROR, bitmask 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="08ec2-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="08ec2-120">O servidor encontrou um erro ao processar a regra.</span><span class="sxs-lookup"><span data-stu-id="08ec2-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="08ec2-121">DE bitmask 0x00000004 (ST_ONLY_WHEN_OOF)</span><span class="sxs-lookup"><span data-stu-id="08ec2-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="08ec2-122">A regra é executada somente quando o usuário define o estado de fora do escritório (OOF) na caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="08ec2-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="08ec2-123">Esse sinalizador não deve ser definida em uma regra de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="08ec2-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="08ec2-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="08ec2-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="08ec2-125">Esse sinalizador não deve ser definida em uma regra de pasta pública.</span><span class="sxs-lookup"><span data-stu-id="08ec2-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="08ec2-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="08ec2-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="08ec2-127">Avaliação de regra será finalizado depois de executar essa regra, exceto para a avaliação das regras de ausência temporária.</span><span class="sxs-lookup"><span data-stu-id="08ec2-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="08ec2-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="08ec2-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="08ec2-129">Avaliação desta regra poderão ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="08ec2-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="08ec2-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="08ec2-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="08ec2-131">O servidor encontrou um erro ao analisar os dados da regra fornecidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="08ec2-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="08ec2-132">X</span><span class="sxs-lookup"><span data-stu-id="08ec2-132">X</span></span>
  
> <span data-ttu-id="08ec2-133">Não usada por esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="08ec2-133">Unused by this protocol.</span></span> <span data-ttu-id="08ec2-134">Esse bit não deve ser modificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="08ec2-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="08ec2-135">Nota sobre a interação entre ST_ONLY_WHEN_OOF e ST_EXIT_LEVEL sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="08ec2-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="08ec2-136">Quando o estado de "ausência temporária" é definido na caixa de correio e uma condição de regra é avaliada como TRUE,</span><span class="sxs-lookup"><span data-stu-id="08ec2-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="08ec2-137">E:</span><span class="sxs-lookup"><span data-stu-id="08ec2-137">AND:</span></span>
  
- <span data-ttu-id="08ec2-138">A regra tem o sinalizador ST_EXIT_LEVEL definido e não tem sinalizador ST_ONLY_WHEN_OOF definido.</span><span class="sxs-lookup"><span data-stu-id="08ec2-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="08ec2-139">Em seguida, o servidor não deve resultar em regras subsequentes que não tenham ST_ONLY_WHEN_OOF sinalizador será definido e deve ser avaliada regras subsequentes que possuem o sinalizador ST_ONLY_WHEN_OOF definido.</span><span class="sxs-lookup"><span data-stu-id="08ec2-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="08ec2-140">OR:</span><span class="sxs-lookup"><span data-stu-id="08ec2-140">OR:</span></span>
  
- <span data-ttu-id="08ec2-141">A regra tem os ST_EXIT_LEVEL ST_ONLY_WHEN_OOF sinalizadores e definir.</span><span class="sxs-lookup"><span data-stu-id="08ec2-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="08ec2-142">Em seguida, o servidor não deve resultar em quaisquer regras subsequentes.</span><span class="sxs-lookup"><span data-stu-id="08ec2-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="08ec2-143">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="08ec2-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08ec2-144">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="08ec2-144">Protocol specifications</span></span>

<span data-ttu-id="08ec2-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08ec2-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08ec2-146">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="08ec2-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08ec2-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08ec2-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08ec2-148">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="08ec2-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08ec2-149">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="08ec2-149">Header files</span></span>

<span data-ttu-id="08ec2-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08ec2-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="08ec2-151">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="08ec2-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="08ec2-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08ec2-152">Mapitags.h</span></span>
  
> <span data-ttu-id="08ec2-153">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="08ec2-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08ec2-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="08ec2-154">See also</span></span>



[<span data-ttu-id="08ec2-155">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="08ec2-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08ec2-156">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="08ec2-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08ec2-157">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="08ec2-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08ec2-158">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="08ec2-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

