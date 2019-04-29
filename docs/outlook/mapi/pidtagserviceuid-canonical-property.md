---
title: Propriedade canônica PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426524"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="5ddd5-103">Propriedade canônica PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="5ddd5-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="5ddd5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ddd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ddd5-105">Contém a estrutura [MAPIUID](mapiuid.md) de um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5ddd5-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ddd5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5ddd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ddd5-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="5ddd5-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="5ddd5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5ddd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ddd5-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="5ddd5-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="5ddd5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5ddd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ddd5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5ddd5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5ddd5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5ddd5-112">Area:</span></span>  <br/> |<span data-ttu-id="5ddd5-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddd5-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ddd5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ddd5-114">Remarks</span></span>

<span data-ttu-id="5ddd5-115">Esta propriedade é calculada por objetos de seção de perfil MAPI em perfil.</span><span class="sxs-lookup"><span data-stu-id="5ddd5-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="5ddd5-116">MAPI usa-o para agrupar todos os provedores que pertencem ao mesmo serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5ddd5-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="5ddd5-117">Essa propriedade é fornecida como um parâmetro para a maioria dos métodos [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5ddd5-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="5ddd5-118">Ele não deve aparecer no MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="5ddd5-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5ddd5-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ddd5-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5ddd5-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5ddd5-120">Header files</span></span>

<span data-ttu-id="5ddd5-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5ddd5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ddd5-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5ddd5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ddd5-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5ddd5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5ddd5-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5ddd5-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ddd5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ddd5-125">See also</span></span>



[<span data-ttu-id="5ddd5-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ddd5-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="5ddd5-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddd5-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ddd5-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddd5-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ddd5-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5ddd5-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ddd5-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5ddd5-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

