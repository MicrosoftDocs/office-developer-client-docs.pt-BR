---
title: Propriedade canônica PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412727"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="04f58-103">Propriedade canônica PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="04f58-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="04f58-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04f58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04f58-105">Contém o identificador de entrada da raiz da subárvore da pasta de mensagens interpessoais (IPM) na árvore de pastas do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="04f58-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04f58-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="04f58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04f58-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="04f58-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="04f58-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="04f58-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04f58-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="04f58-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="04f58-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="04f58-110">Data type:</span></span>  <br/> |<span data-ttu-id="04f58-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="04f58-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="04f58-112">Área:</span><span class="sxs-lookup"><span data-stu-id="04f58-112">Area:</span></span>  <br/> |<span data-ttu-id="04f58-113">Folder</span><span class="sxs-lookup"><span data-stu-id="04f58-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04f58-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="04f58-114">Remarks</span></span>

<span data-ttu-id="04f58-115">Esta propriedade representa a raiz da hierarquia IPM.</span><span class="sxs-lookup"><span data-stu-id="04f58-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="04f58-116">Os clientes IPM não devem exibir pastas que não sejam subpastas da pasta representada por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="04f58-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04f58-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="04f58-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="04f58-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="04f58-118">Header files</span></span>

<span data-ttu-id="04f58-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="04f58-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="04f58-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="04f58-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="04f58-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="04f58-121">Mapitags.h</span></span>
  
> <span data-ttu-id="04f58-122">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="04f58-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04f58-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="04f58-123">See also</span></span>



[<span data-ttu-id="04f58-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="04f58-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04f58-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="04f58-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04f58-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="04f58-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04f58-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="04f58-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

