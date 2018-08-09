---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3477104cc254ea5f22158b9791d7fd3bd776d819
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768152"
---
# <a name="nofolderscan"></a><span data-ttu-id="62a9e-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="62a9e-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="62a9e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62a9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62a9e-105">Especifica se o Microsoft Office Outlook deve verificar as pastas de contatos em um repositório.</span><span class="sxs-lookup"><span data-stu-id="62a9e-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="62a9e-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="62a9e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62a9e-107">Expostas no:</span><span class="sxs-lookup"><span data-stu-id="62a9e-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="62a9e-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="62a9e-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="62a9e-109">Criados por:</span><span class="sxs-lookup"><span data-stu-id="62a9e-109">Created by:</span></span>  <br/> |<span data-ttu-id="62a9e-110">Provedor de armazenamento</span><span class="sxs-lookup"><span data-stu-id="62a9e-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="62a9e-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="62a9e-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="62a9e-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="62a9e-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="62a9e-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="62a9e-113">Property type:</span></span>  <br/> |<span data-ttu-id="62a9e-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="62a9e-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="62a9e-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="62a9e-115">Access type:</span></span>  <br/> |<span data-ttu-id="62a9e-116">Somente leitura ou leitura/gravação, dependendo do provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="62a9e-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62a9e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="62a9e-117">Remarks</span></span>

<span data-ttu-id="62a9e-118">Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="62a9e-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="62a9e-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="62a9e-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="62a9e-120">Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="62a9e-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="62a9e-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="62a9e-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="62a9e-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="62a9e-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62a9e-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="62a9e-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="62a9e-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="62a9e-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="62a9e-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="62a9e-125">ulKind:</span></span>  <br/> |<span data-ttu-id="62a9e-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="62a9e-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="62a9e-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="62a9e-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="62a9e-128">L "NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="62a9e-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="62a9e-129">Essa propriedade oferece uma maneira de provedores de armazenamento especificar como o Outlook não para examinar as pastas de contatos no repositório de para evitar a diminuição do desempenho.</span><span class="sxs-lookup"><span data-stu-id="62a9e-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="62a9e-130">Ele é usado nas operações de mala direta durante o qual o Outlook verifica a presença e o valor dessa propriedade antes de iniciar a varredura.</span><span class="sxs-lookup"><span data-stu-id="62a9e-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="62a9e-131">Por padrão, essa propriedade não está exposta em um repositório, o que significa que o Outlook pode examinar a pasta de contatos no repositório.</span><span class="sxs-lookup"><span data-stu-id="62a9e-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="62a9e-132">Se a propriedade é exposta, estes são os valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="62a9e-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="62a9e-133">Zero (0): Outlook pode executar a verificação.</span><span class="sxs-lookup"><span data-stu-id="62a9e-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="62a9e-134">Valor diferente de zero: o Outlook não deve examinar as pastas de contatos no repositório.</span><span class="sxs-lookup"><span data-stu-id="62a9e-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

