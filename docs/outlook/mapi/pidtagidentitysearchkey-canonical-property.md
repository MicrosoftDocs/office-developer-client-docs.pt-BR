---
title: Propriedade canônica PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423745"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="fe723-103">Propriedade canônica PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="fe723-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="fe723-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe723-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe723-105">Contém a chave de pesquisa para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fe723-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe723-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fe723-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe723-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="fe723-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="fe723-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fe723-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe723-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="fe723-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="fe723-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fe723-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe723-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fe723-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fe723-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fe723-112">Area:</span></span>  <br/> |<span data-ttu-id="fe723-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="fe723-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe723-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe723-114">Remarks</span></span>

<span data-ttu-id="fe723-115">Essa propriedade não aparece como uma propriedade em qualquer objeto, mas somente como uma coluna em uma tabela de status.</span><span class="sxs-lookup"><span data-stu-id="fe723-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="fe723-116">Ele faz parte da identidade do provedor de serviços que expõe a linha da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="fe723-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="fe723-117">A identidade do provedor geralmente se refere à sua conta no servidor, mas pode se referir a qualquer representação que o provedor define no sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fe723-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="fe723-118">Um provedor de serviços que forneça qualquer uma das propriedades de identidade deve fornecer todos eles.</span><span class="sxs-lookup"><span data-stu-id="fe723-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="fe723-119">Os provedores que pertencem ao mesmo serviço de mensagens devem expor os mesmos valores para as propriedades de identidade.</span><span class="sxs-lookup"><span data-stu-id="fe723-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fe723-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe723-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fe723-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe723-121">Header files</span></span>

<span data-ttu-id="fe723-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fe723-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe723-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fe723-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe723-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fe723-124">Mapitags.h</span></span>
  
> <span data-ttu-id="fe723-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fe723-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe723-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe723-126">See also</span></span>



[<span data-ttu-id="fe723-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="fe723-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="fe723-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fe723-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe723-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fe723-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe723-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fe723-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe723-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fe723-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

