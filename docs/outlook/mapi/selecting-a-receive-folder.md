---
title: Escolher uma pasta de recebimento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 87f8b4f4011e405d9848f12b5cae56f27fff1ab8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770337"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="00782-103">Escolher uma pasta de recebimento</span><span class="sxs-lookup"><span data-stu-id="00782-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="00782-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00782-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00782-105">Uma pasta de recebimento é onde as mensagens recebidas de uma determinada classe são colocadas.</span><span class="sxs-lookup"><span data-stu-id="00782-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="00782-106">Para IPM e mensagens de relatório relacionado, MAPI atribui a caixa de entrada, como o padrão de pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="00782-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="00782-107">Para CPI e mensagens de relatório relacionado, MAPI atribui a pasta raiz do armazenamento de mensagens, como o padrão de pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="00782-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="00782-108">Você pode alterar essas atribuições ou fazer atribuições adicionais para outras classes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="00782-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="00782-109">Fazendo explícitas receber atribuições de pasta para seu cliente com suporte a mensagem classes é opcional.</span><span class="sxs-lookup"><span data-stu-id="00782-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="00782-110">Quando uma classe de mensagem de entrada não tiver uma pasta de recebimento atribuída, o provedor de armazenamento de mensagem usa automaticamente a pasta de recebimento para a classe que corresponde ao prefixo possível mais longo da classe recebida.</span><span class="sxs-lookup"><span data-stu-id="00782-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="00782-111">Por exemplo, se o seu cliente recebe uma mensagem da classe IPM. Recebe Note.MyDocument e a única pasta que tenha sido estabelecida é a caixa de entrada para mensagens IPM, esta mensagem será colocada na caixa de entrada porque IPM. Note.MyDocument derivada da classe base IPM.</span><span class="sxs-lookup"><span data-stu-id="00782-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="00782-112">Quando você estiver atribuindo uma pasta de recebimento de mensagens de CPI, nunca use uma pasta de subárvore IPM.</span><span class="sxs-lookup"><span data-stu-id="00782-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="00782-113">Essas pastas devem ser reservadas para apenas para mensagens IPM.</span><span class="sxs-lookup"><span data-stu-id="00782-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="00782-114">Use uma pasta que está contida dentro da pasta raiz do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="00782-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="00782-115">**Para criar uma pasta de recebimento para uma classe de mensagem IPM**</span><span class="sxs-lookup"><span data-stu-id="00782-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="00782-116">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="00782-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="00782-117">Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) com **PR_IPM_SUBTREE_ENTRYID** como o identificador de entrada para abrir a pasta de raiz da subárvore IPM no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="00782-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="00782-118">[IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="00782-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="00782-119">Chame [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta à sua classe de mensagem IPM.</span><span class="sxs-lookup"><span data-stu-id="00782-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="00782-120">**Para criar uma pasta de recebimento para uma classe de mensagem CPI**</span><span class="sxs-lookup"><span data-stu-id="00782-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="00782-121">Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo para abrir a pasta raiz do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="00782-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="00782-122">[IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="00782-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="00782-123">Chame [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para a classe de mensagem do CPI.</span><span class="sxs-lookup"><span data-stu-id="00782-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="00782-124">Atribua a pasta de recebimento que você usa para mensagens para mensagens de relatório relacionado.</span><span class="sxs-lookup"><span data-stu-id="00782-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="00782-125">Por exemplo, se o seu cliente recebe IPM. Pasta de recebimento de mensagens de anotação, definir um para futura IPM. Mensagens de observação e o mesmo receberão a pasta para as mensagens futuras do Report.IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="00782-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

