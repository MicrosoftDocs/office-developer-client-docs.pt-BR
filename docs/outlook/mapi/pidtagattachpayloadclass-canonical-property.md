---
title: Propriedade canônica PidTagAttachPayloadClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6a84e51325fcb60c54c2f6b42af0c26a0efd3382
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396614"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="298de-103">Propriedade canônica PidTagAttachPayloadClass</span><span class="sxs-lookup"><span data-stu-id="298de-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="298de-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="298de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="298de-105">Contém o valor de um campo de cabeçalho X-carga-classe de MIME.</span><span class="sxs-lookup"><span data-stu-id="298de-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="298de-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="298de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="298de-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="298de-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="298de-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="298de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="298de-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="298de-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="298de-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="298de-110">Data type:</span></span>  <br/> |<span data-ttu-id="298de-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="298de-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="298de-112">Área:</span><span class="sxs-lookup"><span data-stu-id="298de-112">Area:</span></span>  <br/> |<span data-ttu-id="298de-113">Aplicativo do Outlook</span><span class="sxs-lookup"><span data-stu-id="298de-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="298de-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="298de-114">Remarks</span></span>

<span data-ttu-id="298de-115">Para definir o valor dessas propriedades, os clientes MIME devem gravar um campo de cabeçalho X-carga de classe uma entidade MIME que vai ser analisada como um anexo.</span><span class="sxs-lookup"><span data-stu-id="298de-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="298de-116">Leitores MIME devem copiar esse valor de campo de cabeçalho com o valor da propriedade correspondente.</span><span class="sxs-lookup"><span data-stu-id="298de-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="298de-117">Leitores MIME devem ignorar este campo de cabeçalho quando ele aparecer em uma entidade MIME é analisada como uma mensagem ou o corpo da mensagem, e não como um anexo.</span><span class="sxs-lookup"><span data-stu-id="298de-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="298de-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="298de-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="298de-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="298de-119">Protocol specifications</span></span>

<span data-ttu-id="298de-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="298de-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="298de-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="298de-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="298de-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="298de-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="298de-123">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="298de-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="298de-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="298de-124">Header files</span></span>

<span data-ttu-id="298de-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="298de-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="298de-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="298de-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="298de-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="298de-127">Mapitags.h</span></span>
  
> <span data-ttu-id="298de-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="298de-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="298de-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="298de-129">See also</span></span>



[<span data-ttu-id="298de-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="298de-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="298de-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="298de-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="298de-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="298de-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="298de-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="298de-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

