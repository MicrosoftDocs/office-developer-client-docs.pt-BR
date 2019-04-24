---
title: Propriedade canônica PidTagScheduleInfoDelegateEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b2adde7c5ecc75fda25b94d005fabfcd705d5d07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321291"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="c484e-103">Propriedade canônica PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="c484e-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="c484e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c484e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c484e-105">Contém o **ENTRYIDs** dos representantes.</span><span class="sxs-lookup"><span data-stu-id="c484e-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c484e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c484e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c484e-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="c484e-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="c484e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c484e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c484e-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="c484e-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="c484e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c484e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c484e-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c484e-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="c484e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c484e-112">Area:</span></span>  <br/> |<span data-ttu-id="c484e-113">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="c484e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c484e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c484e-114">Remarks</span></span>

<span data-ttu-id="c484e-115">Cada entrada deve conter o valor da propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da entrada do catálogo de endereços de cada representante.</span><span class="sxs-lookup"><span data-stu-id="c484e-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="c484e-116">Essa propriedade deve ser definida no objeto delegate Information.</span><span class="sxs-lookup"><span data-stu-id="c484e-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c484e-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c484e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c484e-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="c484e-118">Protocol specifications</span></span>

<span data-ttu-id="c484e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c484e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c484e-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c484e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c484e-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c484e-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c484e-122">Especifica métodos para conectar e configurar caixas de correio como delegados e interações com objetos de mensagem e calendário quando eles atuam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="c484e-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c484e-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c484e-123">Header files</span></span>

<span data-ttu-id="c484e-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c484e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c484e-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c484e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c484e-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c484e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c484e-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c484e-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c484e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c484e-128">See also</span></span>



[<span data-ttu-id="c484e-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c484e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c484e-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c484e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c484e-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c484e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c484e-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c484e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

