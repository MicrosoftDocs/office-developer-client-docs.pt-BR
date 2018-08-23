---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581773"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="be429-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="be429-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="be429-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be429-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be429-105">Especifica se o Microsoft Office Outlook deve verificar pastas em um repositório, incluindo pastas de contatos, calendário e tarefas, na inicialização para preencher o painel de navegação.</span><span class="sxs-lookup"><span data-stu-id="be429-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="be429-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="be429-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be429-107">Expostas no:</span><span class="sxs-lookup"><span data-stu-id="be429-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="be429-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="be429-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="be429-109">Criados por:</span><span class="sxs-lookup"><span data-stu-id="be429-109">Created by:</span></span>  <br/> |<span data-ttu-id="be429-110">Provedor de armazenamento</span><span class="sxs-lookup"><span data-stu-id="be429-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="be429-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="be429-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="be429-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="be429-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="be429-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="be429-113">Property type:</span></span>  <br/> |<span data-ttu-id="be429-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="be429-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="be429-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="be429-115">Access type:</span></span>  <br/> |<span data-ttu-id="be429-116">Somente leitura ou leitura/gravação, dependendo do provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="be429-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be429-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="be429-117">Remarks</span></span>

<span data-ttu-id="be429-118">Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="be429-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="be429-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="be429-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="be429-120">Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="be429-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="be429-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="be429-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="be429-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="be429-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be429-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="be429-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="be429-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="be429-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="be429-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="be429-125">ulKind:</span></span>  <br/> |<span data-ttu-id="be429-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="be429-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="be429-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="be429-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="be429-128">L "CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="be429-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="be429-129">Essa propriedade oferece uma maneira de provedores de armazenamento especificar se o Outlook deve examinar várias pastas em um repositório.</span><span class="sxs-lookup"><span data-stu-id="be429-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="be429-130">Ele é usado na inicialização quando o Outlook verifica as pastas existentes em cada repositório aberto para preencher o painel de **navegação** ; Outlook verifica a presença e o valor dessa propriedade em um repositório antes de iniciar a varredura.</span><span class="sxs-lookup"><span data-stu-id="be429-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="be429-131">Por padrão, essa propriedade não está exposta em um repositório, o que significa que o Outlook pode examinar pastas no repositório.</span><span class="sxs-lookup"><span data-stu-id="be429-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="be429-132">Se a propriedade é exposta, estes são os valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="be429-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="be429-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="be429-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="be429-134">O Outlook pode examinar pastas no repositório.</span><span class="sxs-lookup"><span data-stu-id="be429-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="be429-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="be429-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="be429-136">O Outlook não deve examinar as pastas no repositório.</span><span class="sxs-lookup"><span data-stu-id="be429-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="be429-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="be429-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="be429-138">Não permitir que os clientes alterar essa propriedade no repositório.</span><span class="sxs-lookup"><span data-stu-id="be429-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="be429-139">Observe que a constante **CSM_CLIENT_DO_NOT_CHANGE** é para referência futura e não está implementado no momento.</span><span class="sxs-lookup"><span data-stu-id="be429-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="be429-140">No momento, um repositório pode impedir que os clientes alterem esse sinalizador por codificar o valor que o repositório retorna para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="be429-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

