---
title: Propriedade canônica PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415723"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="17358-103">Propriedade canônica PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="17358-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="17358-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17358-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17358-105">Contém um valor de verificação de integridade de conteúdo ASN.1 que permite que um remetente de mensagem proteja o conteúdo da mensagem contra divulgação para destinatários não autorizados.</span><span class="sxs-lookup"><span data-stu-id="17358-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17358-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="17358-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17358-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="17358-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="17358-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="17358-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17358-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="17358-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="17358-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="17358-110">Data type:</span></span>  <br/> |<span data-ttu-id="17358-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="17358-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="17358-112">Área:</span><span class="sxs-lookup"><span data-stu-id="17358-112">Area:</span></span>  <br/> |<span data-ttu-id="17358-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="17358-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17358-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="17358-114">Remarks</span></span>

<span data-ttu-id="17358-115">Essa propriedade fornece não repúdio do conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="17358-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="17358-116">Em conjunto com **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), garante que o conteúdo de uma mensagem chegue ao seu destino inalterado.</span><span class="sxs-lookup"><span data-stu-id="17358-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17358-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17358-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="17358-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="17358-118">Header files</span></span>

<span data-ttu-id="17358-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17358-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="17358-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="17358-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="17358-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17358-121">Mapitags.h</span></span>
  
> <span data-ttu-id="17358-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="17358-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17358-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="17358-123">See also</span></span>



[<span data-ttu-id="17358-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17358-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17358-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="17358-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17358-126">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="17358-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17358-127">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="17358-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

