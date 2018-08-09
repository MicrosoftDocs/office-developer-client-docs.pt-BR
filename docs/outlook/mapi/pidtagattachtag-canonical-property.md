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
ms.openlocfilehash: d8d8d32bddb98e0ac180b0898478c67297980492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769009"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="46640-103">Propriedade canônica PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="46640-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="46640-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46640-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46640-105">Contém um identificador de objeto de ASN. 1 que especifica o aplicativo que forneceu um anexo.</span><span class="sxs-lookup"><span data-stu-id="46640-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46640-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="46640-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46640-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="46640-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="46640-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="46640-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46640-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="46640-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="46640-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="46640-110">Data type:</span></span>  <br/> |<span data-ttu-id="46640-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="46640-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="46640-112">Área:</span><span class="sxs-lookup"><span data-stu-id="46640-112">Area:</span></span>  <br/> |<span data-ttu-id="46640-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="46640-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46640-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="46640-114">Remarks</span></span>

<span data-ttu-id="46640-115">Esta propriedade identifica o aplicativo que gerou originalmente o anexo.</span><span class="sxs-lookup"><span data-stu-id="46640-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="46640-116">**Observação** As propriedades **PR_ATTACH_TAG** de **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) e não devem ser confundidas.</span><span class="sxs-lookup"><span data-stu-id="46640-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="46640-117">Eles não são combinados ou relacionados.</span><span class="sxs-lookup"><span data-stu-id="46640-117">They are not paired or related.</span></span> <span data-ttu-id="46640-118">**PR_ATTACH_ENCODING** identifica o algoritmo usado para transformar os dados em um anexo.</span><span class="sxs-lookup"><span data-stu-id="46640-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="46640-119">"Objeto" tem um significado muito mais geral do identificador de objeto do termo e na utilização de x. 400, que na programação orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="46640-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="46640-120">Identificadores de objeto do objeto identificador sintaxe e exemplo forem definidos no MAPIOID. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="46640-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="46640-121">Valores para **PR_ATTACH_TAG** não estão limitados àqueles definidos no MAPIOID. H.</span><span class="sxs-lookup"><span data-stu-id="46640-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="46640-122">Para obter informações completas sobre esses identificadores de objeto, consulte a documentação sobre ASN. 1, X.208 e 209.</span><span class="sxs-lookup"><span data-stu-id="46640-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="46640-123">O identificador de objeto é encontrado no elemento de referência do aplicativo do ambiente do arquivo transferir corpo parte (FTBP).</span><span class="sxs-lookup"><span data-stu-id="46640-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="46640-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46640-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46640-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="46640-125">Protocol specifications</span></span>

<span data-ttu-id="46640-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46640-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46640-127">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="46640-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46640-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46640-128">Header files</span></span>

<span data-ttu-id="46640-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46640-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="46640-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="46640-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="46640-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="46640-131">Mapitags.h</span></span>
  
> <span data-ttu-id="46640-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="46640-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46640-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="46640-133">See also</span></span>



[<span data-ttu-id="46640-134">Propriedade canônica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="46640-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="46640-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46640-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46640-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="46640-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46640-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="46640-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46640-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="46640-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

