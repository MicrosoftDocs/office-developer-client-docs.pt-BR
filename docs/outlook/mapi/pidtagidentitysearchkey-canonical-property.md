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
ms.openlocfilehash: 28c269db15d0c0a81950a61ee9e6629ad067b789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769318"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="0f681-103">Propriedade canônica PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="0f681-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="0f681-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f681-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f681-105">Contém a chave de pesquisa para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0f681-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f681-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0f681-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f681-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="0f681-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="0f681-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0f681-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f681-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="0f681-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="0f681-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0f681-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f681-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f681-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f681-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0f681-112">Area:</span></span>  <br/> |<span data-ttu-id="0f681-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="0f681-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f681-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f681-114">Remarks</span></span>

<span data-ttu-id="0f681-115">Essa propriedade não é exibido como uma propriedade em qualquer objeto, mas apenas como uma coluna em uma tabela de status.</span><span class="sxs-lookup"><span data-stu-id="0f681-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="0f681-116">Ele é parte da identidade do provedor de serviços expondo a linha da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="0f681-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="0f681-117">Normalmente, a identidade do provedor refere-se a sua conta no servidor, mas pode se referir a qualquer representação que o provedor define dentro do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0f681-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="0f681-118">Um provedor de serviços que forneçam qualquer uma das propriedades identity deve fornecer aos todos eles.</span><span class="sxs-lookup"><span data-stu-id="0f681-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="0f681-119">Os provedores que pertencem ao mesmo serviço de mensagem devem expor os mesmos valores para as propriedades de identidade.</span><span class="sxs-lookup"><span data-stu-id="0f681-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f681-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f681-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0f681-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f681-121">Header files</span></span>

<span data-ttu-id="0f681-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f681-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f681-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0f681-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f681-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f681-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0f681-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0f681-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f681-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f681-126">See also</span></span>



[<span data-ttu-id="0f681-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="0f681-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="0f681-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0f681-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f681-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0f681-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f681-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0f681-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f681-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0f681-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

