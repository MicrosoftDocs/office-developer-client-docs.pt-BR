---
title: Propriedade canônico de PidTagMessageSecurityLabel
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769481"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="1a9f7-103">Propriedade canônico de PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="1a9f7-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="1a9f7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a9f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a9f7-105">Contém um rótulo de segurança de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a9f7-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a9f7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1a9f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a9f7-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="1a9f7-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="1a9f7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1a9f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a9f7-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="1a9f7-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="1a9f7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1a9f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a9f7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1a9f7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1a9f7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1a9f7-112">Area:</span></span>  <br/> |<span data-ttu-id="1a9f7-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="1a9f7-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a9f7-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="1a9f7-114">Remarks</span></span>

<span data-ttu-id="1a9f7-115">Essa propriedade fornece a base nos quais a propriedade **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protege uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1a9f7-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="1a9f7-116">Sua associação com o conteúdo da mensagem é garantida pelo token.</span><span class="sxs-lookup"><span data-stu-id="1a9f7-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a9f7-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a9f7-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1a9f7-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a9f7-118">Header files</span></span>

<span data-ttu-id="1a9f7-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a9f7-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a9f7-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1a9f7-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a9f7-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a9f7-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1a9f7-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="1a9f7-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a9f7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a9f7-123">See also</span></span>



[<span data-ttu-id="1a9f7-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1a9f7-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a9f7-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1a9f7-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a9f7-126">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1a9f7-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a9f7-127">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="1a9f7-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

