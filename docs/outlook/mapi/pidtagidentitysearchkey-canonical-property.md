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
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565141"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="3087c-103">Propriedade canônica PidTagIdentitySearchKey</span><span class="sxs-lookup"><span data-stu-id="3087c-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="3087c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3087c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3087c-105">Contém a chave de pesquisa para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3087c-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3087c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3087c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3087c-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="3087c-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="3087c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3087c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3087c-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="3087c-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="3087c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3087c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3087c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3087c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3087c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3087c-112">Area:</span></span>  <br/> |<span data-ttu-id="3087c-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="3087c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3087c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3087c-114">Remarks</span></span>

<span data-ttu-id="3087c-115">Essa propriedade não é exibido como uma propriedade em qualquer objeto, mas apenas como uma coluna em uma tabela de status.</span><span class="sxs-lookup"><span data-stu-id="3087c-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="3087c-116">Ele é parte da identidade do provedor de serviços expondo a linha da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="3087c-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="3087c-117">Normalmente, a identidade do provedor refere-se a sua conta no servidor, mas pode se referir a qualquer representação que o provedor define dentro do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3087c-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="3087c-118">Um provedor de serviços que forneçam qualquer uma das propriedades identity deve fornecer aos todos eles.</span><span class="sxs-lookup"><span data-stu-id="3087c-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="3087c-119">Os provedores que pertencem ao mesmo serviço de mensagem devem expor os mesmos valores para as propriedades de identidade.</span><span class="sxs-lookup"><span data-stu-id="3087c-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3087c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3087c-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3087c-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3087c-121">Header files</span></span>

<span data-ttu-id="3087c-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3087c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3087c-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3087c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3087c-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3087c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3087c-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3087c-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3087c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3087c-126">See also</span></span>



[<span data-ttu-id="3087c-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="3087c-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="3087c-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3087c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3087c-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3087c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3087c-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3087c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3087c-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3087c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

