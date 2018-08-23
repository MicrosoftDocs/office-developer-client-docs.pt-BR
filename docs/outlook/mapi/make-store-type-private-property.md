---
title: Propriedade para tornar privado o tipo de repositório
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2d927b00391725d8804e41b66b1ec8c384f98e7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568830"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="3c7c8-103">Propriedade para tornar privado o tipo de repositório</span><span class="sxs-lookup"><span data-stu-id="3c7c8-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="3c7c8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c7c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c7c8-105">Um repositório secundário a tratará como particular.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3c7c8-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="3c7c8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c7c8-107">Expostas no:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="3c7c8-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="3c7c8-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="3c7c8-109">Criados por:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-109">Created by:</span></span>  <br/> |<span data-ttu-id="3c7c8-110">Provedor de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3c7c8-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="3c7c8-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="3c7c8-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="3c7c8-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="3c7c8-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-113">Property type:</span></span>  <br/> |<span data-ttu-id="3c7c8-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3c7c8-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3c7c8-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-115">Access type:</span></span>  <br/> |<span data-ttu-id="3c7c8-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3c7c8-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c7c8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c7c8-117">Remarks</span></span>

<span data-ttu-id="3c7c8-118">Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="3c7c8-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="3c7c8-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="3c7c8-120">Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="3c7c8-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="3c7c8-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c7c8-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="3c7c8-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="3c7c8-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="3c7c8-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-125">ulKind:</span></span>  <br/> |<span data-ttu-id="3c7c8-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="3c7c8-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="3c7c8-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="3c7c8-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="3c7c8-128">L "urn: schemas-microsoft-com:office:outlook #storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="3c7c8-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="3c7c8-129">Um provedor de armazenamento pode usar essa propriedade para fazer com que o Outlook tratá-lo como privada, quando ele é um repositório secundário para um usuário.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="3c7c8-130">Por padrão, o Outlook trata um repositório secundário da mesma maneira como um repositório representante e itens no armazenamento secundário são particulares somente se o usuário marca-las especificamente como particular.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="3c7c8-131">Quando essa propriedade for **true**, os itens excluídos de um repositório secundário são movidos para a pasta **Itens excluídos** no repositório principal.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="3c7c8-132">Itens marcados como particulares não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-132">Items marked private are not displayed.</span></span> <span data-ttu-id="3c7c8-133">Os rascunhos são armazenados na pasta Rascunhos no repositório principal.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="3c7c8-134">Essa propriedade é ignorada se a versão do Outlook é anterior ao Microsoft Office Outlook 2003 Service Pack 1 ou se seu valor for **false**.</span><span class="sxs-lookup"><span data-stu-id="3c7c8-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

