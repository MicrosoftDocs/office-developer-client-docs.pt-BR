---
title: Propriedade canônica PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 71f802014200d4b767c346c14df53f1193d44b0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770029"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="bfe1f-103">Propriedade canônica PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="bfe1f-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="bfe1f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bfe1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bfe1f-105">Contém uma lista de estruturas [MAPIUID](mapiuid.md) que identificam as seções de perfil adicionais para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bfe1f-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe1f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bfe1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfe1f-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="bfe1f-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="bfe1f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bfe1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bfe1f-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="bfe1f-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="bfe1f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bfe1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="bfe1f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bfe1f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bfe1f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bfe1f-112">Area:</span></span>  <br/> |<span data-ttu-id="bfe1f-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe1f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfe1f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfe1f-114">Remarks</span></span>

<span data-ttu-id="bfe1f-115">Novas seções de perfil podem ser criadas para cada filtro de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bfe1f-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="bfe1f-116">Quando as informações sobre o serviço de mensagem deve ser copiado para outro perfil, é importante copiar as seções de perfil adicionais para os filtros também.</span><span class="sxs-lookup"><span data-stu-id="bfe1f-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="bfe1f-117">Um provedor de serviço que usa as seções de perfil adicionais pode armazenar as estruturas **MAPIUID** dessas seções de perfil em **PR_SERVICE_EXTRA_UIDS**, que permite o MAPI copiar as informações do serviço de mensagem adicionais.</span><span class="sxs-lookup"><span data-stu-id="bfe1f-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bfe1f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfe1f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bfe1f-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bfe1f-119">Header files</span></span>

<span data-ttu-id="bfe1f-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfe1f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfe1f-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bfe1f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="bfe1f-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bfe1f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="bfe1f-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bfe1f-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfe1f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfe1f-124">See also</span></span>



[<span data-ttu-id="bfe1f-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe1f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfe1f-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bfe1f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfe1f-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe1f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfe1f-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bfe1f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

