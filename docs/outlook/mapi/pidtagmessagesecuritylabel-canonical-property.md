---
title: Propriedade canônica PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a6caa322e1d266be1fe56aecd89736e757067758
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594366"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="ed154-103">Propriedade canônica PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="ed154-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="ed154-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed154-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed154-105">Contém um rótulo de segurança de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ed154-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed154-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ed154-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed154-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="ed154-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="ed154-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ed154-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed154-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="ed154-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="ed154-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ed154-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed154-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ed154-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ed154-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ed154-112">Area:</span></span>  <br/> |<span data-ttu-id="ed154-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="ed154-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed154-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed154-114">Remarks</span></span>

<span data-ttu-id="ed154-115">Essa propriedade fornece a base nos quais a propriedade **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protege uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ed154-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="ed154-116">Sua associação com o conteúdo da mensagem é garantida pelo token.</span><span class="sxs-lookup"><span data-stu-id="ed154-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed154-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed154-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ed154-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed154-118">Header files</span></span>

<span data-ttu-id="ed154-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed154-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed154-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ed154-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed154-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed154-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ed154-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="ed154-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed154-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed154-123">See also</span></span>



[<span data-ttu-id="ed154-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ed154-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed154-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ed154-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed154-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ed154-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed154-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ed154-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

