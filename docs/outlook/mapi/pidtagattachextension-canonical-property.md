---
title: Propriedade canônica PidTagAttachExtension
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4d71a0e26e2043bbaf961ae5096afc5789be36be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768966"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="943b4-103">Propriedade canônica PidTagAttachExtension</span><span class="sxs-lookup"><span data-stu-id="943b4-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="943b4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="943b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="943b4-105">Contém uma extensão de nome de arquivo que indica o tipo de documento de um anexo.</span><span class="sxs-lookup"><span data-stu-id="943b4-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="943b4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="943b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="943b4-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="943b4-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="943b4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="943b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="943b4-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="943b4-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="943b4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="943b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="943b4-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="943b4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="943b4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="943b4-112">Area:</span></span>  <br/> |<span data-ttu-id="943b4-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="943b4-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="943b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="943b4-114">Remarks</span></span>

<span data-ttu-id="943b4-115">Essas propriedades são definidas pelo aplicativo cliente em tempo de envio.</span><span class="sxs-lookup"><span data-stu-id="943b4-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="943b4-116">As mensagens **PR_ATTACH_EXTENSION** do sistema usa ao converter os anexos de mensagens (na rota de conversão) ou launching aplicativos baseados em anexos em mensagens recebidas.</span><span class="sxs-lookup"><span data-stu-id="943b4-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="943b4-117">Se o cliente de envio não fornecer um valor para essas propriedades, o armazenamento de mensagens tratamento de anexo não é obrigado a gerá-lo.</span><span class="sxs-lookup"><span data-stu-id="943b4-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="943b4-118">O cliente de recebimento deve verificar primeiro **PR_ATTACH_EXTENSION**e se não for fornecido, deve analisar a extensão de nome de arquivo do **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ou o **PR_ATTACH_LONG_FILENAME do anexo **Propriedade ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="943b4-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="943b4-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="943b4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="943b4-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="943b4-120">Protocol specifications</span></span>

<span data-ttu-id="943b4-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="943b4-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="943b4-122">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="943b4-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="943b4-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="943b4-123">Header files</span></span>

<span data-ttu-id="943b4-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="943b4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="943b4-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="943b4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="943b4-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="943b4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="943b4-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="943b4-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="943b4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="943b4-128">See also</span></span>



[<span data-ttu-id="943b4-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="943b4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="943b4-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="943b4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="943b4-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="943b4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="943b4-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="943b4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

