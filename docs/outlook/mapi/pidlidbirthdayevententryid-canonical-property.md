---
title: Propriedade canônica PidLidBirthdayEventEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBirthdayEventEntryId
api_type:
- COM
ms.assetid: 6807dcfc-d9bd-48a1-a093-3097b2cb107c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 90d1dc8a9ce7f94238e8754cfbcaf88b702928f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342018"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="e27f8-103">Propriedade canônica PidLidBirthdayEventEntryId</span><span class="sxs-lookup"><span data-stu-id="e27f8-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e27f8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e27f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e27f8-105">Especifica a **EntryId de** um compromisso opcional que representa o aniversário do contato.</span><span class="sxs-lookup"><span data-stu-id="e27f8-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e27f8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e27f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e27f8-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="e27f8-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="e27f8-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="e27f8-108">Property set:</span></span>  <br/> |<span data-ttu-id="e27f8-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="e27f8-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="e27f8-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e27f8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e27f8-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="e27f8-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="e27f8-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e27f8-112">Data type:</span></span>  <br/> |<span data-ttu-id="e27f8-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e27f8-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e27f8-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e27f8-114">Area:</span></span>  <br/> |<span data-ttu-id="e27f8-115">Contato</span><span class="sxs-lookup"><span data-stu-id="e27f8-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e27f8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e27f8-116">Remarks</span></span>

<span data-ttu-id="e27f8-117">O compromisso especificado por essa propriedade deve ser vinculado a esse contato usando as propriedades **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) e **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), conforme especificado [em [MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e27f8-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e27f8-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e27f8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e27f8-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e27f8-119">Protocol specifications</span></span>

<span data-ttu-id="e27f8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e27f8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e27f8-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e27f8-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e27f8-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e27f8-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e27f8-123">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="e27f8-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e27f8-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e27f8-124">Header files</span></span>

<span data-ttu-id="e27f8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e27f8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e27f8-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e27f8-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e27f8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e27f8-127">See also</span></span>



[<span data-ttu-id="e27f8-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e27f8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e27f8-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e27f8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e27f8-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e27f8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e27f8-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e27f8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

