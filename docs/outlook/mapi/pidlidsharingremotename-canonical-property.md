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
ms.openlocfilehash: fc3324cb686733f06b9cc0945c93b7df2e5980ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768663"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="7643c-103">Propriedade canônica PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="7643c-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="7643c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7643c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7643c-105">Especifica o nome da pasta remoto que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7643c-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="7643c-106">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7643c-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7643c-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7643c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="7643c-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="7643c-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="7643c-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="7643c-109">Property set:</span></span>  <br/> |<span data-ttu-id="7643c-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="7643c-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="7643c-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="7643c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7643c-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="7643c-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="7643c-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7643c-113">Data type:</span></span>  <br/> |<span data-ttu-id="7643c-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7643c-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7643c-115">Área:</span><span class="sxs-lookup"><span data-stu-id="7643c-115">Area:</span></span>  <br/> |<span data-ttu-id="7643c-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="7643c-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7643c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7643c-117">Remarks</span></span>

<span data-ttu-id="7643c-118">Essa propriedade deve ser definida como o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) na pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="7643c-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7643c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7643c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7643c-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7643c-120">Protocol specifications</span></span>

<span data-ttu-id="7643c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7643c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7643c-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7643c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7643c-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7643c-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7643c-124">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="7643c-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7643c-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7643c-125">Header files</span></span>

<span data-ttu-id="7643c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7643c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7643c-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7643c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7643c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7643c-128">See also</span></span>



[<span data-ttu-id="7643c-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7643c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7643c-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7643c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7643c-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7643c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7643c-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7643c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

