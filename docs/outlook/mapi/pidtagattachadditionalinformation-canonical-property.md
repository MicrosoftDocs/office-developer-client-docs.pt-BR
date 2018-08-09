---
title: Propriedade canônica PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 83de3a4ad7c93b2dfee8063ab63bfbf0724a5f61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768946"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="8ad16-103">Propriedade canônica PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="8ad16-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="8ad16-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ad16-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ad16-105">Fornece informações de tipo de arquivo para um anexo não-Windows.</span><span class="sxs-lookup"><span data-stu-id="8ad16-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ad16-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8ad16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ad16-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="8ad16-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="8ad16-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8ad16-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ad16-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="8ad16-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="8ad16-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8ad16-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ad16-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8ad16-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8ad16-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8ad16-112">Area:</span></span>  <br/> |<span data-ttu-id="8ad16-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="8ad16-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ad16-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ad16-114">Remarks</span></span>

<span data-ttu-id="8ad16-115">Essa propriedade oferece metadados sobre um determinada anexo com base em codificação do anexo.</span><span class="sxs-lookup"><span data-stu-id="8ad16-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="8ad16-116">Por exemplo, quando a propriedade **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contém MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contém uma cadeia de caracteres que representa o criador de arquivo do Macintosh e do tipo de arquivo, formatado como ":CREA:TYPE" para o arquivo codificado do Macintosh.</span><span class="sxs-lookup"><span data-stu-id="8ad16-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ad16-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ad16-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ad16-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8ad16-118">Protocol specifications</span></span>

<span data-ttu-id="8ad16-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ad16-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ad16-120">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="8ad16-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ad16-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8ad16-121">Header files</span></span>

<span data-ttu-id="8ad16-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ad16-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ad16-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8ad16-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ad16-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ad16-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8ad16-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8ad16-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ad16-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ad16-126">See also</span></span>



[<span data-ttu-id="8ad16-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad16-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ad16-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8ad16-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ad16-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad16-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ad16-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8ad16-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

