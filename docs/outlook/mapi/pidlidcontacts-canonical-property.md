---
title: Propriedade canônica PidLidContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 10dd12522a635098908285f1a9ee16c93d96f728
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319457"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="76859-103">Propriedade canônica PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="76859-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="76859-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76859-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76859-105">Contém os nomes dos contatos associados ao item.</span><span class="sxs-lookup"><span data-stu-id="76859-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76859-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="76859-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76859-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="76859-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="76859-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="76859-108">Property set:</span></span>  <br/> |<span data-ttu-id="76859-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="76859-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="76859-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="76859-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="76859-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="76859-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="76859-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="76859-112">Data type:</span></span>  <br/> |<span data-ttu-id="76859-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76859-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="76859-114">Área:</span><span class="sxs-lookup"><span data-stu-id="76859-114">Area:</span></span>  <br/> |<span data-ttu-id="76859-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="76859-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76859-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="76859-116">Remarks</span></span>

<span data-ttu-id="76859-117">Essa propriedade contém a **propriedade PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de cada **EntryID** do Livro de Endereços referenciado no valor da **propriedade dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="76859-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="76859-118">Ele pode incluir nomes não referenciados em **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="76859-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76859-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="76859-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76859-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="76859-120">Protocol specifications</span></span>

<span data-ttu-id="76859-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76859-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76859-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="76859-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="76859-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76859-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76859-124">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="76859-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="76859-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76859-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76859-126">Especifica as propriedades e operações permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="76859-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="76859-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76859-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76859-128">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="76859-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76859-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="76859-129">Header files</span></span>

<span data-ttu-id="76859-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76859-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="76859-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="76859-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76859-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="76859-132">See also</span></span>



[<span data-ttu-id="76859-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="76859-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76859-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="76859-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76859-135">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="76859-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76859-136">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="76859-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

