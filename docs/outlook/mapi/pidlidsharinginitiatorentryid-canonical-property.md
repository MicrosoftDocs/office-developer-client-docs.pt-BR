---
title: Propriedade canônica PidLidSharingInitiatorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorEntryId
api_type:
- COM
ms.assetid: 47f00706-83df-49cb-bda7-ef572d76a020
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 79392d892944e8ae2470c3da905e47b804d514aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576817"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a><span data-ttu-id="29030-103">Propriedade canônica PidLidSharingInitiatorEntryId</span><span class="sxs-lookup"><span data-stu-id="29030-103">PidLidSharingInitiatorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="29030-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29030-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29030-105">Designa como uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="29030-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29030-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="29030-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29030-107">dispidSharingInitiatorEid</span><span class="sxs-lookup"><span data-stu-id="29030-107">dispidSharingInitiatorEid</span></span>  <br/> |
|<span data-ttu-id="29030-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="29030-108">Property set:</span></span>  <br/> |<span data-ttu-id="29030-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="29030-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="29030-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="29030-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="29030-111">0x00008A09</span><span class="sxs-lookup"><span data-stu-id="29030-111">0x00008A09</span></span>  <br/> |
|<span data-ttu-id="29030-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="29030-112">Data type:</span></span>  <br/> |<span data-ttu-id="29030-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="29030-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="29030-114">Área:</span><span class="sxs-lookup"><span data-stu-id="29030-114">Area:</span></span>  <br/> |<span data-ttu-id="29030-115">Sharing</span><span class="sxs-lookup"><span data-stu-id="29030-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29030-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="29030-116">Remarks</span></span>

<span data-ttu-id="29030-117">Essa propriedade deverá ser definida como o valor da propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para o catálogo de endereços do usuário conectado no momento (consulte [[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span><span class="sxs-lookup"><span data-stu-id="29030-117">This property must be set to the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property for the Address Book of the currently logged-on user (see [[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="29030-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="29030-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29030-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="29030-119">Protocol specifications</span></span>

<span data-ttu-id="29030-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29030-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29030-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="29030-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29030-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29030-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29030-123">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="29030-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29030-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="29030-124">Header files</span></span>

<span data-ttu-id="29030-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29030-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="29030-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="29030-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29030-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="29030-127">See also</span></span>



[<span data-ttu-id="29030-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="29030-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29030-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="29030-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29030-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="29030-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29030-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="29030-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

