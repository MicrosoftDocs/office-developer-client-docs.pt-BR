---
title: Propriedade canônica PidTagInternetMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ce5de883d28d7575a8abb83ec48454752ea7ba6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580478"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="6651d-103">Propriedade canônica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="6651d-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="6651d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6651d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6651d-105">Corresponde ao campo de ID de mensagem conforme especificado na [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="6651d-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6651d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6651d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6651d-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="6651d-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="6651d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6651d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6651d-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="6651d-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="6651d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6651d-110">Data type:</span></span>  <br/> |<span data-ttu-id="6651d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6651d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6651d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6651d-112">Area:</span></span>  <br/> |<span data-ttu-id="6651d-113">MIME</span><span class="sxs-lookup"><span data-stu-id="6651d-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6651d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6651d-114">Remarks</span></span>

<span data-ttu-id="6651d-115">Essas propriedades devem estar presentes em todas as mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="6651d-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6651d-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6651d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6651d-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6651d-117">Protocol specifications</span></span>

<span data-ttu-id="6651d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6651d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6651d-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6651d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6651d-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6651d-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6651d-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="6651d-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6651d-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6651d-122">Header files</span></span>

<span data-ttu-id="6651d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6651d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6651d-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6651d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6651d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6651d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6651d-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6651d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6651d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6651d-127">See also</span></span>



[<span data-ttu-id="6651d-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6651d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6651d-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6651d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6651d-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6651d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6651d-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6651d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

