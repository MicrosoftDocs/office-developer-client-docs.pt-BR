---
title: Propriedade canônica PidTagAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea78d9487e4929c2df3d49a9b85ba4aefac90a59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768930"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="ee220-103">Propriedade canônica PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="ee220-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="ee220-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee220-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee220-105">Contém uma lista de identificadores de entrada para destinatários alternativos designados pelo destinatário original.</span><span class="sxs-lookup"><span data-stu-id="ee220-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee220-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ee220-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee220-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="ee220-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="ee220-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ee220-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee220-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="ee220-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="ee220-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ee220-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee220-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ee220-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ee220-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ee220-112">Area:</span></span>  <br/> |<span data-ttu-id="ee220-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="ee220-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee220-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee220-114">Remarks</span></span>

<span data-ttu-id="ee220-115">Essa propriedade é usada para automático mensagens encaminhado.</span><span class="sxs-lookup"><span data-stu-id="ee220-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="ee220-116">Ele contém uma estrutura [FLATENTRYLIST](flatentrylist.md) de destinatários alternativos.</span><span class="sxs-lookup"><span data-stu-id="ee220-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="ee220-117">Se o encaminhamento automático não é permitido ou nenhum destinatário alternativo foi designado, é gerado um relatório de não entrega.</span><span class="sxs-lookup"><span data-stu-id="ee220-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee220-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee220-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee220-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ee220-119">Protocol specifications</span></span>

<span data-ttu-id="ee220-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee220-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee220-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ee220-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee220-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee220-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee220-123">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="ee220-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ee220-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee220-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee220-125">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="ee220-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ee220-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee220-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee220-127">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="ee220-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee220-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee220-128">Header files</span></span>

<span data-ttu-id="ee220-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee220-129">Mapitags.h</span></span>
  
> <span data-ttu-id="ee220-130">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="ee220-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="ee220-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee220-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee220-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ee220-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee220-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee220-133">See also</span></span>



[<span data-ttu-id="ee220-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="ee220-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="ee220-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ee220-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee220-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ee220-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee220-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ee220-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee220-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ee220-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

