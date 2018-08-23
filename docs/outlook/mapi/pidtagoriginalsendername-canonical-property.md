---
title: Propriedade canônica PidTagOriginalSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 11f8df87dd9248a9d6061892bb0500274478646d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579162"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="e730d-103">Propriedade canônica PidTagOriginalSenderName</span><span class="sxs-lookup"><span data-stu-id="e730d-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="e730d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e730d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e730d-105">Contém o nome de exibição do remetente da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="e730d-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e730d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e730d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e730d-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e730d-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e730d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e730d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e730d-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="e730d-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="e730d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e730d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e730d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e730d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e730d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e730d-112">Area:</span></span>  <br/> |<span data-ttu-id="e730d-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="e730d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e730d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e730d-114">Remarks</span></span>

<span data-ttu-id="e730d-115">Essas propriedades são exemplos das propriedades de endereço do remetente original de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e730d-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="e730d-116">No primeiro envio da mensagem, um aplicativo cliente deve definir essas propriedades com o valor da propriedade **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e730d-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="e730d-117">Ele nunca é alterado quando a mensagem for encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="e730d-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e730d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e730d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e730d-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e730d-119">Protocol specifications</span></span>

<span data-ttu-id="e730d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e730d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e730d-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e730d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e730d-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e730d-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e730d-123">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e730d-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e730d-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e730d-124">Header files</span></span>

<span data-ttu-id="e730d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e730d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e730d-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e730d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e730d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e730d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e730d-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e730d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e730d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e730d-129">See also</span></span>



[<span data-ttu-id="e730d-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e730d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e730d-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e730d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e730d-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e730d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e730d-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e730d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

