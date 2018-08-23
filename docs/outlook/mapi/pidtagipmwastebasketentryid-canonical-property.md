---
title: Propriedade canônica PidTagIpmWastebasketEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 66bbf49d737c42ecc2f6c765a60540163649f447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573891"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="a9f50-103">Propriedade canônica PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="a9f50-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a9f50-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9f50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9f50-105">Contém o identificador de entrada da pasta Itens excluídos mensagem interpessoais padrão (IPM).</span><span class="sxs-lookup"><span data-stu-id="a9f50-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9f50-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a9f50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9f50-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a9f50-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a9f50-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a9f50-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9f50-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="a9f50-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="a9f50-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a9f50-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9f50-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9f50-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a9f50-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a9f50-112">Area:</span></span>  <br/> |<span data-ttu-id="a9f50-113">Folder</span><span class="sxs-lookup"><span data-stu-id="a9f50-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9f50-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9f50-114">Remarks</span></span>

<span data-ttu-id="a9f50-115">Um aplicativo cliente deve mover excluídos interpessoais emails para a pasta Itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="a9f50-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="a9f50-116">Se a mensagem estiver nesta pasta, ou se não há suporte para essa propriedade, o cliente deve excluir a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a9f50-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a9f50-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9f50-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a9f50-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a9f50-118">Header files</span></span>

<span data-ttu-id="a9f50-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9f50-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9f50-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a9f50-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9f50-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9f50-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a9f50-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a9f50-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9f50-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9f50-123">See also</span></span>



[<span data-ttu-id="a9f50-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a9f50-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9f50-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a9f50-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9f50-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a9f50-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9f50-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a9f50-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

