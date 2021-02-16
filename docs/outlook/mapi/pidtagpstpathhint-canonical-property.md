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
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437305"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="84c2b-103">Propriedade canônica PidTagPstPathHint</span><span class="sxs-lookup"><span data-stu-id="84c2b-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="84c2b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84c2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84c2b-105">Fornece o nome da tabela de armazenamento pessoal (arquivo .pst), que o usuário pode editar, para a caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="84c2b-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84c2b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="84c2b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84c2b-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="84c2b-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="84c2b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="84c2b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84c2b-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="84c2b-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="84c2b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="84c2b-110">Data type:</span></span>  <br/> |<span data-ttu-id="84c2b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84c2b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="84c2b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="84c2b-112">Area:</span></span>  <br/> |<span data-ttu-id="84c2b-113">Tabela de armazenamento pessoal (.pst) interna</span><span class="sxs-lookup"><span data-stu-id="84c2b-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84c2b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="84c2b-114">Remarks</span></span>

<span data-ttu-id="84c2b-115">Se a **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) for usada em vez disso, a caixa de diálogo de configuração será aberta, mas o usuário não poderá editar o caminho e muitas outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="84c2b-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84c2b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="84c2b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84c2b-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="84c2b-117">Protocol specifications</span></span>

<span data-ttu-id="84c2b-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="84c2b-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="84c2b-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="84c2b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84c2b-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="84c2b-120">Header files</span></span>

<span data-ttu-id="84c2b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84c2b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="84c2b-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="84c2b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="84c2b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84c2b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="84c2b-124">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="84c2b-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84c2b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="84c2b-125">See also</span></span>



[<span data-ttu-id="84c2b-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="84c2b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84c2b-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="84c2b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84c2b-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="84c2b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84c2b-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="84c2b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

