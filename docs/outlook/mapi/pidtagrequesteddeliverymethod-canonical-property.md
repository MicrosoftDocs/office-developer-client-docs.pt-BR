---
title: Propriedade canônica PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434071"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="80cd9-103">Propriedade canônica PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="80cd9-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="80cd9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80cd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80cd9-105">Essa propriedade contém uma matriz binária de métodos de entrega (provedores de serviço), na ordem de preferência de um remetente de mensagem.</span><span class="sxs-lookup"><span data-stu-id="80cd9-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80cd9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="80cd9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80cd9-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="80cd9-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="80cd9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="80cd9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80cd9-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="80cd9-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="80cd9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="80cd9-110">Data type:</span></span>  <br/> |<span data-ttu-id="80cd9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="80cd9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="80cd9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="80cd9-112">Area:</span></span>  <br/> |<span data-ttu-id="80cd9-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="80cd9-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80cd9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="80cd9-114">Remarks</span></span>

<span data-ttu-id="80cd9-115">A matriz contida na propriedade é composta por identificadores ASN. 1 para cada um dos provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="80cd9-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="80cd9-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="80cd9-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="80cd9-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="80cd9-117">Header files</span></span>

<span data-ttu-id="80cd9-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="80cd9-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="80cd9-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="80cd9-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="80cd9-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="80cd9-120">Mapitags.h</span></span>
  
> <span data-ttu-id="80cd9-121">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="80cd9-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80cd9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="80cd9-122">See also</span></span>



[<span data-ttu-id="80cd9-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="80cd9-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80cd9-124">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="80cd9-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80cd9-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="80cd9-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80cd9-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="80cd9-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

