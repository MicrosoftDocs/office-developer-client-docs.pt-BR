---
title: Propriedade canônica PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769689"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="e6c67-103">Propriedade canônica PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="e6c67-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="e6c67-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6c67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6c67-105">Contém o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="e6c67-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6c67-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e6c67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6c67-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e6c67-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e6c67-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e6c67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e6c67-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="e6c67-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="e6c67-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e6c67-110">Data type:</span></span>  <br/> |<span data-ttu-id="e6c67-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e6c67-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e6c67-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e6c67-112">Area:</span></span>  <br/> |<span data-ttu-id="e6c67-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="e6c67-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6c67-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6c67-114">Remarks</span></span>

<span data-ttu-id="e6c67-115">Essas propriedades são calculadas por provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="e6c67-115">These properties are computed by service providers.</span></span> <span data-ttu-id="e6c67-116">Implementação de um provedor da função **ServiceEntry** pode utilizar essas propriedades para descobrir o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="e6c67-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="e6c67-117">Aplicativos cliente podem usar essas propriedades como uma alternativa conveniente para obter o nome do perfil examinando a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) na linha de tabela de status do subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6c67-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="e6c67-118">Essas propriedades podem não ser exclusivas longo do tempo, por exemplo onde um perfil é excluído e recriado mais tarde com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="e6c67-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="e6c67-119">MAPI fornece uma propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) totalmente exclusiva em uma seção de perfil codificadas chamada **MUID_PROFILE_INSTANCE.**</span><span class="sxs-lookup"><span data-stu-id="e6c67-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e6c67-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6c67-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e6c67-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6c67-121">Header files</span></span>

<span data-ttu-id="e6c67-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6c67-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6c67-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e6c67-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="e6c67-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e6c67-124">Mapitags.h</span></span>
  
> <span data-ttu-id="e6c67-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e6c67-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6c67-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6c67-126">See also</span></span>



[<span data-ttu-id="e6c67-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e6c67-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6c67-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e6c67-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6c67-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e6c67-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6c67-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e6c67-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
