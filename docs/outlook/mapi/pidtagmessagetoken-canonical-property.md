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
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769492"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="00bd6-103">Propriedade canônica PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="00bd6-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="00bd6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00bd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00bd6-105">Contém um token de segurança de uma mensagem ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="00bd6-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00bd6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="00bd6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00bd6-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="00bd6-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="00bd6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="00bd6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00bd6-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="00bd6-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="00bd6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="00bd6-110">Data type:</span></span>  <br/> |<span data-ttu-id="00bd6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="00bd6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="00bd6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="00bd6-112">Area:</span></span>  <br/> |<span data-ttu-id="00bd6-113">Propriedades de mensagens de seguro</span><span class="sxs-lookup"><span data-stu-id="00bd6-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00bd6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="00bd6-114">Remarks</span></span>

<span data-ttu-id="00bd6-115">Essa propriedade transmite protegidas informações relacionadas à segurança do originador ao destinatário.</span><span class="sxs-lookup"><span data-stu-id="00bd6-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="00bd6-116">Em conjunto com a propriedade **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), garante a associação do rótulo com o conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="00bd6-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="00bd6-117">Em conjunto com a propriedade **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), ele verifica se o conteúdo da mensagem está inalterado.</span><span class="sxs-lookup"><span data-stu-id="00bd6-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="00bd6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="00bd6-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="00bd6-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="00bd6-119">Header files</span></span>

<span data-ttu-id="00bd6-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00bd6-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="00bd6-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="00bd6-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="00bd6-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00bd6-122">Mapitags.h</span></span>
  
> <span data-ttu-id="00bd6-123">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="00bd6-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00bd6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="00bd6-124">See also</span></span>



[<span data-ttu-id="00bd6-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="00bd6-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00bd6-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="00bd6-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00bd6-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="00bd6-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00bd6-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="00bd6-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

