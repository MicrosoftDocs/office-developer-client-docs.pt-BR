---
title: Propriedade canônica PidTagOriginalSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 43d0387f1c25c5ac86168caaddddd9fb9171c827
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769592"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="fbac0-103">Propriedade canônica PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="fbac0-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="fbac0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbac0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbac0-105">Contém a data de envio original e a hora da mensagem no relatório.</span><span class="sxs-lookup"><span data-stu-id="fbac0-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbac0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fbac0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fbac0-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="fbac0-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="fbac0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fbac0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fbac0-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="fbac0-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="fbac0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fbac0-110">Data type:</span></span>  <br/> |<span data-ttu-id="fbac0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fbac0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fbac0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fbac0-112">Area:</span></span>  <br/> |<span data-ttu-id="fbac0-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="fbac0-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbac0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbac0-114">Remarks</span></span>

<span data-ttu-id="fbac0-115">No primeiro envio de uma mensagem, um aplicativo cliente deve definir essa propriedade como o valor da propriedade **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fbac0-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="fbac0-116">Ele não é alterado quando a mensagem é encaminhada.</span><span class="sxs-lookup"><span data-stu-id="fbac0-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="fbac0-117">Isso é usado somente para relatórios.</span><span class="sxs-lookup"><span data-stu-id="fbac0-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fbac0-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fbac0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fbac0-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fbac0-119">Protocol specifications</span></span>

<span data-ttu-id="fbac0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbac0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbac0-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fbac0-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fbac0-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbac0-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbac0-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="fbac0-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fbac0-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fbac0-124">Header files</span></span>

<span data-ttu-id="fbac0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fbac0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fbac0-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fbac0-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="fbac0-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fbac0-127">Mapitags.h</span></span>
  
> <span data-ttu-id="fbac0-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fbac0-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fbac0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbac0-129">See also</span></span>



[<span data-ttu-id="fbac0-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fbac0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fbac0-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fbac0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fbac0-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fbac0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fbac0-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fbac0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

