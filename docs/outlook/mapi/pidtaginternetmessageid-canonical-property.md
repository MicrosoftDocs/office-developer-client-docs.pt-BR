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
ms.openlocfilehash: 7b0af907fd5346de5b818c9c75a3d115e598b5e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769375"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="8e355-103">Propriedade canônica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="8e355-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="8e355-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e355-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e355-105">Corresponde ao campo de ID de mensagem conforme especificado na [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="8e355-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e355-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8e355-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e355-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="8e355-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="8e355-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8e355-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e355-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="8e355-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="8e355-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8e355-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e355-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e355-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8e355-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8e355-112">Area:</span></span>  <br/> |<span data-ttu-id="8e355-113">MIME</span><span class="sxs-lookup"><span data-stu-id="8e355-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e355-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e355-114">Remarks</span></span>

<span data-ttu-id="8e355-115">Essas propriedades devem estar presentes em todas as mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="8e355-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e355-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e355-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e355-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8e355-117">Protocol specifications</span></span>

<span data-ttu-id="8e355-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e355-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e355-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8e355-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e355-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e355-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e355-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8e355-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e355-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e355-122">Header files</span></span>

<span data-ttu-id="8e355-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e355-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e355-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8e355-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e355-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e355-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8e355-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8e355-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e355-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e355-127">See also</span></span>



[<span data-ttu-id="8e355-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e355-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e355-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8e355-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e355-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e355-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e355-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8e355-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

