---
title: Propriedade canônico de PidTagServiceUid
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770045"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="2c727-103">Propriedade canônico de PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="2c727-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="2c727-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c727-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c727-105">Contém a estrutura [MAPIUID](mapiuid.md) para um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2c727-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c727-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2c727-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c727-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="2c727-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="2c727-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2c727-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c727-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="2c727-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="2c727-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2c727-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c727-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2c727-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2c727-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c727-112">Area:</span></span>  <br/> |<span data-ttu-id="2c727-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="2c727-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c727-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="2c727-114">Remarks</span></span>

<span data-ttu-id="2c727-115">Essa propriedade é computada pelo MAPI em objetos de seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="2c727-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="2c727-116">MAPI utiliza para todos os provedores que pertencem ao mesmo serviço de mensagem de grupo.</span><span class="sxs-lookup"><span data-stu-id="2c727-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="2c727-117">Essa propriedade é fornecida como um parâmetro para a maioria dos métodos [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="2c727-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="2c727-118">Ele não deve aparecer em MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="2c727-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2c727-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c727-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2c727-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c727-120">Header files</span></span>

<span data-ttu-id="2c727-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c727-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c727-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2c727-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c727-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c727-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2c727-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2c727-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c727-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c727-125">See also</span></span>



[<span data-ttu-id="2c727-126">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c727-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="2c727-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c727-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c727-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2c727-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c727-129">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2c727-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c727-130">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="2c727-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

