---
title: Expor pastas em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 457620dd0f805e78d12fc8feba09f8fc8aedc554
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341346"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="a9450-103">Expor pastas em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="a9450-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="a9450-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9450-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9450-105">Todo provedor de repositórios de mensagens deve apresentar uma interface [IMAPIFolder](imapifolderimapicontainer.md) de nível superior para aplicativos clientes.</span><span class="sxs-lookup"><span data-stu-id="a9450-105">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications.</span></span> <span data-ttu-id="a9450-106">A pasta de nível superior corresponde ao a todo o repositórios de mensagens; ela fornece acesso às pastas que os usuários veem como o conteúdo do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9450-106">The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store.</span></span> <span data-ttu-id="a9450-107">Além disso, a pasta de nível superior é usada com frequência como pasta de recebimento padrão para mensagens IPC, e como a pasta da qual os relatórios de leitura são enviados.</span><span class="sxs-lookup"><span data-stu-id="a9450-107">In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent.</span></span> <span data-ttu-id="a9450-108">Os provedores de repositórios de mensagens também devem apresentar uma subárvore IPM — um conjunto de pastas usado para guardar mensagens IPM — para aplicativos clientes.</span><span class="sxs-lookup"><span data-stu-id="a9450-108">Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="a9450-109">Os aplicativos cliente podem abrir a pasta de nível superior chamando o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com 0 e NULO para os parâmetros _cbEntryId_ e _lpEntryId_, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a9450-109">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively.</span></span> <span data-ttu-id="a9450-110">Na maioria dos casos, no entanto, os aplicativos clientes abrem o conjunto de pastas que contém mensagens IPM.</span><span class="sxs-lookup"><span data-stu-id="a9450-110">In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="a9450-111">Para obter uma lista de pastas na árvore de pastas IPM do repositório de mensagens, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="a9450-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="a9450-112">Usar a sessão MAPI para chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="a9450-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="a9450-113">Use o ponteiro do banco de dados resultante mensagem para chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a9450-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="a9450-114">Chame o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com o identificador de entrada para obter um ponteiro **IMAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="a9450-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="a9450-115">Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obter uma tabela do conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="a9450-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="a9450-116">Chame o método [IMAPITable::QueryRows](imapitable-queryrows.md) para listar as pastas na pasta de nível superior.</span><span class="sxs-lookup"><span data-stu-id="a9450-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="a9450-117">Os clientes MAPI usam essas pastas para acessar outros objetos de pasta e objetos de mensagem no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9450-117">MAPI clients use these folders to access other folder objects and message objects in the message store.</span></span> <span data-ttu-id="a9450-118">**IMAPIFolder**e sua interface do pai [IMAPIContainer](imapicontainerimapiprop.md) contêm os métodos que seu provedor de repositório de mensagens precisa implementar para preencher as pastas com objetos de mensagem e responder a solicitações de clientes para operar nas mensagens.</span><span class="sxs-lookup"><span data-stu-id="a9450-118">**IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9450-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9450-119">See also</span></span>



[<span data-ttu-id="a9450-120">Implementar pastas em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="a9450-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

