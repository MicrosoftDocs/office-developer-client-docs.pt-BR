---
title: Selecionar uma pasta de recebimento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428414"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="9e15c-103">Selecionar uma pasta de recebimento</span><span class="sxs-lookup"><span data-stu-id="9e15c-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="9e15c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e15c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e15c-105">Uma pasta de recebimento é onde as mensagens de entrada de uma determinada classe são colocadas.</span><span class="sxs-lookup"><span data-stu-id="9e15c-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="9e15c-106">Para as mensagens IPM e de relatórios relacionados, o MAPI atribui a caixa de entrada como a pasta de recebimento padrão.</span><span class="sxs-lookup"><span data-stu-id="9e15c-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="9e15c-107">Para mensagens de relatório relacionadas e IPC, o MAPI atribui a pasta raiz do repositório de mensagens como a pasta de recebimento padrão.</span><span class="sxs-lookup"><span data-stu-id="9e15c-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="9e15c-108">Você pode alterar essas atribuições ou fazer atribuições adicionais para outras classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9e15c-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="9e15c-109">Fazer atribuições explícitas de pastas de recebimento para as classes de mensagens com suporte do cliente é opcional.</span><span class="sxs-lookup"><span data-stu-id="9e15c-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="9e15c-110">Quando uma classe de mensagens de entrada não tem uma pasta de recebimento atribuída, o provedor de armazenamento de mensagens usa automaticamente a pasta de recebimento da classe que corresponde ao prefixo mais longo possível da classe de entrada.</span><span class="sxs-lookup"><span data-stu-id="9e15c-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="9e15c-111">Por exemplo, se o cliente receber uma mensagem da classe IPM. Note. myDocument e a única pasta de recebimento estabelecida é a caixa de entrada de mensagens IPM, esta mensagem será colocada na caixa de entrada porque IPM. Note. mydocument deriva da classe base IPM.</span><span class="sxs-lookup"><span data-stu-id="9e15c-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="9e15c-112">Quando você estiver atribuindo uma pasta de recebimento para mensagens IPC, nunca use uma pasta da sub-árvore IPM.</span><span class="sxs-lookup"><span data-stu-id="9e15c-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="9e15c-113">Essas pastas devem ser reservadas apenas para mensagens IPM.</span><span class="sxs-lookup"><span data-stu-id="9e15c-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="9e15c-114">Use em vez de uma pasta contida na pasta raiz do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9e15c-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="9e15c-115">**Para criar uma pasta de recebimento para uma classe de mensagem IPM**</span><span class="sxs-lookup"><span data-stu-id="9e15c-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="9e15c-116">Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9e15c-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="9e15c-117">Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) com **PR_IPM_SUBTREE_ENTRYID** como o identificador de entrada para abrir a pasta raiz da sub-árvore IPM no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9e15c-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="9e15c-118">Chame [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="9e15c-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="9e15c-119">Chame [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para sua classe de mensagem IPM.</span><span class="sxs-lookup"><span data-stu-id="9e15c-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="9e15c-120">**Para criar uma pasta de recebimento para uma classe de mensagem de IPC**</span><span class="sxs-lookup"><span data-stu-id="9e15c-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="9e15c-121">Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo para abrir a pasta raiz do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9e15c-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="9e15c-122">Chame [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="9e15c-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="9e15c-123">Chame [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para sua classe de mensagens de IPC.</span><span class="sxs-lookup"><span data-stu-id="9e15c-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="9e15c-124">Atribua a pasta de recebimento que você usa para mensagens de relatórios relacionados.</span><span class="sxs-lookup"><span data-stu-id="9e15c-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="9e15c-125">Por exemplo, se o cliente receber IPM. Observação mensagens, configure uma pasta de recebimento para o futuro IPM. Mensagens de observação e a mesma pasta de recebimento para mensagens de relatórios. IPM.</span><span class="sxs-lookup"><span data-stu-id="9e15c-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

