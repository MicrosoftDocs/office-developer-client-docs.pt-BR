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
ms.openlocfilehash: 4a8cf9ac24f275d8b9cdbe03b5a90477771a2ab4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768323"
---
# <a name="pidlidbirthdayevententryid-canonical-property"></a><span data-ttu-id="c63bf-103">Propriedade canônica PidLidBirthdayEventEntryId</span><span class="sxs-lookup"><span data-stu-id="c63bf-103">PidLidBirthdayEventEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c63bf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c63bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c63bf-105">Especifica a **identificação de entrada** de um compromisso opcional que representa o aniversário do contato.</span><span class="sxs-lookup"><span data-stu-id="c63bf-105">Specifies the **EntryId** of an optional appointment that represents the contact's birthday.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c63bf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c63bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c63bf-107">dispidBirthdayEventEID</span><span class="sxs-lookup"><span data-stu-id="c63bf-107">dispidBirthdayEventEID</span></span>  <br/> |
|<span data-ttu-id="c63bf-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="c63bf-108">Property set:</span></span>  <br/> |<span data-ttu-id="c63bf-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="c63bf-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="c63bf-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="c63bf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c63bf-111">0x0000804D</span><span class="sxs-lookup"><span data-stu-id="c63bf-111">0x0000804D</span></span>  <br/> |
|<span data-ttu-id="c63bf-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c63bf-112">Data type:</span></span>  <br/> |<span data-ttu-id="c63bf-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c63bf-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c63bf-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c63bf-114">Area:</span></span>  <br/> |<span data-ttu-id="c63bf-115">Contato</span><span class="sxs-lookup"><span data-stu-id="c63bf-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c63bf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c63bf-116">Remarks</span></span>

<span data-ttu-id="c63bf-117">O compromisso que for especificado por esta propriedade deve ser vinculado a este contato usando o **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)) e ** dispidContactLinkName** propriedades de ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)), conforme especificado na [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c63bf-117">The appointment this is specified by this property must be linked to this contact by using the **dispidApptStateFlags** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)), **dispidContactLinkSearchKey** ([PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md)), and **dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) properties, as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c63bf-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c63bf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c63bf-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c63bf-119">Protocol specifications</span></span>

<span data-ttu-id="c63bf-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c63bf-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c63bf-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c63bf-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c63bf-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c63bf-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c63bf-123">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="c63bf-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c63bf-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c63bf-124">Header files</span></span>

<span data-ttu-id="c63bf-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c63bf-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c63bf-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c63bf-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c63bf-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c63bf-127">See also</span></span>



[<span data-ttu-id="c63bf-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c63bf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c63bf-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c63bf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c63bf-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c63bf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c63bf-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c63bf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
