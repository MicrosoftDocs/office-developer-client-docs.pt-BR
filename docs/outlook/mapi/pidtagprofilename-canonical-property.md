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
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435646"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="aba19-103">Propriedade canônica PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="aba19-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="aba19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aba19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aba19-105">Contém o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="aba19-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aba19-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="aba19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aba19-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="aba19-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="aba19-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="aba19-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aba19-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="aba19-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="aba19-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="aba19-110">Data type:</span></span>  <br/> |<span data-ttu-id="aba19-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aba19-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aba19-112">Área:</span><span class="sxs-lookup"><span data-stu-id="aba19-112">Area:</span></span>  <br/> |<span data-ttu-id="aba19-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="aba19-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aba19-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aba19-114">Remarks</span></span>

<span data-ttu-id="aba19-115">Essas propriedades são calculadas pelos provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="aba19-115">These properties are computed by service providers.</span></span> <span data-ttu-id="aba19-116">A implementação da função **ServiceEntry** de um provedor pode usar essas propriedades para descobrir o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="aba19-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="aba19-117">Os aplicativos cliente podem usar essas propriedades como uma alternativa conveniente para obter o nome do perfil examinando a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) na linha da tabela de status do subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="aba19-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="aba19-118">Essas propriedades podem não ser exclusivas ao longo do tempo, por exemplo, onde um perfil é excluído e posteriormente recriado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="aba19-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="aba19-119">O MAPI fornece uma propriedade **totalmente exclusiva PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) em uma seção de perfil em código chamada **MUID_PROFILE_INSTANCE.**</span><span class="sxs-lookup"><span data-stu-id="aba19-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aba19-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="aba19-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="aba19-121">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="aba19-121">Header files</span></span>

<span data-ttu-id="aba19-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aba19-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="aba19-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="aba19-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="aba19-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aba19-124">Mapitags.h</span></span>
  
> <span data-ttu-id="aba19-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="aba19-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aba19-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aba19-126">See also</span></span>



[<span data-ttu-id="aba19-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="aba19-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aba19-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="aba19-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aba19-129">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="aba19-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aba19-130">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="aba19-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

