---
title: Propriedade canônica PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361079"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="1b3ed-103">Propriedade canônica PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="1b3ed-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="1b3ed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b3ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b3ed-105">Contém um identificador de objeto ASN.1 especificando o aplicativo que forneceu um anexo.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b3ed-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1b3ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b3ed-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="1b3ed-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="1b3ed-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1b3ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b3ed-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="1b3ed-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="1b3ed-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1b3ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b3ed-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1b3ed-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1b3ed-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1b3ed-112">Area:</span></span>  <br/> |<span data-ttu-id="1b3ed-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="1b3ed-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b3ed-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b3ed-114">Remarks</span></span>

<span data-ttu-id="1b3ed-115">Essa propriedade identifica o aplicativo que gerou originalmente o anexo.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="1b3ed-116">**Observação** As **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  e PR_ATTACH_TAG propriedades não devem ser confundidas.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="1b3ed-117">Eles não estão emparelhados ou relacionados.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-117">They are not paired or related.</span></span> <span data-ttu-id="1b3ed-118">**PR_ATTACH_ENCODING** identifica o algoritmo usado para transformar os dados em um anexo.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="1b3ed-119">"Object" tem um significado muito mais geral no identificador de objeto do termo e no uso de X.400 do que na programação orientada a objeto.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="1b3ed-120">A sintaxe do identificador de objeto e os identificadores de objeto de exemplo são definidos no MAPIOID. Arquivo de header H.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="1b3ed-121">Os valores **PR_ATTACH_TAG** não são limitados aos definidos em MAPIOID.H.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="1b3ed-122">Para obter informações completas sobre esses identificadores de objeto, consulte a documentação sobre ASN.1, X.208 e X.209.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="1b3ed-123">O identificador de objeto é encontrado no elemento de referência de aplicativo do ambiente FTBP (File Transfer Body Part).</span><span class="sxs-lookup"><span data-stu-id="1b3ed-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1b3ed-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b3ed-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b3ed-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1b3ed-125">Protocol specifications</span></span>

<span data-ttu-id="1b3ed-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b3ed-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b3ed-127">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b3ed-128">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1b3ed-128">Header files</span></span>

<span data-ttu-id="1b3ed-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b3ed-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b3ed-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b3ed-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b3ed-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1b3ed-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1b3ed-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b3ed-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b3ed-133">See also</span></span>



[<span data-ttu-id="1b3ed-134">Propriedade canônica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="1b3ed-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="1b3ed-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3ed-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b3ed-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3ed-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b3ed-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3ed-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b3ed-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1b3ed-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

