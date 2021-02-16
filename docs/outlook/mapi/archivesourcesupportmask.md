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
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418089"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="b9452-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="b9452-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="b9452-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9452-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9452-105">Especifica se o Microsoft Office Outlook deve verificar pastas em um armazenamento e arquivar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b9452-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b9452-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b9452-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9452-107">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="b9452-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="b9452-108">[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="b9452-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="b9452-109">Criado por:</span><span class="sxs-lookup"><span data-stu-id="b9452-109">Created by:</span></span>  <br/> |<span data-ttu-id="b9452-110">Provedor da Loja</span><span class="sxs-lookup"><span data-stu-id="b9452-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="b9452-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="b9452-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="b9452-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="b9452-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="b9452-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="b9452-113">Property type:</span></span>  <br/> |<span data-ttu-id="b9452-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b9452-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b9452-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="b9452-115">Access type:</span></span>  <br/> |<span data-ttu-id="b9452-116">Somente leitura ou leitura/gravação, dependendo do provedor da loja</span><span class="sxs-lookup"><span data-stu-id="b9452-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9452-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9452-117">Remarks</span></span>

<span data-ttu-id="b9452-118">Para fornecer qualquer uma das funcionalidades do armazenamento, o provedor de armazenamento deve implementar [IMAPIProp : IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="b9452-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="b9452-119">Quando a marca de propriedade de qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor de propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="b9452-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="b9452-120">Os provedores da loja podem [chamar HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b9452-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="b9452-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="b9452-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="b9452-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a [estrutura MAPINAMEID](mapinameid.md) apontada pelo parâmetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="b9452-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9452-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="b9452-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="b9452-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b9452-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b9452-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="b9452-125">ulKind:</span></span>  <br/> |<span data-ttu-id="b9452-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b9452-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="b9452-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="b9452-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="b9452-128">L"ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="b9452-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="b9452-129">Essa propriedade permite que os provedores de armazenamento especifiquem se o Outlook deve verificar pastas em um armazenamento e arquivar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b9452-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="b9452-130">Por padrão, essa propriedade não é exposta em um armazenamento, o que significa que o Outlook pode verificar pastas no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9452-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="b9452-131">Se a propriedade for exposta, os valores possíveis serão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="b9452-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="b9452-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b9452-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="b9452-133">Outlook can scan folders on the store.</span><span class="sxs-lookup"><span data-stu-id="b9452-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="b9452-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="b9452-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="b9452-135">Outlook should not scan folders on the store.</span><span class="sxs-lookup"><span data-stu-id="b9452-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="b9452-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b9452-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="b9452-137">Não permita que os clientes alterem essa propriedade no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9452-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="b9452-138">Observe que a constante **ASM_CLIENT_DO_NOT_CHANGE** é para referência futura e não está implementada no momento.</span><span class="sxs-lookup"><span data-stu-id="b9452-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="b9452-139">Por enquanto, um armazenamento pode impedir que os clientes mudem esse sinalizador ao decodificar o valor que o armazenamento retorna para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b9452-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

