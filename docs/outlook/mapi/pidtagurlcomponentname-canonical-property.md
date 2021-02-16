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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320423"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="162f5-103">Propriedade canônica PidTagUrlComponentName</span><span class="sxs-lookup"><span data-stu-id="162f5-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="162f5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="162f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="162f5-105">O nome do componente url para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="162f5-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="162f5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="162f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="162f5-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="162f5-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="162f5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="162f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="162f5-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="162f5-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="162f5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="162f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="162f5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="162f5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="162f5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="162f5-112">Area:</span></span>  <br/> |<span data-ttu-id="162f5-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="162f5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="162f5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="162f5-114">Remarks</span></span>

<span data-ttu-id="162f5-115">Essas propriedades devem ser exclusivas em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="162f5-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="162f5-116">Se não for definida quando a mensagem for criada, o armazenamento de mensagens deverá definir essas propriedades com base em várias propriedades da mensagem, dependendo da classe da mensagem.</span><span class="sxs-lookup"><span data-stu-id="162f5-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="162f5-117">Por exemplo, o **IPM. Observação** e **IPM. As** mensagens de compromisso devem ter essa propriedade definida com **base na propriedade PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e no **IPM. As** mensagens de contato devem ter essa propriedade definida com base na **propriedade dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="162f5-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="162f5-118">Para a maioria das outras classes de mensagem, essa propriedade deve ser baseada na **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="162f5-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="162f5-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="162f5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="162f5-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="162f5-120">Protocol specifications</span></span>

<span data-ttu-id="162f5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="162f5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="162f5-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="162f5-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="162f5-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="162f5-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="162f5-124">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="162f5-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="162f5-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="162f5-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="162f5-126">Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="162f5-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="162f5-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="162f5-127">Header files</span></span>

<span data-ttu-id="162f5-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="162f5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="162f5-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="162f5-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="162f5-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="162f5-130">Mapitags.h</span></span>
  
> <span data-ttu-id="162f5-131">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="162f5-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="162f5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="162f5-132">See also</span></span>



[<span data-ttu-id="162f5-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="162f5-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="162f5-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="162f5-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="162f5-135">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="162f5-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="162f5-136">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="162f5-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

