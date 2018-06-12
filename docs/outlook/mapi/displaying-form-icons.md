---
title: Exibir ícones de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766432"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="a755e-103">Exibir ícones de formulário</span><span class="sxs-lookup"><span data-stu-id="a755e-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="a755e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a755e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a755e-105">Ao exibir uma lista de mensagens em uma pasta, é útil para os usuários se você distinguir mensagens com classes de mensagem personalizada do standard IPM. Observe as mensagens.</span><span class="sxs-lookup"><span data-stu-id="a755e-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="a755e-106">Classes de mensagem personalizada correspondem aos servidores de formulário, e os servidores de formulário fornecem ícones para representar a próprios.</span><span class="sxs-lookup"><span data-stu-id="a755e-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="a755e-107">Você pode exibir esses ícones na lista de mensagens para alertar os usuários à classe de mensagem de cada mensagem antes do usuário abrir as mensagens.</span><span class="sxs-lookup"><span data-stu-id="a755e-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="a755e-108">Normalmente, o ícone na propriedade de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) do formulário é aquela que deve ser exibida na lista de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a755e-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="a755e-109">Formulários também têm uma propriedade de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que pode ser exibida quando o formulário é minimizado em uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a755e-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="a755e-110">**Para obter um ícone para uma classe de mensagem sem ativar o servidor de formulário para essa classe de mensagem**</span><span class="sxs-lookup"><span data-stu-id="a755e-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="a755e-111">Chame o método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obter um ponteiro para uma [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="a755e-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="a755e-112">Chame o método [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obter um ponteiro para uma [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="a755e-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="a755e-113">Chame o método [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obter um identificador de ícone.</span><span class="sxs-lookup"><span data-stu-id="a755e-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="a755e-114">O ícone pode ser exibido usando APIs do Win32 padrão.</span><span class="sxs-lookup"><span data-stu-id="a755e-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a755e-115">Depois que você tiver o ícone de uma classe de mensagem, fazer todos os esforços para armazenar em cache nesse ícone.</span><span class="sxs-lookup"><span data-stu-id="a755e-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="a755e-116">Não cache ícones está seriamente afeta o desempenho dos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="a755e-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="a755e-117">Ao cache ícones, tenha cuidado das relações entre as classes de mensagens e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="a755e-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="a755e-118">Por exemplo, se o formulário IPM. Classe de mensagem Note.Meeting.Cancel acontece resolver novamente IPM. Observação, não presuma que todas as subclasses da IPM. Observação deve usar o ícone para IPM. Nota.</span><span class="sxs-lookup"><span data-stu-id="a755e-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

