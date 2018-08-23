---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da1a1403ce454eef03a4b1e965441b0c654a99aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563811"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="72e5b-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="72e5b-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="72e5b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72e5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72e5b-105">Especifica se o Microsoft Office Outlook deve examinar as pastas em um repositório e arquivá-los automaticamente.</span><span class="sxs-lookup"><span data-stu-id="72e5b-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="72e5b-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="72e5b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72e5b-107">Expostas no:</span><span class="sxs-lookup"><span data-stu-id="72e5b-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="72e5b-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="72e5b-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="72e5b-109">Criados por:</span><span class="sxs-lookup"><span data-stu-id="72e5b-109">Created by:</span></span>  <br/> |<span data-ttu-id="72e5b-110">Provedor de armazenamento</span><span class="sxs-lookup"><span data-stu-id="72e5b-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="72e5b-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="72e5b-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="72e5b-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="72e5b-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="72e5b-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="72e5b-113">Property type:</span></span>  <br/> |<span data-ttu-id="72e5b-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="72e5b-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="72e5b-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="72e5b-115">Access type:</span></span>  <br/> |<span data-ttu-id="72e5b-116">Somente leitura ou leitura/gravação, dependendo do provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="72e5b-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72e5b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="72e5b-117">Remarks</span></span>

<span data-ttu-id="72e5b-118">Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="72e5b-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="72e5b-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="72e5b-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="72e5b-120">Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="72e5b-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="72e5b-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="72e5b-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="72e5b-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="72e5b-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72e5b-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="72e5b-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="72e5b-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="72e5b-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="72e5b-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="72e5b-125">ulKind:</span></span>  <br/> |<span data-ttu-id="72e5b-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="72e5b-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="72e5b-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="72e5b-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="72e5b-128">L "ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="72e5b-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="72e5b-129">Essa propriedade permite que os provedores de armazenamento especificar se o Outlook deve examinar as pastas em um repositório e arquivá-los automaticamente.</span><span class="sxs-lookup"><span data-stu-id="72e5b-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="72e5b-130">Por padrão, essa propriedade não está exposta em um repositório, o que significa que o Outlook pode examinar pastas no repositório.</span><span class="sxs-lookup"><span data-stu-id="72e5b-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="72e5b-131">Se a propriedade é exposta, estes são os valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="72e5b-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="72e5b-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="72e5b-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="72e5b-133">O Outlook pode examinar pastas no repositório.</span><span class="sxs-lookup"><span data-stu-id="72e5b-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="72e5b-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="72e5b-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="72e5b-135">O Outlook não deve examinar as pastas no repositório.</span><span class="sxs-lookup"><span data-stu-id="72e5b-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="72e5b-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="72e5b-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="72e5b-137">Não permitir que os clientes alterar essa propriedade no repositório.</span><span class="sxs-lookup"><span data-stu-id="72e5b-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="72e5b-138">Observe que a constante **ASM_CLIENT_DO_NOT_CHANGE** é para referência futura e não está implementado no momento.</span><span class="sxs-lookup"><span data-stu-id="72e5b-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="72e5b-139">No momento, um repositório pode impedir que os clientes alterem esse sinalizador por codificar o valor que o repositório retorna para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="72e5b-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

