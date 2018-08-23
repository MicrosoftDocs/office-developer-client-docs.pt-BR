---
title: Expor pastas em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582592"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="7136d-103">Expor pastas em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="7136d-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="7136d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7136d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7136d-105">Provedor de armazenamento de cada mensagem deve apresentar uma interface de [IMAPIFolder](imapifolderimapicontainer.md) de nível superior para os aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="7136d-105">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications.</span></span> <span data-ttu-id="7136d-106">A pasta de nível superior corresponde ao repositório de toda a mensagem; Ele fornece acesso às pastas que os usuários veem como o conteúdo do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7136d-106">The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store.</span></span> <span data-ttu-id="7136d-107">Além disso, a pasta de nível superior é frequentemente usada como pasta para mensagens de CPI e como a pasta de recebimento padrão do qual ler relatórios são enviados.</span><span class="sxs-lookup"><span data-stu-id="7136d-107">In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent.</span></span> <span data-ttu-id="7136d-108">Provedores de armazenamento de mensagem também devem apresentar uma subárvore IPM — um conjunto de pastas usadas para armazenar mensagens IPM — para os aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="7136d-108">Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="7136d-109">Aplicativos cliente podem abrir a pasta de nível superior chamando o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com 0 e NULL para os parâmetros _cbEntryId_ e _lpEntryId_ , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7136d-109">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively.</span></span> <span data-ttu-id="7136d-110">Na maioria dos casos, no entanto, os aplicativos cliente abram o conjunto de pastas que contêm mensagens IPM.</span><span class="sxs-lookup"><span data-stu-id="7136d-110">In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="7136d-111">Para obter uma lista de pastas na árvore de pastas da loja mensagem IPM, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="7136d-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="7136d-112">Use sua sessão MAPI para chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="7136d-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="7136d-113">Use o ponteiro de banco de dados de mensagem resultante para chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7136d-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="7136d-114">Chame o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com o identificador de entrada para obter um ponteiro **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="7136d-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="7136d-115">Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obter um índice de conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="7136d-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="7136d-116">Chame o método [IMAPITable:: QueryRows](imapitable-queryrows.md) para listar as pastas na pasta de nível superior.</span><span class="sxs-lookup"><span data-stu-id="7136d-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="7136d-117">Clientes MAPI usam essas pastas para acessar outros objetos folder e objetos de mensagem no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7136d-117">MAPI clients use these folders to access other folder objects and message objects in the message store.</span></span> <span data-ttu-id="7136d-118">**IMAPIFolder**e sua interface pai [IMAPIContainer](imapicontainerimapiprop.md), contêm os métodos que seu provedor de armazenamento de mensagem deve implementar para preencher pastas com objetos de mensagem e responde a solicitações de cliente para operar nas mensagens.</span><span class="sxs-lookup"><span data-stu-id="7136d-118">**IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7136d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7136d-119">See also</span></span>



[<span data-ttu-id="7136d-120">Implementar pastas em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="7136d-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

