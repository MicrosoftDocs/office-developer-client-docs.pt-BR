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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391931"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="8911c-103">Propriedade canônica PidLidBirthdayEventEntryId</span><span class="sxs-lookup"><span data-stu-id="8911c-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8911c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8911c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8911c-105">Especifica a **identificação de entrada** de um compromisso opcional que representa o aniversário do contato.</span><span class="sxs-lookup"><span data-stu-id="8911c-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8911c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8911c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8911c-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="8911c-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="8911c-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="8911c-108">Property set:</span></span>  <br/> |<span data-ttu-id="8911c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="8911c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="8911c-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="8911c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8911c-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="8911c-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="8911c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8911c-112">Data type:</span></span>  <br/> |<span data-ttu-id="8911c-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8911c-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8911c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8911c-114">Area:</span></span>  <br/> |<span data-ttu-id="8911c-115">Contato</span><span class="sxs-lookup"><span data-stu-id="8911c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8911c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8911c-116">Remarks</span></span>

<span data-ttu-id="8911c-117">O compromisso que for especificado por esta propriedade deve ser vinculado a este contato usando o **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) e \*\* dispidContactLinkName\*\* propriedades de ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), conforme especificado na [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8911c-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8911c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8911c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8911c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8911c-119">Protocol specifications</span></span>

<span data-ttu-id="8911c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8911c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8911c-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8911c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8911c-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8911c-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8911c-123">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="8911c-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8911c-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8911c-124">Header files</span></span>

<span data-ttu-id="8911c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8911c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8911c-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8911c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8911c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8911c-127">See also</span></span>



[<span data-ttu-id="8911c-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8911c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8911c-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8911c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8911c-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8911c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8911c-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8911c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

