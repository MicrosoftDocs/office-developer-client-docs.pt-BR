---
title: Propriedade canônica PidTagRuleSequence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleSequence
api_type:
- COM
ms.assetid: c42f2539-f7d6-464a-a82c-f0ac51823168
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 70e7a20a69b7467c1d8c31469273dcc28ce219ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321242"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="b2946-103">Propriedade canônica PidTagRuleSequence</span><span class="sxs-lookup"><span data-stu-id="b2946-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="b2946-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2946-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2946-105">Um valor usado para determinar a ordem na qual as regras são avaliadas e executadas.</span><span class="sxs-lookup"><span data-stu-id="b2946-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2946-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b2946-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2946-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="b2946-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="b2946-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b2946-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2946-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="b2946-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="b2946-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b2946-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2946-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b2946-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b2946-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b2946-112">Area:</span></span>  <br/> |<span data-ttu-id="b2946-113">Regras do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="b2946-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2946-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2946-114">Remarks</span></span>

<span data-ttu-id="b2946-115">As regras são avaliadas em sequência de acordo com a ordem crescente desse valor.</span><span class="sxs-lookup"><span data-stu-id="b2946-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="b2946-116">A ordem de avaliação para regras que têm o mesmo valor nessa propriedade é indefinida.</span><span class="sxs-lookup"><span data-stu-id="b2946-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b2946-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2946-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2946-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b2946-118">Protocol specifications</span></span>

<span data-ttu-id="b2946-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2946-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2946-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b2946-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2946-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2946-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2946-122">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="b2946-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="b2946-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2946-123">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2946-124">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com itens de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="b2946-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="b2946-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2946-125">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2946-126">Inclui operações permitidas para os objetos de tabela principais.</span><span class="sxs-lookup"><span data-stu-id="b2946-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="b2946-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2946-127">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2946-128">Especifica operações permitidas para os objetos principais do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b2946-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2946-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b2946-129">Header files</span></span>

<span data-ttu-id="b2946-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2946-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2946-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b2946-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2946-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b2946-132">Mapitags.h</span></span>
  
> <span data-ttu-id="b2946-133">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b2946-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2946-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2946-134">See also</span></span>



[<span data-ttu-id="b2946-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b2946-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2946-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b2946-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2946-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b2946-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2946-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b2946-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

