---
title: Propriedade canônica PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316335"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="b7df1-103">Propriedade canônica PidTagExtendedRuleMessageActions</span><span class="sxs-lookup"><span data-stu-id="b7df1-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="b7df1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7df1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7df1-105">Contém informações adicionais sobre as propriedades nomeadas usadas em uma mensagem de informações associadas à pasta (FAI).</span><span class="sxs-lookup"><span data-stu-id="b7df1-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7df1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b7df1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7df1-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="b7df1-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="b7df1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b7df1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7df1-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="b7df1-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="b7df1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b7df1-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7df1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b7df1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b7df1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b7df1-112">Area:</span></span>  <br/> |<span data-ttu-id="b7df1-113">Regras</span><span class="sxs-lookup"><span data-stu-id="b7df1-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7df1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7df1-114">Remarks</span></span>

<span data-ttu-id="b7df1-115">Essa propriedade deve ser definida em uma mensagem FAI.</span><span class="sxs-lookup"><span data-stu-id="b7df1-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="b7df1-116">Essa propriedade serve a mesma finalidade que **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), mas contém informações adicionais sobre a versão da regra e as propriedades nomeadas armazenadas na ação da regra, bem como informações sobre as ações a serem realizado por essa regra.</span><span class="sxs-lookup"><span data-stu-id="b7df1-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="b7df1-117">Todos os valores de cadeia de caracteres contidos em qualquer parte do buffer de ação usado para conter ações devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b7df1-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="b7df1-118">Para obter informações sobre o formato dessa propriedade binária, consulte [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b7df1-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7df1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7df1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7df1-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="b7df1-120">Protocol specifications</span></span>

<span data-ttu-id="b7df1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7df1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7df1-122">Fornece referências a especificações de protocolo do Exchange Server relacionadas..</span><span class="sxs-lookup"><span data-stu-id="b7df1-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="b7df1-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7df1-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7df1-124">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="b7df1-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7df1-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b7df1-125">Header files</span></span>

<span data-ttu-id="b7df1-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b7df1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7df1-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b7df1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7df1-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b7df1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b7df1-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b7df1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7df1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7df1-130">See also</span></span>



[<span data-ttu-id="b7df1-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b7df1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7df1-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b7df1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7df1-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b7df1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7df1-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b7df1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

