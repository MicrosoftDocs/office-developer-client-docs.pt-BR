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
ms.openlocfilehash: cd42711fc5647f16b33677a330e71d141f1962d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566863"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a><span data-ttu-id="0d41c-103">Propriedade canônica PidLidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="0d41c-103">PidLidSharingRemoteUid Canonical Property</span></span>

  
  
<span data-ttu-id="0d41c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d41c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d41c-105">Especifica a identificação de entrada da pasta remota está sendo compartilhada.</span><span class="sxs-lookup"><span data-stu-id="0d41c-105">Specifies the entry ID of the remote folder being shared.</span></span> <span data-ttu-id="0d41c-106">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0d41c-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d41c-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0d41c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d41c-108">dispidSharingRemoteUid</span><span class="sxs-lookup"><span data-stu-id="0d41c-108">dispidSharingRemoteUid</span></span>  <br/> |
|<span data-ttu-id="0d41c-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="0d41c-109">Property set:</span></span>  <br/> |<span data-ttu-id="0d41c-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="0d41c-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="0d41c-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="0d41c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0d41c-112">0x00008A06</span><span class="sxs-lookup"><span data-stu-id="0d41c-112">0x00008A06</span></span>  <br/> |
|<span data-ttu-id="0d41c-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0d41c-113">Data type:</span></span>  <br/> |<span data-ttu-id="0d41c-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d41c-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0d41c-115">Área:</span><span class="sxs-lookup"><span data-stu-id="0d41c-115">Area:</span></span>  <br/> |<span data-ttu-id="0d41c-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="0d41c-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d41c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d41c-117">Remarks</span></span>

<span data-ttu-id="0d41c-118">Esta propriedade deve ser definida como a representação de cadeia de caracteres hexadecimais do valor da propriedade PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) na pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="0d41c-118">This property must be set to the hexadecimal string representation of the value of the PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) property on the folder being shared.</span></span> <span data-ttu-id="0d41c-119">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0d41c-119">This is a property of a sharing message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d41c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d41c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d41c-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0d41c-121">Protocol specifications</span></span>

<span data-ttu-id="0d41c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d41c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d41c-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d41c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d41c-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d41c-124">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d41c-125">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="0d41c-125">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d41c-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0d41c-126">Header files</span></span>

<span data-ttu-id="0d41c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d41c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d41c-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0d41c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d41c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d41c-129">See also</span></span>



[<span data-ttu-id="0d41c-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0d41c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d41c-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0d41c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d41c-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0d41c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d41c-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0d41c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

