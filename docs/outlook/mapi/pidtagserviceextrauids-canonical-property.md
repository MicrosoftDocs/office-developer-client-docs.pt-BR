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
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328725"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="e8592-103">Propriedade canônica PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="e8592-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="e8592-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8592-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8592-105">Contém uma lista de estruturas [MAPIUID](mapiuid.md) que identificam seções de perfil adicionais para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e8592-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8592-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e8592-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8592-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="e8592-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="e8592-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e8592-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8592-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="e8592-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="e8592-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e8592-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8592-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e8592-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e8592-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e8592-112">Area:</span></span>  <br/> |<span data-ttu-id="e8592-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="e8592-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8592-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8592-114">Remarks</span></span>

<span data-ttu-id="e8592-115">Novas seções de perfil podem ser criadas para cada filtro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e8592-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="e8592-116">Quando as informações sobre o serviço de mensagens são copiadas para outro perfil, é importante também copiar as seções de perfil adicionais para os filtros.</span><span class="sxs-lookup"><span data-stu-id="e8592-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="e8592-117">Um provedor de serviços que usa seções de perfil adicionais pode armazenar as estruturas **MAPIUID** dessas seções de perfil no **PR_SERVICE_EXTRA_UIDS**, que permite que o MAPI copie as informações adicionais do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e8592-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8592-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8592-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e8592-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8592-119">Header files</span></span>

<span data-ttu-id="e8592-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e8592-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8592-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e8592-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8592-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e8592-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e8592-123">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e8592-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8592-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8592-124">See also</span></span>



[<span data-ttu-id="e8592-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e8592-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8592-126">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e8592-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8592-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e8592-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8592-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e8592-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

