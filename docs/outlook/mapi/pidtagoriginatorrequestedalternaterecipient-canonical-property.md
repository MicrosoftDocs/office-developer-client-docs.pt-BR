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
ms.openlocfilehash: 463f2eb6e730c9250861ce50515a7f662bb75d23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588864"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="108f3-103">Propriedade canônica PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="108f3-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="108f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="108f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="108f3-105">Contém um identificador de entrada para um destinatário alternativo designado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="108f3-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="108f3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="108f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="108f3-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="108f3-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="108f3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="108f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="108f3-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="108f3-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="108f3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="108f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="108f3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="108f3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="108f3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="108f3-112">Area:</span></span>  <br/> |<span data-ttu-id="108f3-113">MIME</span><span class="sxs-lookup"><span data-stu-id="108f3-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="108f3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="108f3-114">Remarks</span></span>

<span data-ttu-id="108f3-115">Essa propriedade é usada em mensagens de autoforwarded.</span><span class="sxs-lookup"><span data-stu-id="108f3-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="108f3-116">Se o encaminhamento automático não é permitido ou nenhum destinatário alternativo foi designado, um relatório de não entrega deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="108f3-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="108f3-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="108f3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="108f3-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="108f3-118">Header files</span></span>

<span data-ttu-id="108f3-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="108f3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="108f3-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="108f3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="108f3-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="108f3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="108f3-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="108f3-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="108f3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="108f3-123">See also</span></span>



[<span data-ttu-id="108f3-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="108f3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="108f3-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="108f3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="108f3-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="108f3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="108f3-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="108f3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

