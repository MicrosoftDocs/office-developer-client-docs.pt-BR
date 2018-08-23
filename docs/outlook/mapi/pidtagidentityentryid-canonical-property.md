---
title: Propriedade canônica PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a8810b6c39b909ebaa612496824150499cd15165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584839"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="44410-103">Propriedade canônica PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="44410-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="44410-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44410-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44410-105">Contém o identificador de entrada para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="44410-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44410-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="44410-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44410-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="44410-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="44410-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="44410-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44410-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="44410-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="44410-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="44410-110">Data type:</span></span>  <br/> |<span data-ttu-id="44410-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="44410-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="44410-112">Área:</span><span class="sxs-lookup"><span data-stu-id="44410-112">Area:</span></span>  <br/> |<span data-ttu-id="44410-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="44410-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44410-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="44410-114">Remarks</span></span>

<span data-ttu-id="44410-115">Essa propriedade não é exibido como uma propriedade em qualquer objeto, mas apenas como uma coluna em uma tabela de status.</span><span class="sxs-lookup"><span data-stu-id="44410-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="44410-116">Ele é parte da identidade do provedor de serviços expondo a linha da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="44410-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="44410-117">Normalmente, a identidade do provedor refere-se a sua conta no servidor, mas pode se referir a qualquer representação que o provedor define dentro do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="44410-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="44410-118">Esta propriedade é geralmente definida para o identificador de entrada do catálogo de endereço apropriado.</span><span class="sxs-lookup"><span data-stu-id="44410-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="44410-119">Um provedor de serviços que forneçam qualquer uma das propriedades identity deve fornecer aos todos eles.</span><span class="sxs-lookup"><span data-stu-id="44410-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="44410-120">Os provedores que pertencem ao mesmo serviço de mensagem devem expor os mesmos valores para as propriedades de identidade.</span><span class="sxs-lookup"><span data-stu-id="44410-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="44410-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="44410-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="44410-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44410-122">Header files</span></span>

<span data-ttu-id="44410-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44410-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="44410-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="44410-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="44410-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44410-125">Mapitags.h</span></span>
  
> <span data-ttu-id="44410-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="44410-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44410-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="44410-127">See also</span></span>



[<span data-ttu-id="44410-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="44410-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="44410-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="44410-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44410-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="44410-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44410-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="44410-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44410-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="44410-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

