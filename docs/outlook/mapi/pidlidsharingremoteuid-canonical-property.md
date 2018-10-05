---
title: Propriedade canônica PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394731"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="185f4-103">Propriedade canônica PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="185f4-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="185f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="185f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="185f4-105">Especifica a identificação de entrada da pasta remota está sendo compartilhada.</span><span class="sxs-lookup"><span data-stu-id="185f4-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="185f4-106">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="185f4-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="185f4-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="185f4-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="185f4-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="185f4-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="185f4-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="185f4-109">Property set:</span></span>  <br/> |<span data-ttu-id="185f4-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="185f4-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="185f4-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="185f4-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="185f4-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="185f4-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="185f4-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="185f4-113">Data type:</span></span>  <br/> |<span data-ttu-id="185f4-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="185f4-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="185f4-115">Área:</span><span class="sxs-lookup"><span data-stu-id="185f4-115">Area:</span></span>  <br/> |<span data-ttu-id="185f4-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="185f4-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="185f4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="185f4-117">Remarks</span></span>

<span data-ttu-id="185f4-118">Esta propriedade deve ser definida como a representação de cadeia de caracteres hexadecimais do valor da propriedade PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) na pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="185f4-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="185f4-119">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="185f4-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="185f4-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="185f4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="185f4-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="185f4-121">Protocol specifications</span></span>

<span data-ttu-id="185f4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="185f4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="185f4-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="185f4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="185f4-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="185f4-124">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="185f4-125">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="185f4-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="185f4-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="185f4-126">Header files</span></span>

<span data-ttu-id="185f4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="185f4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="185f4-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="185f4-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="185f4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="185f4-129">See also</span></span>



[<span data-ttu-id="185f4-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="185f4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="185f4-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="185f4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="185f4-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="185f4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="185f4-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="185f4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

