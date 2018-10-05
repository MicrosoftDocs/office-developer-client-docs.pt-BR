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
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400331"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="fadb6-103">Propriedade canônica PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="fadb6-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="fadb6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fadb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fadb6-105">O nome do componente de URL para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="fadb6-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fadb6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fadb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fadb6-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="fadb6-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="fadb6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fadb6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fadb6-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="fadb6-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="fadb6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fadb6-110">Data type:</span></span>  <br/> |<span data-ttu-id="fadb6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fadb6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fadb6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fadb6-112">Area:</span></span>  <br/> |<span data-ttu-id="fadb6-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="fadb6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fadb6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fadb6-114">Remarks</span></span>

<span data-ttu-id="fadb6-115">Essas propriedades devem ser exclusivas dentro de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="fadb6-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="fadb6-116">Se não for definida quando a mensagem é criada, o armazenamento de mensagens deve definir essas propriedades com base em várias propriedades de mensagem, dependendo da classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fadb6-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="fadb6-117">Por exemplo, o **IPM. Observação** e **IPM. Compromisso** mensagens devem ter essa propriedade definidas com base na propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e o **IPM. Contato** mensagens devem ter essa propriedade definidas com base na propriedade **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fadb6-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="fadb6-118">Para a maioria das outras classes de mensagem, esta propriedade deve se basear na propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fadb6-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fadb6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fadb6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fadb6-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fadb6-120">Protocol specifications</span></span>

<span data-ttu-id="fadb6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fadb6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fadb6-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fadb6-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fadb6-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fadb6-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fadb6-124">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="fadb6-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="fadb6-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fadb6-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fadb6-126">Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="fadb6-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fadb6-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fadb6-127">Header files</span></span>

<span data-ttu-id="fadb6-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fadb6-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="fadb6-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fadb6-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="fadb6-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fadb6-130">Mapitags.h</span></span>
  
> <span data-ttu-id="fadb6-131">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fadb6-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fadb6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fadb6-132">See also</span></span>



[<span data-ttu-id="fadb6-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fadb6-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fadb6-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fadb6-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fadb6-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fadb6-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fadb6-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fadb6-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

