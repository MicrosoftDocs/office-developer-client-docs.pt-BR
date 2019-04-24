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
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333044"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="4e98f-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="4e98f-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="4e98f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e98f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e98f-105">Especifica se o Microsoft Office Outlook deve verificar pastas em um repositório, incluindo as pastas contatos, calendário e tarefas, na inicialização para preencher o painel de navegação.</span><span class="sxs-lookup"><span data-stu-id="4e98f-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4e98f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4e98f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e98f-107">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="4e98f-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="4e98f-108">[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="4e98f-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="4e98f-109">Criado por:</span><span class="sxs-lookup"><span data-stu-id="4e98f-109">Created by:</span></span>  <br/> |<span data-ttu-id="4e98f-110">Provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="4e98f-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="4e98f-111">AcEssado por:</span><span class="sxs-lookup"><span data-stu-id="4e98f-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="4e98f-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="4e98f-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="4e98f-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="4e98f-113">Property type:</span></span>  <br/> |<span data-ttu-id="4e98f-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4e98f-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4e98f-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="4e98f-115">Access type:</span></span>  <br/> |<span data-ttu-id="4e98f-116">Somente leitura ou leitura/gravação dependendo do provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="4e98f-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e98f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e98f-117">Remarks</span></span>

<span data-ttu-id="4e98f-118">Para fornecer qualquer uma das funcionalidades de armazenamento, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="4e98f-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="4e98f-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::](imapiprop-getprops.md)GetProps, o provedor de repositório também deve retornar o valor de propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="4e98f-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="4e98f-120">Os provedores de repositório podem chamar o [HrGetOneProp](hrgetoneprop.md) e o [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4e98f-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="4e98f-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="4e98f-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="4e98f-122">Ao chamar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="4e98f-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e98f-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="4e98f-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="4e98f-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4e98f-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4e98f-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="4e98f-125">ulKind:</span></span>  <br/> |<span data-ttu-id="4e98f-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="4e98f-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="4e98f-127">Tipo. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="4e98f-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="4e98f-128">L "CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="4e98f-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="4e98f-129">Essa propriedade oferece uma maneira de os provedores de repositório especificarem se o Outlook deve examinar várias pastas em um repositório.</span><span class="sxs-lookup"><span data-stu-id="4e98f-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="4e98f-130">Ele é usado na inicialização quando o Outlook verifica pastas existentes em cada repositório aberto para preencher o painel de **navegação** ; O Outlook verifica a presença e o valor dessa propriedade em um repositório antes de iniciar a verificação.</span><span class="sxs-lookup"><span data-stu-id="4e98f-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="4e98f-131">Por padrão, essa propriedade não é exposta em um repositório, o que significa que o Outlook pode examinar pastas na loja.</span><span class="sxs-lookup"><span data-stu-id="4e98f-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="4e98f-132">Se a propriedade for exposta, estes são os valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="4e98f-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="4e98f-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="4e98f-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="4e98f-134">O Outlook pode examinar pastas na loja.</span><span class="sxs-lookup"><span data-stu-id="4e98f-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="4e98f-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="4e98f-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="4e98f-136">O Outlook não deve verificar pastas na loja.</span><span class="sxs-lookup"><span data-stu-id="4e98f-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="4e98f-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="4e98f-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="4e98f-138">Não permita que os clientes alterem essa propriedade na loja.</span><span class="sxs-lookup"><span data-stu-id="4e98f-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="4e98f-139">Observe que a constante **CSM_CLIENT_DO_NOT_CHANGE** é para referência futura e não está implementada no momento.</span><span class="sxs-lookup"><span data-stu-id="4e98f-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="4e98f-140">Por enquanto, um repositório pode impedir que os clientes alterem esse sinalizador codificando o valor que o repositório retorna para esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="4e98f-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

