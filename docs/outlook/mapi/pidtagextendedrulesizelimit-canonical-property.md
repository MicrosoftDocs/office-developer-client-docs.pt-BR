---
title: Propriedade canônica PidTagExtendedRuleSizeLimit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 347d84021b7e9ece925acb99e8b539ba608337a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316342"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="aadc9-103">Propriedade canônica PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="aadc9-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="aadc9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aadc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aadc9-105">Contém o tamanho máximo, em bytes, que o usuário pode acumular para uma única regra "estendida".</span><span class="sxs-lookup"><span data-stu-id="aadc9-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aadc9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="aadc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aadc9-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="aadc9-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="aadc9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="aadc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aadc9-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="aadc9-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="aadc9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="aadc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="aadc9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aadc9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aadc9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="aadc9-112">Area:</span></span>  <br/> |<span data-ttu-id="aadc9-113">Rules</span><span class="sxs-lookup"><span data-stu-id="aadc9-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aadc9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aadc9-114">Remarks</span></span>

<span data-ttu-id="aadc9-115">Se essa propriedade for definida no objeto de logon, o cliente deverá manter o tamanho da propriedade **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) sob o valor especificado por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="aadc9-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="aadc9-116">Por outro lado, o servidor deve retornar um erro se o cliente tentar definir uma propriedade binária muito grande.</span><span class="sxs-lookup"><span data-stu-id="aadc9-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="aadc9-117">Para obter informações sobre regras estendidas, consulte [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aadc9-117">For information about extended rules, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aadc9-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="aadc9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aadc9-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="aadc9-119">Protocol specifications</span></span>

<span data-ttu-id="aadc9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="aadc9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aadc9-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aadc9-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aadc9-123">Especifica operações permitidas para os objetos principais do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="aadc9-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aadc9-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="aadc9-124">Header files</span></span>

<span data-ttu-id="aadc9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aadc9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="aadc9-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="aadc9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="aadc9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aadc9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="aadc9-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="aadc9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aadc9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="aadc9-129">See also</span></span>



[<span data-ttu-id="aadc9-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="aadc9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aadc9-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="aadc9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aadc9-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="aadc9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aadc9-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="aadc9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

