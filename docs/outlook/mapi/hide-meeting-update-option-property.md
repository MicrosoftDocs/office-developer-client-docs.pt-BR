---
title: Ocultar a propriedade de opção de atualização de reunião
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766699"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="f8cf8-103">Ocultar a propriedade de opção de atualização de reunião</span><span class="sxs-lookup"><span data-stu-id="f8cf8-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="f8cf8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8cf8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f8cf8-105">Oculta a opção para enviar atualizações de reunião para apenas os participantes adicionados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f8cf8-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f8cf8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8cf8-107">Expostas no:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="f8cf8-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="f8cf8-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="f8cf8-109">Criados por:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-109">Created by:</span></span>  <br/> |<span data-ttu-id="f8cf8-110">Provedor de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f8cf8-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="f8cf8-111">Acessado por:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="f8cf8-112">Outlook e outros clientes</span><span class="sxs-lookup"><span data-stu-id="f8cf8-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="f8cf8-113">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-113">Property type:</span></span>  <br/> |<span data-ttu-id="f8cf8-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f8cf8-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f8cf8-115">Tipo de acesso:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-115">Access type:</span></span>  <br/> |<span data-ttu-id="f8cf8-116">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f8cf8-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8cf8-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="f8cf8-117">Remarks</span></span>

<span data-ttu-id="f8cf8-118">Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="f8cf8-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="f8cf8-119">Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="f8cf8-120">Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="f8cf8-121">Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="f8cf8-122">Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8cf8-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="f8cf8-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="f8cf8-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="f8cf8-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-125">ulKind:</span></span>  <br/> |<span data-ttu-id="f8cf8-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="f8cf8-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="f8cf8-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="f8cf8-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="f8cf8-128">L "urn: schemas-microsoft-com:office:outlook #allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="f8cf8-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="f8cf8-129">Um provedor de armazenamento que usa um servidor para enviar atualizações de reunião pode modificar a caixa de diálogo **Enviar atualização aos participantes** .</span><span class="sxs-lookup"><span data-stu-id="f8cf8-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="f8cf8-130">Essa funcionalidade é útil porque quando o servidor envia uma atualização de reunião, o servidor não saber quais participantes foram adicionados ou excluídos pelo usuário desde a solicitação de reunião inicial.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="f8cf8-131">Quando essa propriedade for **true**, a opção **Enviar atualização apenas aos participantes adicionados ou excluídos** não é exibida na caixa de diálogo **Enviar atualização aos participantes** .</span><span class="sxs-lookup"><span data-stu-id="f8cf8-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="f8cf8-132">Essa propriedade é ignorada se a versão do Outlook é anterior ao Microsoft Office Outlook 2003 Service Pack 1 ou se seu valor for **false**.</span><span class="sxs-lookup"><span data-stu-id="f8cf8-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

