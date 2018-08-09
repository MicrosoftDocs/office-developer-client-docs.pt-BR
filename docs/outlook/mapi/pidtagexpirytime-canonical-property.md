---
title: Propriedade canônica PidTagExpiryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryTime
api_type:
- HeaderDef
ms.assetid: 6e4d4ee9-c6b1-4987-b02e-684c2af3d21c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4666a5837c9f9f2ceb209088929aa3d343eb02f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769243"
---
# <a name="pidtagexpirytime-canonical-property"></a><span data-ttu-id="17fc9-103">Propriedade canônica PidTagExpiryTime</span><span class="sxs-lookup"><span data-stu-id="17fc9-103">PidTagExpiryTime Canonical Property</span></span>

  
  
<span data-ttu-id="17fc9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17fc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17fc9-105">Contém a data e hora de quando o sistema de mensagens pode invalidar o conteúdo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="17fc9-105">Contains the date and time when the messaging system can invalidate the content of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17fc9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="17fc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17fc9-107">PR_EXPIRY_TIME</span><span class="sxs-lookup"><span data-stu-id="17fc9-107">PR_EXPIRY_TIME</span></span>  <br/> |
|<span data-ttu-id="17fc9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="17fc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17fc9-109">0x0015</span><span class="sxs-lookup"><span data-stu-id="17fc9-109">0x0015</span></span>  <br/> |
|<span data-ttu-id="17fc9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="17fc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="17fc9-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="17fc9-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="17fc9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="17fc9-112">Area:</span></span>  <br/> |<span data-ttu-id="17fc9-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="17fc9-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17fc9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="17fc9-114">Remarks</span></span>

<span data-ttu-id="17fc9-115">Essa propriedade é usada para direcionar que o sistema de mensagens na manipulação entregue interpessoais emails.</span><span class="sxs-lookup"><span data-stu-id="17fc9-115">This property is used to direct the messaging system in handling delivered interpersonal messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="17fc9-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17fc9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17fc9-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="17fc9-117">Protocol specifications</span></span>

<span data-ttu-id="17fc9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17fc9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17fc9-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="17fc9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17fc9-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17fc9-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17fc9-121">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="17fc9-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17fc9-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="17fc9-122">Header files</span></span>

<span data-ttu-id="17fc9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17fc9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="17fc9-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="17fc9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="17fc9-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17fc9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="17fc9-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="17fc9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17fc9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="17fc9-127">See also</span></span>



[<span data-ttu-id="17fc9-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17fc9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17fc9-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="17fc9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17fc9-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="17fc9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17fc9-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="17fc9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

