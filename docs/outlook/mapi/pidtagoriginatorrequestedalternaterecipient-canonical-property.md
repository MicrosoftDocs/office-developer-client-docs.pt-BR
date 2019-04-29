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
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437858"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="ae756-103">Propriedade canônica PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="ae756-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="ae756-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae756-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae756-105">Contém um identificador de entrada para um destinatário alternativo designado pelo remetente.</span><span class="sxs-lookup"><span data-stu-id="ae756-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae756-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ae756-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae756-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="ae756-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="ae756-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ae756-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ae756-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="ae756-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="ae756-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ae756-110">Data type:</span></span>  <br/> |<span data-ttu-id="ae756-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ae756-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ae756-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ae756-112">Area:</span></span>  <br/> |<span data-ttu-id="ae756-113">MIME</span><span class="sxs-lookup"><span data-stu-id="ae756-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae756-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae756-114">Remarks</span></span>

<span data-ttu-id="ae756-115">Essa propriedade é usada em mensagens de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="ae756-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="ae756-116">Se o encaminhamento não for permitido ou se nenhum destinatário alternativo tiver sido designado, um relatório de não entrega deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="ae756-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ae756-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae756-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ae756-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ae756-118">Header files</span></span>

<span data-ttu-id="ae756-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ae756-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae756-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ae756-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ae756-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ae756-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ae756-122">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ae756-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae756-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae756-123">See also</span></span>



[<span data-ttu-id="ae756-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ae756-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae756-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ae756-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae756-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ae756-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae756-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ae756-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

