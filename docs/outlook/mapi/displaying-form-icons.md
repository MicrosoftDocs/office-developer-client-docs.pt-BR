---
title: Exibindo ícones de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438628"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="0d452-103">Exibindo ícones de formulário</span><span class="sxs-lookup"><span data-stu-id="0d452-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="0d452-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d452-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d452-105">Ao exibir uma lista de mensagens em uma pasta, será útil para os usuários distinguir mensagens com classes de mensagens personalizadas do IPM padrão. Anotações de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0d452-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="0d452-106">As classes de mensagens personalizadas correspondem a servidores de formulário, e os servidores de formulário fornecem ícones para representarem a si mesmos.</span><span class="sxs-lookup"><span data-stu-id="0d452-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="0d452-107">Você pode exibir esses ícones na lista de mensagens para alertar os usuários sobre a classe de mensagens de cada mensagem antes que o usuário abra as mensagens.</span><span class="sxs-lookup"><span data-stu-id="0d452-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="0d452-108">Normalmente, o ícone na propriedade **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) do formulário é aquele que deve ser exibido na lista de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0d452-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="0d452-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span><span class="sxs-lookup"><span data-stu-id="0d452-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="0d452-110">**Para obter um ícone para uma classe de mensagem sem ativar o servidor de formulário para essa classe de mensagem**</span><span class="sxs-lookup"><span data-stu-id="0d452-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="0d452-111">Chame o [método IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obter um ponteiro para [um IMAPIFormContainer : interface IUnknown.](imapiformcontaineriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="0d452-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="0d452-112">Chame o [método IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obter um ponteiro para [uma interface IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="0d452-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="0d452-113">Chame o [método IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obter uma alça de ícone.</span><span class="sxs-lookup"><span data-stu-id="0d452-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="0d452-114">Em seguida, o ícone pode ser exibido usando APIs win32 padrão.</span><span class="sxs-lookup"><span data-stu-id="0d452-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="0d452-115">Depois de ter o ícone de uma classe de mensagem, faça todo o esforço para armazenar em cache esse ícone.</span><span class="sxs-lookup"><span data-stu-id="0d452-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="0d452-116">Não o armazenamento em cache de ícones afeta gravemente o desempenho dos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="0d452-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="0d452-117">Ao cache de ícones, tenha cuidado com as relações entre classes de mensagem e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="0d452-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="0d452-118">Por exemplo, se o IPM. Note.Meeting.Cancel message class happens to resolve back to IPM. Observação, não suponha que todas as subclasses do IPM. A observação deve usar o ícone do IPM. Observação.</span><span class="sxs-lookup"><span data-stu-id="0d452-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

