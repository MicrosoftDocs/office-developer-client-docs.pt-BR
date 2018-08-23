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
ms.openlocfilehash: 6b5def94096f7664169935a062d3b28171fb2919
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578427"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="71e19-103">Propriedade canônica PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="71e19-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="71e19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71e19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71e19-105">Contém um token de segurança de uma mensagem ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="71e19-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71e19-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="71e19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71e19-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="71e19-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="71e19-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="71e19-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71e19-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="71e19-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="71e19-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="71e19-110">Data type:</span></span>  <br/> |<span data-ttu-id="71e19-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="71e19-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="71e19-112">Área:</span><span class="sxs-lookup"><span data-stu-id="71e19-112">Area:</span></span>  <br/> |<span data-ttu-id="71e19-113">Propriedades de mensagens de seguro</span><span class="sxs-lookup"><span data-stu-id="71e19-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71e19-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="71e19-114">Remarks</span></span>

<span data-ttu-id="71e19-115">Essa propriedade transmite protegidas informações relacionadas à segurança do originador ao destinatário.</span><span class="sxs-lookup"><span data-stu-id="71e19-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="71e19-116">Em conjunto com a propriedade **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), garante a associação do rótulo com o conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="71e19-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="71e19-117">Em conjunto com a propriedade **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), ele verifica se o conteúdo da mensagem está inalterado.</span><span class="sxs-lookup"><span data-stu-id="71e19-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71e19-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="71e19-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="71e19-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="71e19-119">Header files</span></span>

<span data-ttu-id="71e19-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71e19-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="71e19-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="71e19-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="71e19-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71e19-122">Mapitags.h</span></span>
  
> <span data-ttu-id="71e19-123">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="71e19-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71e19-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="71e19-124">See also</span></span>



[<span data-ttu-id="71e19-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="71e19-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71e19-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="71e19-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71e19-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="71e19-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71e19-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="71e19-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

