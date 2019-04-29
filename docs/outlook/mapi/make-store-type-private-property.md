---
title: Propriedade tornar tipo de repositório privado
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
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428540"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="c95d3-103">Propriedade tornar tipo de repositório privado</span><span class="sxs-lookup"><span data-stu-id="c95d3-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="c95d3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c95d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c95d3-105">Trata um repositório secundário como privado.</span><span class="sxs-lookup"><span data-stu-id="c95d3-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c95d3-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c95d3-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c95d3-107">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="c95d3-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="c95d3-108">[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="c95d3-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="c95d3-109">Criado por:</span><span class="sxs-lookup"><span data-stu-id="c95d3-109">Created by:</span></span>  <br/> |<span data-ttu-id="c95d3-110">Provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="c95d3-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="c95d3-111">AcEssado por:</span><span class="sxs-lookup"><span data-stu-id="c95d3-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="c95d3-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="c95d3-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="c95d3-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="c95d3-113">Property type:</span></span>  <br/> |<span data-ttu-id="c95d3-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c95d3-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c95d3-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="c95d3-115">Access type:</span></span>  <br/> |<span data-ttu-id="c95d3-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c95d3-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c95d3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c95d3-117">Remarks</span></span>

<span data-ttu-id="c95d3-118">Para fornecer qualquer uma das funcionalidades de armazenamento, o provedor de repositório deve implementar [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="c95d3-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="c95d3-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::](imapiprop-getprops.md)GetProps, o provedor de repositório também deve retornar o valor de propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="c95d3-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="c95d3-120">Os provedores de repositório podem chamar o [HrGetOneProp](hrgetoneprop.md) e o [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c95d3-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="c95d3-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="c95d3-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="c95d3-122">Ao chamar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="c95d3-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c95d3-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="c95d3-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="c95d3-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="c95d3-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="c95d3-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="c95d3-125">ulKind:</span></span>  <br/> |<span data-ttu-id="c95d3-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="c95d3-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="c95d3-127">Tipo. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="c95d3-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="c95d3-128">L "urn: schemas-microsoft-com: Office: Outlook # storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="c95d3-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="c95d3-129">Um provedor de repositório pode usar essa propriedade para que o Outlook a trate como particular quando for um repositório secundário para um usuário.</span><span class="sxs-lookup"><span data-stu-id="c95d3-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="c95d3-130">Por padrão, o Outlook trata um repositório secundário da mesma forma que um repositório de representante, e os itens no repositório secundário são privados somente se o usuário os marca especificamente como privado.</span><span class="sxs-lookup"><span data-stu-id="c95d3-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="c95d3-131">Quando essa propriedade é **true**, os itens excluídos de um repositório secundário são movidos para a pasta **itens excluídos** no repositório principal.</span><span class="sxs-lookup"><span data-stu-id="c95d3-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="c95d3-132">Os itens marcados como particulares não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="c95d3-132">Items marked private are not displayed.</span></span> <span data-ttu-id="c95d3-133">Rascunhos são armazenados na pasta Rascunhos no repositório principal.</span><span class="sxs-lookup"><span data-stu-id="c95d3-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="c95d3-134">Esta propriedade será ignorada se a versão do Outlook for anterior ao Microsoft Office Outlook 2003 Service Pack 1 ou se o valor for **false**.</span><span class="sxs-lookup"><span data-stu-id="c95d3-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

