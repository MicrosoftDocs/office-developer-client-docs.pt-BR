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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436797"
---
# <a name="nofolderscan"></a><span data-ttu-id="5988a-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="5988a-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="5988a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5988a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5988a-105">Especifica se o Microsoft Office Outlook deve verificar pastas de Contatos em um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5988a-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5988a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5988a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5988a-107">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="5988a-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="5988a-108">[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="5988a-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="5988a-109">Criado por:</span><span class="sxs-lookup"><span data-stu-id="5988a-109">Created by:</span></span>  <br/> |<span data-ttu-id="5988a-110">Provedor da Loja</span><span class="sxs-lookup"><span data-stu-id="5988a-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="5988a-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="5988a-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="5988a-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="5988a-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="5988a-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="5988a-113">Property type:</span></span>  <br/> |<span data-ttu-id="5988a-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5988a-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5988a-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="5988a-115">Access type:</span></span>  <br/> |<span data-ttu-id="5988a-116">Somente leitura ou leitura/gravação, dependendo do provedor da loja</span><span class="sxs-lookup"><span data-stu-id="5988a-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5988a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5988a-117">Remarks</span></span>

<span data-ttu-id="5988a-118">Para fornecer qualquer uma das funcionalidades do armazenamento, o provedor de armazenamento deve implementar [IMAPIProp : IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="5988a-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="5988a-119">Quando a marca de propriedade de qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor de propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="5988a-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="5988a-120">Os provedores da loja podem [chamar HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5988a-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="5988a-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="5988a-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="5988a-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a [estrutura MAPINAMEID](mapinameid.md) apontada pelo parâmetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="5988a-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5988a-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="5988a-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="5988a-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5988a-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5988a-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="5988a-125">ulKind:</span></span>  <br/> |<span data-ttu-id="5988a-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="5988a-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="5988a-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="5988a-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="5988a-128">L"NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="5988a-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="5988a-129">Essa propriedade fornece uma maneira para os provedores de armazenamento especificarem para o Outlook não verificar pastas de contatos no armazenamento para evitar a degradação do desempenho.</span><span class="sxs-lookup"><span data-stu-id="5988a-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="5988a-130">Ele é usado em operações de mala direta durante as quais o Outlook verifica a presença e o valor dessa propriedade antes de iniciar a verificação.</span><span class="sxs-lookup"><span data-stu-id="5988a-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="5988a-131">Por padrão, essa propriedade não é exposta em um armazenamento, o que significa que o Outlook pode verificar a pasta Contatos no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5988a-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="5988a-132">Se a propriedade for exposta, os valores possíveis serão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="5988a-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="5988a-133">Zero (0): o Outlook pode realizar a verificação.</span><span class="sxs-lookup"><span data-stu-id="5988a-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="5988a-134">Valor diferente de zero: o Outlook não deve verificar pastas de contatos no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5988a-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

