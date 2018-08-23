---
title: Propriedade canônica PidLidSharingRemoteName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteName
api_type:
- COM
ms.assetid: be975f74-4b95-45a4-bbee-959fa8e4ad45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eddcc911653830f63ae4afc564af891d3d7213e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595234"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="cef01-103">Propriedade canônica PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="cef01-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="cef01-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cef01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cef01-105">Especifica o nome da pasta remoto que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="cef01-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="cef01-106">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="cef01-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cef01-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cef01-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="cef01-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="cef01-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="cef01-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="cef01-109">Property set:</span></span>  <br/> |<span data-ttu-id="cef01-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="cef01-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="cef01-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="cef01-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cef01-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="cef01-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="cef01-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cef01-113">Data type:</span></span>  <br/> |<span data-ttu-id="cef01-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cef01-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cef01-115">Área:</span><span class="sxs-lookup"><span data-stu-id="cef01-115">Area:</span></span>  <br/> |<span data-ttu-id="cef01-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="cef01-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cef01-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cef01-117">Remarks</span></span>

<span data-ttu-id="cef01-118">Essa propriedade deve ser definida como o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) na pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="cef01-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cef01-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cef01-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cef01-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cef01-120">Protocol specifications</span></span>

<span data-ttu-id="cef01-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cef01-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cef01-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="cef01-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cef01-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cef01-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cef01-124">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="cef01-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cef01-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cef01-125">Header files</span></span>

<span data-ttu-id="cef01-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cef01-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cef01-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cef01-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cef01-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cef01-128">See also</span></span>



[<span data-ttu-id="cef01-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cef01-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cef01-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cef01-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cef01-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cef01-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cef01-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cef01-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

