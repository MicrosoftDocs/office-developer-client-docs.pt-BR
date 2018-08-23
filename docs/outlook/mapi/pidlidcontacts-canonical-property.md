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
ms.openlocfilehash: 2a097b8e8071c08b82a05f3c8e0b021db8ec5107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585392"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="fb76e-103">Propriedade canônica PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="fb76e-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="fb76e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb76e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb76e-105">Contém os nomes dos contatos associados ao item.</span><span class="sxs-lookup"><span data-stu-id="fb76e-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb76e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fb76e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb76e-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="fb76e-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="fb76e-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="fb76e-108">Property set:</span></span>  <br/> |<span data-ttu-id="fb76e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fb76e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fb76e-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="fb76e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fb76e-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="fb76e-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="fb76e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fb76e-112">Data type:</span></span>  <br/> |<span data-ttu-id="fb76e-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb76e-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fb76e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fb76e-114">Area:</span></span>  <br/> |<span data-ttu-id="fb76e-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="fb76e-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb76e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb76e-116">Remarks</span></span>

<span data-ttu-id="fb76e-117">Essa propriedade contém a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de cada **EntryID** de catálogo de endereços que é referenciado no valor da propriedade **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fb76e-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="fb76e-118">Ela pode incluir nomes não mencionados no **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="fb76e-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fb76e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb76e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb76e-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fb76e-120">Protocol specifications</span></span>

<span data-ttu-id="fb76e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb76e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb76e-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fb76e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb76e-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb76e-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb76e-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="fb76e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="fb76e-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb76e-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb76e-126">Especifica as propriedades e operações que são permitidas para diários.</span><span class="sxs-lookup"><span data-stu-id="fb76e-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="fb76e-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb76e-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb76e-128">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="fb76e-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb76e-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fb76e-129">Header files</span></span>

<span data-ttu-id="fb76e-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb76e-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb76e-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fb76e-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb76e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb76e-132">See also</span></span>



[<span data-ttu-id="fb76e-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fb76e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb76e-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fb76e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb76e-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fb76e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb76e-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fb76e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

