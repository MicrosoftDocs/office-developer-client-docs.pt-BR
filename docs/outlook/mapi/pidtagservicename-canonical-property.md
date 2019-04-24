---
title: Propriedade canônica PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359476"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="7d757-103">Propriedade canônica PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="7d757-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="7d757-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d757-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d757-105">Contém o nome de um serviço de mensagens, conforme definido pelo usuário no arquivo MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="7d757-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d757-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7d757-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d757-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="7d757-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="7d757-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7d757-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d757-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="7d757-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="7d757-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7d757-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d757-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d757-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7d757-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7d757-112">Area:</span></span>  <br/> |<span data-ttu-id="7d757-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="7d757-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d757-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d757-114">Remarks</span></span>

<span data-ttu-id="7d757-115">O nome contido nessas propriedades é específico para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7d757-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="7d757-116">Ele vem da seção [serviços] no MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="7d757-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="7d757-117">Essas propriedades aparecem como uma coluna na tabela de serviço de mensagens e podem ser usadas para filtrar serviços.</span><span class="sxs-lookup"><span data-stu-id="7d757-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="7d757-118">Como ele é usado para identificar e filtrar serviços, o valor não deve ser localizado.</span><span class="sxs-lookup"><span data-stu-id="7d757-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d757-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d757-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7d757-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7d757-120">Header files</span></span>

<span data-ttu-id="7d757-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7d757-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d757-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7d757-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d757-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7d757-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7d757-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7d757-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d757-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d757-125">See also</span></span>



[<span data-ttu-id="7d757-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d757-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d757-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7d757-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d757-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7d757-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d757-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7d757-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

