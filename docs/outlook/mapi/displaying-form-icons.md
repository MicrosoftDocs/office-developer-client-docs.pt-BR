---
title: Exibir ícones de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337041"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="16452-103">Exibir ícones de formulário</span><span class="sxs-lookup"><span data-stu-id="16452-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="16452-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16452-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16452-105">Ao exibir uma lista de mensagens em uma pasta, é útil para os seus usuários se você distinguir mensagens com classes de mensagens personalizadas da IPM padrão. Mensagens de observação.</span><span class="sxs-lookup"><span data-stu-id="16452-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="16452-106">As classes de mensagem personalizadas correspondem a servidores de formulários e os servidores de formulário fornecem ícones para serem representados por conta própria.</span><span class="sxs-lookup"><span data-stu-id="16452-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="16452-107">Você pode exibir esses ícones na lista de mensagens para alertar os usuários sobre a classe de mensagem de cada mensagem antes de o usuário abrir as mensagens.</span><span class="sxs-lookup"><span data-stu-id="16452-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="16452-108">Normalmente, o ícone na propriedade **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) do formulário é aquele que deve ser exibido na lista de mensagens.</span><span class="sxs-lookup"><span data-stu-id="16452-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="16452-109">Formulários também têm uma propriedade **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que pode ser exibida quando o formulário é minimizado em uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="16452-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="16452-110">**Para obter um ícone para uma classe de mensagem sem ativar o servidor de formulário para essa classe de mensagem**</span><span class="sxs-lookup"><span data-stu-id="16452-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="16452-111">Chame o método [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) para obter um ponteiro para uma interface [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="16452-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="16452-112">Chame o método [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obter um ponteiro para uma interface [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="16452-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="16452-113">Chame o método [IMAPIFormInfo:: MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obter uma alça de ícone.</span><span class="sxs-lookup"><span data-stu-id="16452-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="16452-114">O ícone pode ser exibido usando as APIs padrão do Win32.</span><span class="sxs-lookup"><span data-stu-id="16452-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="16452-115">Quando tiver o ícone de uma classe de mensagem, faça todos os esforços para armazenar em cache o ícone.</span><span class="sxs-lookup"><span data-stu-id="16452-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="16452-116">Os ícones de não cache afetam seriamente o desempenho dos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="16452-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="16452-117">Ao armazenar em cache ícones, cuidado com as relações entre as classes de mensagens e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="16452-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="16452-118">Por exemplo, se IPM. Observação. Meeting. Cancel a classe de mensagem ocorre para resolver de volta para IPM. Observe que, não presuma que todas as subclasses IPM. Observação deve usar o ícone de IPM. Observação.</span><span class="sxs-lookup"><span data-stu-id="16452-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

