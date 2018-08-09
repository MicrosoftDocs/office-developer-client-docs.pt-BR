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
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770028"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="37387-103">Propriedade canônica PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="37387-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="37387-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="37387-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="37387-105">Contém o nome de um serviço de mensagem conforme definido pelo usuário no arquivo Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="37387-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37387-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="37387-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37387-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="37387-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="37387-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="37387-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37387-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="37387-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="37387-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="37387-110">Data type:</span></span>  <br/> |<span data-ttu-id="37387-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="37387-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="37387-112">Área:</span><span class="sxs-lookup"><span data-stu-id="37387-112">Area:</span></span>  <br/> |<span data-ttu-id="37387-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="37387-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37387-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="37387-114">Remarks</span></span>

<span data-ttu-id="37387-115">O nome contido nessas propriedades é específico para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="37387-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="37387-116">Ele proveniente da seção [serviços] em MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="37387-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="37387-117">Essas propriedades aparecem como uma coluna na tabela de serviço de mensagem e podem ser usadas para filtrar os serviços.</span><span class="sxs-lookup"><span data-stu-id="37387-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="37387-118">Porque ele é usado para identificar e filtrar os serviços, o valor não deve ser localizado.</span><span class="sxs-lookup"><span data-stu-id="37387-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37387-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37387-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="37387-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="37387-120">Header files</span></span>

<span data-ttu-id="37387-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37387-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="37387-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="37387-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="37387-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="37387-123">Mapitags.h</span></span>
  
> <span data-ttu-id="37387-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="37387-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37387-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="37387-125">See also</span></span>



[<span data-ttu-id="37387-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37387-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37387-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="37387-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37387-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="37387-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37387-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="37387-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

