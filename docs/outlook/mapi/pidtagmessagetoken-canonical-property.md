---
title: Propriedade canônica PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408184"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="c8b0f-103">Propriedade canônica PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="c8b0f-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="c8b0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8b0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8b0f-105">Contém um token de segurança ASN.1 para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8b0f-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8b0f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c8b0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8b0f-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="c8b0f-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="c8b0f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c8b0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8b0f-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="c8b0f-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="c8b0f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c8b0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8b0f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c8b0f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c8b0f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c8b0f-112">Area:</span></span>  <br/> |<span data-ttu-id="c8b0f-113">Propriedades de Mensagens Seguras</span><span class="sxs-lookup"><span data-stu-id="c8b0f-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8b0f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8b0f-114">Remarks</span></span>

<span data-ttu-id="c8b0f-115">Essa propriedade transmite informações protegidas relacionadas à segurança de seu originador para seu destinatário.</span><span class="sxs-lookup"><span data-stu-id="c8b0f-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="c8b0f-116">Em conjunto com a **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), ela garante a associação do rótulo com o conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8b0f-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="c8b0f-117">Em conjunto com a **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), verifica se o conteúdo da mensagem não foi alterado.</span><span class="sxs-lookup"><span data-stu-id="c8b0f-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8b0f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8b0f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c8b0f-119">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="c8b0f-119">Header files</span></span>

<span data-ttu-id="c8b0f-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8b0f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8b0f-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c8b0f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8b0f-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8b0f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c8b0f-123">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c8b0f-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8b0f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8b0f-124">See also</span></span>



[<span data-ttu-id="c8b0f-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c8b0f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8b0f-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c8b0f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8b0f-127">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c8b0f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8b0f-128">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c8b0f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

