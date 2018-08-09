---
title: Propriedade canônica PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769616"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="6dea4-103">Propriedade canônica PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="6dea4-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="6dea4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6dea4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6dea4-105">Contém um identificador de entrada para um destinatário alternativo designado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="6dea4-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6dea4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6dea4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6dea4-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="6dea4-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="6dea4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6dea4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6dea4-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="6dea4-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="6dea4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6dea4-110">Data type:</span></span>  <br/> |<span data-ttu-id="6dea4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6dea4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6dea4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6dea4-112">Area:</span></span>  <br/> |<span data-ttu-id="6dea4-113">MIME</span><span class="sxs-lookup"><span data-stu-id="6dea4-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dea4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dea4-114">Remarks</span></span>

<span data-ttu-id="6dea4-115">Essa propriedade é usada em mensagens de autoforwarded.</span><span class="sxs-lookup"><span data-stu-id="6dea4-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="6dea4-116">Se o encaminhamento automático não é permitido ou nenhum destinatário alternativo foi designado, um relatório de não entrega deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="6dea4-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6dea4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6dea4-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6dea4-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6dea4-118">Header files</span></span>

<span data-ttu-id="6dea4-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dea4-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6dea4-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6dea4-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6dea4-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6dea4-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6dea4-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6dea4-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6dea4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dea4-123">See also</span></span>



[<span data-ttu-id="6dea4-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6dea4-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6dea4-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6dea4-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6dea4-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6dea4-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6dea4-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6dea4-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

