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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401508"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a><span data-ttu-id="6b58c-103">Propriedade canônica PidTagScheduleInfoDelegateEntryIds</span><span class="sxs-lookup"><span data-stu-id="6b58c-103">PidTagScheduleInfoDelegateEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="6b58c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b58c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b58c-105">Contém as **EntryIDs** de representantes.</span><span class="sxs-lookup"><span data-stu-id="6b58c-105">Contains the **EntryIDs** of the delegates.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b58c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6b58c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b58c-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="6b58c-107">PR_SCHDINFO_DELEGATE_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="6b58c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6b58c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b58c-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="6b58c-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="6b58c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6b58c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b58c-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="6b58c-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="6b58c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6b58c-112">Area:</span></span>  <br/> |<span data-ttu-id="6b58c-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="6b58c-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b58c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b58c-114">Remarks</span></span>

<span data-ttu-id="6b58c-115">Cada entrada deve conter o valor da propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de entrada do catálogo de endereços do cada representante.</span><span class="sxs-lookup"><span data-stu-id="6b58c-115">Each entry must contain the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property of each delegate's address book entry.</span></span> <span data-ttu-id="6b58c-116">Essa propriedade deverá ser definida no objeto de informações do representante.</span><span class="sxs-lookup"><span data-stu-id="6b58c-116">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6b58c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b58c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b58c-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6b58c-118">Protocol specifications</span></span>

<span data-ttu-id="6b58c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b58c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b58c-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6b58c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b58c-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b58c-121">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b58c-122">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="6b58c-122">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b58c-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6b58c-123">Header files</span></span>

<span data-ttu-id="6b58c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b58c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b58c-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6b58c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b58c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6b58c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6b58c-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6b58c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b58c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b58c-128">See also</span></span>



[<span data-ttu-id="6b58c-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6b58c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b58c-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6b58c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b58c-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6b58c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b58c-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6b58c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

