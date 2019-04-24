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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360092"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="b4459-103">Propriedade canônica PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="b4459-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="b4459-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4459-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4459-105">Contém uma lista de identificadores de entrada para destinatários alternativos designados pelo destinatário original.</span><span class="sxs-lookup"><span data-stu-id="b4459-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4459-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b4459-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4459-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="b4459-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="b4459-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b4459-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4459-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="b4459-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="b4459-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b4459-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4459-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4459-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4459-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b4459-112">Area:</span></span>  <br/> |<span data-ttu-id="b4459-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="b4459-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4459-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4459-114">Remarks</span></span>

<span data-ttu-id="b4459-115">Essa propriedade é usada para mensagens de encaminhamento automático.</span><span class="sxs-lookup"><span data-stu-id="b4459-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="b4459-116">Ele contém uma estrutura [FLATENTRYLIST](flatentrylist.md) de destinatários alternativos.</span><span class="sxs-lookup"><span data-stu-id="b4459-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="b4459-117">Se o encaminhamento não for permitido ou se nenhum destinatário alternativo tiver sido designado, um relatório de não entrega será gerado.</span><span class="sxs-lookup"><span data-stu-id="b4459-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b4459-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4459-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4459-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="b4459-119">Protocol specifications</span></span>

<span data-ttu-id="b4459-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4459-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4459-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b4459-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4459-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4459-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4459-123">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="b4459-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b4459-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4459-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4459-125">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="b4459-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b4459-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4459-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4459-127">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="b4459-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4459-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b4459-128">Header files</span></span>

<span data-ttu-id="b4459-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b4459-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b4459-130">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="b4459-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="b4459-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b4459-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4459-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b4459-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4459-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4459-133">See also</span></span>



[<span data-ttu-id="b4459-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="b4459-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="b4459-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b4459-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4459-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b4459-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4459-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b4459-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4459-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b4459-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

