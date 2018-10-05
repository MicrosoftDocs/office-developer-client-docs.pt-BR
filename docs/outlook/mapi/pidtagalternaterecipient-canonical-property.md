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
ms.openlocfilehash: 7c304de3184e49044d3f83cef1f1ebaac019b2ee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392778"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="ff6b2-103">Propriedade canônica PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="ff6b2-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="ff6b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff6b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff6b2-105">Contém uma lista de identificadores de entrada para destinatários alternativos designados pelo destinatário original.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff6b2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ff6b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff6b2-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="ff6b2-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="ff6b2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ff6b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff6b2-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="ff6b2-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="ff6b2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ff6b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff6b2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff6b2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff6b2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ff6b2-112">Area:</span></span>  <br/> |<span data-ttu-id="ff6b2-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="ff6b2-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff6b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff6b2-114">Remarks</span></span>

<span data-ttu-id="ff6b2-115">Essa propriedade é usada para automático mensagens encaminhado.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="ff6b2-116">Ele contém uma estrutura [FLATENTRYLIST](flatentrylist.md) de destinatários alternativos.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="ff6b2-117">Se o encaminhamento automático não é permitido ou nenhum destinatário alternativo foi designado, é gerado um relatório de não entrega.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ff6b2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff6b2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff6b2-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ff6b2-119">Protocol specifications</span></span>

<span data-ttu-id="ff6b2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff6b2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff6b2-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff6b2-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff6b2-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff6b2-123">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ff6b2-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff6b2-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff6b2-125">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ff6b2-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff6b2-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff6b2-127">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff6b2-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ff6b2-128">Header files</span></span>

<span data-ttu-id="ff6b2-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff6b2-129">Mapitags.h</span></span>
  
> <span data-ttu-id="ff6b2-130">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="ff6b2-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff6b2-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff6b2-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ff6b2-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff6b2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff6b2-133">See also</span></span>



[<span data-ttu-id="ff6b2-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="ff6b2-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="ff6b2-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ff6b2-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff6b2-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ff6b2-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff6b2-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ff6b2-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff6b2-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ff6b2-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

