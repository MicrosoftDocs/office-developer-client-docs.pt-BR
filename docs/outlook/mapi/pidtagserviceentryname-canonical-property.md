---
title: Propriedade canônica PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432468"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="dbf6c-103">Propriedade canônica PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="dbf6c-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="dbf6c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbf6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbf6c-105">Contém o nome da função de ponto de entrada para configuração de um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dbf6c-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dbf6c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dbf6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dbf6c-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="dbf6c-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="dbf6c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dbf6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dbf6c-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="dbf6c-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="dbf6c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dbf6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="dbf6c-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="dbf6c-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="dbf6c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dbf6c-112">Area:</span></span>  <br/> |<span data-ttu-id="dbf6c-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="dbf6c-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbf6c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbf6c-114">Remarks</span></span>

<span data-ttu-id="dbf6c-115">É recomendável que os implementadores de serviço de mensagens forneçam um ponto de entrada de serviço de mensagens, mas o ponto de entrada não é necessário.</span><span class="sxs-lookup"><span data-stu-id="dbf6c-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="dbf6c-116">No enTanto, o ponto de entrada deve ser fornecido somente se as propriedades de configuração relacionadas existirem.</span><span class="sxs-lookup"><span data-stu-id="dbf6c-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="dbf6c-117">Se essas propriedades não existirem, MAPI pressupõe que nenhum ponto de entrada seja fornecido.</span><span class="sxs-lookup"><span data-stu-id="dbf6c-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="dbf6c-118">A biblioteca de vínculo dinâmico (DLL) na qual a função de ponto de entrada aparece é nomeada pela propriedade **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dbf6c-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="dbf6c-119">Para obter mais informações sobre os pontos de entrada do serviço de mensagens, consulte [implementando uma função de ponto de entrada do provedor de serviços](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="dbf6c-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dbf6c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbf6c-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dbf6c-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dbf6c-121">Header files</span></span>

<span data-ttu-id="dbf6c-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dbf6c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="dbf6c-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dbf6c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="dbf6c-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="dbf6c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="dbf6c-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dbf6c-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dbf6c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbf6c-126">See also</span></span>



[<span data-ttu-id="dbf6c-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dbf6c-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dbf6c-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dbf6c-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dbf6c-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dbf6c-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dbf6c-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dbf6c-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

