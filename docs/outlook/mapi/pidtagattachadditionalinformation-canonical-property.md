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
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339869"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="7053d-103">Propriedade canônica PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="7053d-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="7053d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7053d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7053d-105">Fornece informações de tipo de arquivo para um anexo não Windows.</span><span class="sxs-lookup"><span data-stu-id="7053d-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7053d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7053d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7053d-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="7053d-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="7053d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7053d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7053d-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="7053d-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="7053d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7053d-110">Data type:</span></span>  <br/> |<span data-ttu-id="7053d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7053d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7053d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7053d-112">Area:</span></span>  <br/> |<span data-ttu-id="7053d-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="7053d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7053d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7053d-114">Remarks</span></span>

<span data-ttu-id="7053d-115">Esta propriedade fornece metadados sobre um anexo específico com base na codificação do anexo.</span><span class="sxs-lookup"><span data-stu-id="7053d-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="7053d-116">Por exemplo, quando a propriedade **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contém MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contém uma cadeia de caracteres que representa o criador e o tipo de arquivo do Macintosh, formatado como ": CREA: tipo" para o arquivo de Macintosh codificado.</span><span class="sxs-lookup"><span data-stu-id="7053d-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7053d-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7053d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7053d-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="7053d-118">Protocol specifications</span></span>

<span data-ttu-id="7053d-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7053d-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7053d-120">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="7053d-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7053d-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7053d-121">Header files</span></span>

<span data-ttu-id="7053d-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7053d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="7053d-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7053d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="7053d-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7053d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="7053d-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7053d-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7053d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7053d-126">See also</span></span>



[<span data-ttu-id="7053d-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7053d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7053d-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7053d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7053d-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7053d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7053d-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7053d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

