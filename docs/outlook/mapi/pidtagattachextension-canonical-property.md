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
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319758"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="d1365-103">Propriedade canônica PidTagAttachExtension</span><span class="sxs-lookup"><span data-stu-id="d1365-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="d1365-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1365-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1365-105">Contém uma extensão de nome de arquivo que indica o tipo de documento de um anexo.</span><span class="sxs-lookup"><span data-stu-id="d1365-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1365-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d1365-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1365-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="d1365-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="d1365-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d1365-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1365-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="d1365-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="d1365-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d1365-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1365-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1365-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d1365-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d1365-112">Area:</span></span>  <br/> |<span data-ttu-id="d1365-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="d1365-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1365-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1365-114">Remarks</span></span>

<span data-ttu-id="d1365-115">Essas propriedades são definidas pelo aplicativo cliente no momento do envio.</span><span class="sxs-lookup"><span data-stu-id="d1365-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="d1365-116">O sistema de mensagens usa **PR_ATTACH_EXTENSION** ao converter anexos de mensagem (conversão em rota) ou iniciar aplicativos com base em anexos em mensagens recebidas.</span><span class="sxs-lookup"><span data-stu-id="d1365-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="d1365-117">Se o cliente de envio não fornecer um valor para essas propriedades, o armazenamento de mensagens que manipula o anexo não será obrigado a gerá-lo.</span><span class="sxs-lookup"><span data-stu-id="d1365-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="d1365-118">O cliente receptor deve primeiro verificar se **o PR_ATTACH_EXTENSION** e, se não for fornecido, deve analisar a extensão do nome de arquivo da propriedade **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ou **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) do anexo.</span><span class="sxs-lookup"><span data-stu-id="d1365-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d1365-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1365-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1365-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d1365-120">Protocol specifications</span></span>

<span data-ttu-id="d1365-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1365-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1365-122">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="d1365-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1365-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d1365-123">Header files</span></span>

<span data-ttu-id="d1365-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1365-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1365-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d1365-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1365-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d1365-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d1365-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d1365-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1365-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1365-128">See also</span></span>



[<span data-ttu-id="d1365-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1365-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1365-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d1365-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1365-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d1365-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1365-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d1365-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

