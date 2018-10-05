---
title: Propriedade canônica PidTagAttachMimeTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389096"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="a1ed7-103">Propriedade canônica PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="a1ed7-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="a1ed7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1ed7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1ed7-105">Contém informações de formatação sobre um anexo de email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="a1ed7-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1ed7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a1ed7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1ed7-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="a1ed7-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="a1ed7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a1ed7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1ed7-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="a1ed7-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="a1ed7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a1ed7-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1ed7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1ed7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a1ed7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a1ed7-112">Area:</span></span>  <br/> |<span data-ttu-id="a1ed7-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="a1ed7-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1ed7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1ed7-114">Remarks</span></span>

<span data-ttu-id="a1ed7-115">Se a propriedade **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contiver o valor **OID_MIMETAG**, o provedor de transporte deve examinar essas propriedades para determinar como o anexo é formatado.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="a1ed7-116">Essas propriedades são copiadas no parâmetro tipo de conteúdo do cabeçalho da entrada de MIME.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="a1ed7-117">A composição da cadeia de caracteres é definida no documento RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="a1ed7-118">O formato é tipo/subtipo, como binário do aplicativo ou texto/simples.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1ed7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1ed7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1ed7-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a1ed7-120">Protocol specifications</span></span>

<span data-ttu-id="a1ed7-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1ed7-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1ed7-122">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a1ed7-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1ed7-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1ed7-124">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1ed7-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a1ed7-125">Header files</span></span>

<span data-ttu-id="a1ed7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1ed7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1ed7-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1ed7-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1ed7-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a1ed7-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a1ed7-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1ed7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1ed7-130">See also</span></span>



[<span data-ttu-id="a1ed7-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ed7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1ed7-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a1ed7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1ed7-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ed7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1ed7-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a1ed7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

