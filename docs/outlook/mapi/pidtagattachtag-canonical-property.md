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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400450"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="6f06e-103">Propriedade canônica PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="6f06e-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="6f06e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f06e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f06e-105">Contém um identificador de objeto de ASN. 1 que especifica o aplicativo que forneceu um anexo.</span><span class="sxs-lookup"><span data-stu-id="6f06e-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f06e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6f06e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f06e-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="6f06e-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="6f06e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6f06e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f06e-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="6f06e-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="6f06e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6f06e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f06e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6f06e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6f06e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6f06e-112">Area:</span></span>  <br/> |<span data-ttu-id="6f06e-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="6f06e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f06e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f06e-114">Remarks</span></span>

<span data-ttu-id="6f06e-115">Esta propriedade identifica o aplicativo que gerou originalmente o anexo.</span><span class="sxs-lookup"><span data-stu-id="6f06e-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="6f06e-116">**Observação** As propriedades **PR_ATTACH_TAG** de **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) e não devem ser confundidas.</span><span class="sxs-lookup"><span data-stu-id="6f06e-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="6f06e-117">Eles não são combinados ou relacionados.</span><span class="sxs-lookup"><span data-stu-id="6f06e-117">They are not paired or related.</span></span> <span data-ttu-id="6f06e-118">**PR_ATTACH_ENCODING** identifica o algoritmo usado para transformar os dados em um anexo.</span><span class="sxs-lookup"><span data-stu-id="6f06e-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="6f06e-119">"Objeto" tem um significado muito mais geral do identificador de objeto do termo e na utilização de x. 400, que na programação orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="6f06e-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="6f06e-120">Identificadores de objeto do objeto identificador sintaxe e exemplo forem definidos no MAPIOID. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="6f06e-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="6f06e-121">Valores para **PR_ATTACH_TAG** não estão limitados àqueles definidos no MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="6f06e-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="6f06e-122">Para obter informações completas sobre esses identificadores de objeto, consulte a documentação sobre ASN. 1, X.208 e 209.</span><span class="sxs-lookup"><span data-stu-id="6f06e-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="6f06e-123">O identificador de objeto é encontrado no elemento de referência do aplicativo do ambiente do arquivo transferir corpo parte (FTBP).</span><span class="sxs-lookup"><span data-stu-id="6f06e-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f06e-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f06e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f06e-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6f06e-125">Protocol specifications</span></span>

<span data-ttu-id="6f06e-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f06e-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f06e-127">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="6f06e-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f06e-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f06e-128">Header files</span></span>

<span data-ttu-id="6f06e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f06e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f06e-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6f06e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f06e-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f06e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="6f06e-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6f06e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f06e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f06e-133">See also</span></span>



[<span data-ttu-id="6f06e-134">Propriedade canônica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="6f06e-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="6f06e-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6f06e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f06e-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6f06e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f06e-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6f06e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f06e-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6f06e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

