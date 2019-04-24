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
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326261"
---
# <a name="nofolderscan"></a><span data-ttu-id="63243-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="63243-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="63243-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63243-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63243-105">Especifica se o Microsoft Office Outlook deve examinar pastas de contatos em um repositório.</span><span class="sxs-lookup"><span data-stu-id="63243-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="63243-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="63243-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63243-107">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="63243-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="63243-108">[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="63243-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="63243-109">Criado por:</span><span class="sxs-lookup"><span data-stu-id="63243-109">Created by:</span></span>  <br/> |<span data-ttu-id="63243-110">Provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="63243-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="63243-111">AcEssado por:</span><span class="sxs-lookup"><span data-stu-id="63243-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="63243-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="63243-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="63243-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="63243-113">Property type:</span></span>  <br/> |<span data-ttu-id="63243-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63243-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63243-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="63243-115">Access type:</span></span>  <br/> |<span data-ttu-id="63243-116">Somente leitura ou leitura/gravação dependendo do provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="63243-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63243-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="63243-117">Remarks</span></span>

<span data-ttu-id="63243-118">Para fornecer qualquer uma das funcionalidades de armazenamento, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="63243-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="63243-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::](imapiprop-getprops.md)GetProps, o provedor de repositório também deve retornar o valor de propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="63243-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="63243-120">Os provedores de repositório podem chamar o [HrGetOneProp](hrgetoneprop.md) e o [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="63243-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="63243-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="63243-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="63243-122">Ao chamar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="63243-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63243-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="63243-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="63243-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="63243-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="63243-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="63243-125">ulKind:</span></span>  <br/> |<span data-ttu-id="63243-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="63243-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="63243-127">Tipo. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="63243-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="63243-128">L "NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="63243-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="63243-129">Esta propriedade oferece uma maneira de os provedores de loja especificarem para que o Outlook não examine as pastas de contatos no repositório para evitar a degradação de desempenho.</span><span class="sxs-lookup"><span data-stu-id="63243-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="63243-130">É usado em operações de mala direta durante as quais o Outlook verifica a presença e o valor dessa propriedade antes de iniciar a verificação.</span><span class="sxs-lookup"><span data-stu-id="63243-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="63243-131">Por padrão, essa propriedade não é exposta em um repositório, o que significa que o Outlook pode verificar a pasta de contatos no repositório.</span><span class="sxs-lookup"><span data-stu-id="63243-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="63243-132">Se a propriedade for exposta, estes são os valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="63243-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="63243-133">Zero (0): o Outlook pode realizar a verificação.</span><span class="sxs-lookup"><span data-stu-id="63243-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="63243-134">Valor diferente de zero: o Outlook não deve examinar pastas de contatos na loja.</span><span class="sxs-lookup"><span data-stu-id="63243-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

