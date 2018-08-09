---
title: Propriedade canônica PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ccf4a6054ecc89e280f2f5cbc4c72b2a8a829055
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769033"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="1e5fc-103">Propriedade canônica PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="1e5fc-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="1e5fc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e5fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e5fc-105">Contém a data e hora que o remetente da mensagem enviada uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e5fc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1e5fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e5fc-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="1e5fc-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="1e5fc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1e5fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e5fc-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="1e5fc-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="1e5fc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1e5fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e5fc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1e5fc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1e5fc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1e5fc-112">Area:</span></span>  <br/> |<span data-ttu-id="1e5fc-113">Hora da mensagem</span><span class="sxs-lookup"><span data-stu-id="1e5fc-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e5fc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e5fc-114">Remarks</span></span>

<span data-ttu-id="1e5fc-115">O provedor de armazenamento define **PR_CLIENT_SUBMIT_TIME** até o momento em que o aplicativo cliente chamado [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="1e5fc-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e5fc-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e5fc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e5fc-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1e5fc-117">Protocol specifications</span></span>

<span data-ttu-id="1e5fc-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e5fc-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e5fc-119">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e5fc-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1e5fc-120">Header files</span></span>

<span data-ttu-id="1e5fc-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e5fc-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e5fc-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e5fc-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e5fc-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1e5fc-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e5fc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e5fc-125">See also</span></span>



[<span data-ttu-id="1e5fc-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1e5fc-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e5fc-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1e5fc-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e5fc-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1e5fc-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e5fc-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1e5fc-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

