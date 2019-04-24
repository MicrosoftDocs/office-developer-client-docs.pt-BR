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
ms.openlocfilehash: 3be288b606e197b350c1b053303077c1cb984e9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303091"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="8670c-103">Propriedade canônica PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="8670c-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="8670c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8670c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8670c-105">Especifica o nome da pasta remota que está sendo compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8670c-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="8670c-106">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="8670c-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8670c-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8670c-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8670c-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="8670c-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="8670c-109">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="8670c-109">Property set:</span></span>  <br/> |<span data-ttu-id="8670c-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="8670c-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="8670c-111">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8670c-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8670c-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="8670c-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="8670c-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8670c-113">Data type:</span></span>  <br/> |<span data-ttu-id="8670c-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8670c-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8670c-115">Área:</span><span class="sxs-lookup"><span data-stu-id="8670c-115">Area:</span></span>  <br/> |<span data-ttu-id="8670c-116">Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="8670c-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8670c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8670c-117">Remarks</span></span>

<span data-ttu-id="8670c-118">Essa propriedade deve ser definida como o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) na pasta que está sendo compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8670c-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8670c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8670c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8670c-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="8670c-120">Protocol specifications</span></span>

<span data-ttu-id="8670c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8670c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8670c-122">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8670c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8670c-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8670c-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8670c-124">Compartilha pastas de caixa de correio entre os clientes.</span><span class="sxs-lookup"><span data-stu-id="8670c-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8670c-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8670c-125">Header files</span></span>

<span data-ttu-id="8670c-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8670c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8670c-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8670c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8670c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8670c-128">See also</span></span>



[<span data-ttu-id="8670c-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8670c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8670c-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8670c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8670c-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8670c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8670c-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8670c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

