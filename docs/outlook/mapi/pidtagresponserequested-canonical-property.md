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
ms.openlocfilehash: 02ab7f88edda39fcb1c66eaf643a8263e9d509c8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591727"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="bb204-103">Propriedade canônica PidTagResponseRequested</span><span class="sxs-lookup"><span data-stu-id="bb204-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="bb204-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb204-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb204-105">Conterá TRUE se o remetente da mensagem desejar uma resposta para uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="bb204-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb204-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bb204-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb204-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="bb204-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="bb204-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bb204-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb204-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="bb204-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="bb204-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bb204-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb204-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bb204-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bb204-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bb204-112">Area:</span></span>  <br/> |<span data-ttu-id="bb204-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="bb204-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb204-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb204-114">Remarks</span></span>

<span data-ttu-id="bb204-115">Essa propriedade é usada para solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="bb204-115">This property is used for meeting requests.</span></span> <span data-ttu-id="bb204-116">O aplicativo cliente de recebimento deve solicitar ao usuário para aceitar ou recusar a solicitação e envie essa resposta de volta ao remetente.</span><span class="sxs-lookup"><span data-stu-id="bb204-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb204-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb204-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb204-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bb204-118">Protocol specifications</span></span>

<span data-ttu-id="bb204-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb204-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb204-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bb204-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb204-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb204-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb204-122">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="bb204-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="bb204-123">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb204-123">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb204-124">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="bb204-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="bb204-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb204-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb204-126">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="bb204-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb204-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bb204-127">Header files</span></span>

<span data-ttu-id="bb204-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb204-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb204-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bb204-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb204-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bb204-130">Mapitags.h</span></span>
  
> <span data-ttu-id="bb204-131">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bb204-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb204-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb204-132">See also</span></span>



[<span data-ttu-id="bb204-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bb204-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb204-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bb204-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb204-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bb204-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb204-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bb204-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

