---
title: Propriedade canônica PidTagResponseRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 77c724affd2057ca6347d752323c5ba0a3094ecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330153"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="336d5-103">Propriedade canônica PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="336d5-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="336d5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="336d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="336d5-105">Contém TRUE se o remetente da mensagem quiser uma resposta a uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="336d5-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="336d5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="336d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="336d5-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="336d5-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="336d5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="336d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="336d5-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="336d5-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="336d5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="336d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="336d5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="336d5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="336d5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="336d5-112">Area:</span></span>  <br/> |<span data-ttu-id="336d5-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="336d5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="336d5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="336d5-114">Remarks</span></span>

<span data-ttu-id="336d5-115">Essa propriedade é usada para solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="336d5-115">This property is used for meeting requests.</span></span> <span data-ttu-id="336d5-116">O aplicativo cliente de recebimento deve solicitar que o usuário aceite ou recuse a solicitação e, em seguida, envie essa resposta de volta para o remetente.</span><span class="sxs-lookup"><span data-stu-id="336d5-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="336d5-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="336d5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="336d5-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="336d5-118">Protocol specifications</span></span>

<span data-ttu-id="336d5-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336d5-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336d5-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="336d5-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="336d5-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336d5-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336d5-122">Especifica as propriedades e as operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="336d5-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="336d5-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336d5-123">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336d5-124">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="336d5-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="336d5-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="336d5-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="336d5-126">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="336d5-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="336d5-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="336d5-127">Header files</span></span>

<span data-ttu-id="336d5-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="336d5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="336d5-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="336d5-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="336d5-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="336d5-130">Mapitags.h</span></span>
  
> <span data-ttu-id="336d5-131">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="336d5-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="336d5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="336d5-132">See also</span></span>



[<span data-ttu-id="336d5-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="336d5-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="336d5-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="336d5-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="336d5-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="336d5-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="336d5-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="336d5-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

