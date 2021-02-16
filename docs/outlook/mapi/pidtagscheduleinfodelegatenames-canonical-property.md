---
title: Propriedade canônica PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314935"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="369d6-103">Propriedade canônica PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="369d6-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="369d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="369d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="369d6-105">Contém os nomes dos representantes.</span><span class="sxs-lookup"><span data-stu-id="369d6-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="369d6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="369d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="369d6-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="369d6-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="369d6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="369d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="369d6-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="369d6-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="369d6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="369d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="369d6-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="369d6-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="369d6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="369d6-112">Area:</span></span>  <br/> |<span data-ttu-id="369d6-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="369d6-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="369d6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="369d6-114">Remarks</span></span>

<span data-ttu-id="369d6-115">Cada entrada nessas propriedades deve conter o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do livro de endereços de cada representante.</span><span class="sxs-lookup"><span data-stu-id="369d6-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="369d6-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="369d6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="369d6-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="369d6-117">Protocol specifications</span></span>

<span data-ttu-id="369d6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="369d6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="369d6-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="369d6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="369d6-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="369d6-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="369d6-121">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="369d6-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="369d6-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="369d6-122">Header files</span></span>

<span data-ttu-id="369d6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="369d6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="369d6-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="369d6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="369d6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="369d6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="369d6-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="369d6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="369d6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="369d6-127">See also</span></span>



[<span data-ttu-id="369d6-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="369d6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="369d6-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="369d6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="369d6-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="369d6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="369d6-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="369d6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

