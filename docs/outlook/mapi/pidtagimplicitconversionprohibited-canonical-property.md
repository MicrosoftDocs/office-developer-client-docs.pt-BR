---
title: Propriedade canônica PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dcfaf9f4e71a13a8697da0cac98f7ea9cc3d8708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769347"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="c9ab5-103">Propriedade canônica PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="c9ab5-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="c9ab5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9ab5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9ab5-105">Conterá TRUE se um agente de transferência de mensagem (MTA) é proibido de fazer a mensagem implícita conversões de texto.</span><span class="sxs-lookup"><span data-stu-id="c9ab5-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9ab5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c9ab5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9ab5-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="c9ab5-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="c9ab5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9ab5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9ab5-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="c9ab5-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="c9ab5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c9ab5-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9ab5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c9ab5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c9ab5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9ab5-112">Area:</span></span>  <br/> |<span data-ttu-id="c9ab5-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="c9ab5-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9ab5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9ab5-114">Remarks</span></span>

<span data-ttu-id="c9ab5-115">Se essa propriedade for TRUE, o sistema de mensagens deve não execute nenhuma conversão de conteúdo na mensagem, a menos que seja solicitado explicitamente em uma base por destinatário com a propriedade **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c9ab5-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9ab5-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9ab5-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9ab5-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9ab5-117">Header files</span></span>

<span data-ttu-id="c9ab5-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9ab5-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9ab5-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c9ab5-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9ab5-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9ab5-120">Mapitags.h</span></span>
  
> <span data-ttu-id="c9ab5-121">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c9ab5-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9ab5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9ab5-122">See also</span></span>



[<span data-ttu-id="c9ab5-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ab5-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9ab5-124">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c9ab5-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9ab5-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ab5-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9ab5-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c9ab5-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

