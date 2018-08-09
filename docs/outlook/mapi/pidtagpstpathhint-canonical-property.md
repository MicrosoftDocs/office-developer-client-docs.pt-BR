---
title: Propriedade canônica PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 295b20ebc0c41104a8b1c8e46e2064c3ef32f99e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769732"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="926a0-103">Propriedade canônica PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="926a0-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="926a0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="926a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="926a0-105">Fornece o nome de tabela (arquivo. pst) do armazenamento pessoal, que o usuário pode editar, para a caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="926a0-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="926a0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="926a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="926a0-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="926a0-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="926a0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="926a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="926a0-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="926a0-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="926a0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="926a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="926a0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="926a0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="926a0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="926a0-112">Area:</span></span>  <br/> |<span data-ttu-id="926a0-113">Tabela de armazenamento pessoal (. pst) interna</span><span class="sxs-lookup"><span data-stu-id="926a0-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="926a0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="926a0-114">Remarks</span></span>

<span data-ttu-id="926a0-115">Se a propriedade **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) for usada em vez disso, a caixa de diálogo de configuração será aberto, mas o usuário não poderão para editar o caminho e muitas outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="926a0-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="926a0-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="926a0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="926a0-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="926a0-117">Protocol specifications</span></span>

<span data-ttu-id="926a0-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="926a0-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="926a0-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="926a0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="926a0-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="926a0-120">Header files</span></span>

<span data-ttu-id="926a0-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="926a0-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="926a0-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="926a0-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="926a0-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="926a0-123">Mapitags.h</span></span>
  
> <span data-ttu-id="926a0-124">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="926a0-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="926a0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="926a0-125">See also</span></span>



[<span data-ttu-id="926a0-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="926a0-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="926a0-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="926a0-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="926a0-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="926a0-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="926a0-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="926a0-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

