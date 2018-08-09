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
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769234"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="4cd4c-103">Propriedade canônica PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="4cd4c-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="4cd4c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4cd4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4cd4c-105">Contém o tamanho máximo, em bytes, o usuário tem permissão para acumular para uma única regra "estendida".</span><span class="sxs-lookup"><span data-stu-id="4cd4c-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cd4c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4cd4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cd4c-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="4cd4c-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="4cd4c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4cd4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4cd4c-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="4cd4c-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="4cd4c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4cd4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4cd4c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4cd4c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4cd4c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4cd4c-112">Area:</span></span>  <br/> |<span data-ttu-id="4cd4c-113">Rules</span><span class="sxs-lookup"><span data-stu-id="4cd4c-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cd4c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cd4c-114">Remarks</span></span>

<span data-ttu-id="4cd4c-115">Se essa propriedade é definida no objeto de logon, o cliente deve manter o tamanho da propriedade **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) em que o valor especificado por esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="4cd4c-116">Por outro lado, o servidor deve retornar um erro se o cliente tentar definir uma propriedade binária muito grande.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="4cd4c-117">Para obter informações sobre regras ampliadas, consulte [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4cd4c-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4cd4c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4cd4c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cd4c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4cd4c-119">Protocol specifications</span></span>

<span data-ttu-id="4cd4c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cd4c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cd4c-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4cd4c-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cd4c-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cd4c-123">Especifica as operações permitidas para os objetos do repositório de mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cd4c-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4cd4c-124">Header files</span></span>

<span data-ttu-id="4cd4c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cd4c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cd4c-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cd4c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4cd4c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4cd4c-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cd4c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cd4c-129">See also</span></span>



[<span data-ttu-id="4cd4c-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd4c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cd4c-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4cd4c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cd4c-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd4c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cd4c-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4cd4c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

