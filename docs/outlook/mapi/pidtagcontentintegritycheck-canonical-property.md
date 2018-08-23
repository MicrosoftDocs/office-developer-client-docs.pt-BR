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
ms.openlocfilehash: 53226daafd1c0a53f96db5af3432d6f34738fd93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585805"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="f1d08-103">Propriedade canônica PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="f1d08-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="f1d08-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1d08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1d08-105">Contém um valor de verificação de integridade do conteúdo de ASN. 1 que permite que um remetente da mensagem proteger o conteúdo da mensagem do divulgação para destinatários não autorizados.</span><span class="sxs-lookup"><span data-stu-id="f1d08-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1d08-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f1d08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1d08-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="f1d08-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="f1d08-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f1d08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1d08-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="f1d08-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="f1d08-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f1d08-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1d08-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f1d08-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f1d08-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f1d08-112">Area:</span></span>  <br/> |<span data-ttu-id="f1d08-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f1d08-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1d08-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1d08-114">Remarks</span></span>

<span data-ttu-id="f1d08-115">Essa propriedade oferece para não-recusa do conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1d08-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="f1d08-116">Em conjunto com **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), ele garante que o conteúdo de uma mensagem chega ao seu destino inalterado.</span><span class="sxs-lookup"><span data-stu-id="f1d08-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1d08-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1d08-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f1d08-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f1d08-118">Header files</span></span>

<span data-ttu-id="f1d08-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1d08-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1d08-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f1d08-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1d08-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f1d08-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f1d08-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="f1d08-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1d08-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1d08-123">See also</span></span>



[<span data-ttu-id="f1d08-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f1d08-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1d08-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f1d08-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1d08-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f1d08-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1d08-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f1d08-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

