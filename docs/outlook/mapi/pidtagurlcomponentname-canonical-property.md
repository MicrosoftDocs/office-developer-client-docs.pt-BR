---
title: Propriedade canônica PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3a2b0939bbfa5143e4bd99e74b0f84e3ca7efb12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770151"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="3520f-103">Propriedade canônica PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="3520f-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="3520f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3520f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3520f-105">O nome do componente de URL para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3520f-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3520f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3520f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3520f-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="3520f-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="3520f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3520f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3520f-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="3520f-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="3520f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3520f-110">Data type:</span></span>  <br/> |<span data-ttu-id="3520f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3520f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3520f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3520f-112">Area:</span></span>  <br/> |<span data-ttu-id="3520f-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="3520f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3520f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3520f-114">Remarks</span></span>

<span data-ttu-id="3520f-115">Essas propriedades devem ser exclusivas dentro de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="3520f-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="3520f-116">Se não for definida quando a mensagem é criada, o armazenamento de mensagens deve definir essas propriedades com base em várias propriedades de mensagem, dependendo da classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3520f-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="3520f-117">Por exemplo, o **IPM. Observação** e **IPM. Compromisso** mensagens devem ter essa propriedade definidas com base na propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e o **IPM. Contato** mensagens devem ter essa propriedade definidas com base na propriedade **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3520f-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="3520f-118">Para a maioria das outras classes de mensagem, esta propriedade deve se basear na propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3520f-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3520f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3520f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3520f-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3520f-120">Protocol specifications</span></span>

<span data-ttu-id="3520f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3520f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3520f-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3520f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3520f-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3520f-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3520f-124">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="3520f-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3520f-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3520f-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3520f-126">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="3520f-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3520f-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3520f-127">Header files</span></span>

<span data-ttu-id="3520f-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3520f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3520f-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3520f-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="3520f-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3520f-130">Mapitags.h</span></span>
  
> <span data-ttu-id="3520f-131">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3520f-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3520f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3520f-132">See also</span></span>



[<span data-ttu-id="3520f-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3520f-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3520f-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3520f-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3520f-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3520f-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3520f-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3520f-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

