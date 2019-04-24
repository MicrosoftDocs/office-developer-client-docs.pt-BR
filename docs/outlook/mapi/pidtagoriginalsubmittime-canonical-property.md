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
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341045"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="d1e70-103">Propriedade canônica PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="d1e70-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="d1e70-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1e70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1e70-105">Contém a data e a hora de envio originais da mensagem no relatório.</span><span class="sxs-lookup"><span data-stu-id="d1e70-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1e70-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d1e70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1e70-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="d1e70-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="d1e70-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d1e70-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1e70-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="d1e70-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="d1e70-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d1e70-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1e70-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d1e70-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d1e70-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d1e70-112">Area:</span></span>  <br/> |<span data-ttu-id="d1e70-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="d1e70-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1e70-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1e70-114">Remarks</span></span>

<span data-ttu-id="d1e70-115">No primeiro envio de uma mensagem, um aplicativo cliente deve definir essa propriedade como o valor da propriedade **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d1e70-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="d1e70-116">Ela não é alterada quando a mensagem é encaminhada.</span><span class="sxs-lookup"><span data-stu-id="d1e70-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="d1e70-117">Isso é usado somente em relatórios.</span><span class="sxs-lookup"><span data-stu-id="d1e70-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1e70-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1e70-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1e70-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="d1e70-119">Protocol specifications</span></span>

<span data-ttu-id="d1e70-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1e70-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1e70-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d1e70-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1e70-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1e70-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1e70-123">Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d1e70-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1e70-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1e70-124">Header files</span></span>

<span data-ttu-id="d1e70-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d1e70-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1e70-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d1e70-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1e70-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d1e70-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d1e70-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d1e70-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1e70-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1e70-129">See also</span></span>



[<span data-ttu-id="d1e70-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e70-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1e70-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e70-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1e70-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e70-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1e70-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d1e70-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

