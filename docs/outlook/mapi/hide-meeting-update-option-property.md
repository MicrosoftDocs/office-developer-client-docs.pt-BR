---
title: Ocultar propriedade de opção de atualização de reunião
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299507"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="51d74-103">Ocultar propriedade de opção de atualização de reunião</span><span class="sxs-lookup"><span data-stu-id="51d74-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="51d74-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51d74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51d74-105">Oculta a opção para enviar atualizações de reunião somente para participantes adicionados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="51d74-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="51d74-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="51d74-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51d74-107">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="51d74-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="51d74-108">[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="51d74-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="51d74-109">Criado por:</span><span class="sxs-lookup"><span data-stu-id="51d74-109">Created by:</span></span>  <br/> |<span data-ttu-id="51d74-110">Provedor de repositório</span><span class="sxs-lookup"><span data-stu-id="51d74-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="51d74-111">AcEssado por:</span><span class="sxs-lookup"><span data-stu-id="51d74-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="51d74-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="51d74-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="51d74-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="51d74-113">Property type:</span></span>  <br/> |<span data-ttu-id="51d74-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="51d74-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="51d74-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="51d74-115">Access type:</span></span>  <br/> |<span data-ttu-id="51d74-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="51d74-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51d74-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="51d74-117">Remarks</span></span>

<span data-ttu-id="51d74-118">Para fornecer qualquer uma das funcionalidades de armazenamento, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="51d74-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="51d74-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::](imapiprop-getprops.md)GetProps, o provedor de repositório também deve retornar o valor de propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="51d74-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="51d74-120">Os provedores de repositório podem chamar o [HrGetOneProp](hrgetoneprop.md) e o [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="51d74-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="51d74-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="51d74-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="51d74-122">Ao chamar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="51d74-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51d74-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="51d74-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="51d74-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="51d74-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="51d74-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="51d74-125">ulKind:</span></span>  <br/> |<span data-ttu-id="51d74-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="51d74-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="51d74-127">Tipo. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="51d74-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="51d74-128">L "urn: schemas-microsoft-com: Office: Outlook # allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="51d74-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="51d74-129">Um provedor de repositório que usa um servidor para enviar atualizações de reunião pode modificar a caixa de diálogo **Enviar atualização para participantes** .</span><span class="sxs-lookup"><span data-stu-id="51d74-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="51d74-130">Essa funcionalidade é útil porque quando o servidor envia uma atualização de reunião, o servidor não sabe quais participantes foram adicionados ou excluídos pelo usuário desde a solicitação de reunião inicial.</span><span class="sxs-lookup"><span data-stu-id="51d74-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="51d74-131">Quando essa propriedade é **true**, a opção **Enviar somente para os participantes adicionado ou excluído** não é exibida na caixa de diálogo **Enviar atualização para participantes** .</span><span class="sxs-lookup"><span data-stu-id="51d74-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="51d74-132">Esta propriedade será ignorada se a versão do Outlook for anterior ao Microsoft Office Outlook 2003 Service Pack 1 ou se o valor for **false**.</span><span class="sxs-lookup"><span data-stu-id="51d74-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

