---
title: Acessar um repositório no servidor remoto quando o Outlook estiver no modo cache do Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Última modificação: 02 de julho de 2012'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299059"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="659e7-103">Acessar um repositório no servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="659e7-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="659e7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="659e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="659e7-105">Este tópico contém um exemplo de código em C++ que mostra como usar o sinalizador **MAPI_NO_CACHE** para abrir uma pasta ou uma mensagem em um repositório de mensagens no servidor remoto quando o Microsoft Office Outlook estiver no modo cache do Exchange.</span><span class="sxs-lookup"><span data-stu-id="659e7-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="659e7-106">O modo cache do Exchange permite que o Outlook use uma cópia local da caixa de correio de um usuário enquanto o Outlook mantém uma conexão online com uma cópia remota da caixa de correio do usuário no servidor Exchange remoto.</span><span class="sxs-lookup"><span data-stu-id="659e7-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="659e7-107">Quando o Outlook está sendo executado no modo cache do Exchange, por padrão, as soluções MAPI que fazem logon na mesma sessão também são conectadas ao repositório de mensagens em cache.</span><span class="sxs-lookup"><span data-stu-id="659e7-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="659e7-108">Quaisquer dados que sejam acessados e quaisquer alterações feitas serão feitas em relação à cópia local da caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="659e7-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="659e7-109">Um cliente ou um provedor de serviços pode substituir a conexão com o repositório de mensagens local e abrir uma mensagem ou uma pasta no repositório remoto Configurando o bit para **MAPI_NO_CACHE** no parâmetro *Parâmetroulflags* ao chamar **[IMsgStore:: OpenEntry](imsgstore-openentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="659e7-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="659e7-110">O exemplo de código a seguir mostra como chamar **IMsgStore:: OpenEntry** com o sinalizador **MAPI_NO_CACHE** definido no parâmetro *parâmetroulflags* para abrir a pasta raiz no repositório de mensagens remoto.</span><span class="sxs-lookup"><span data-stu-id="659e7-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

<span data-ttu-id="659e7-111">Se você abriu o repositório de mensagens com o sinalizador **MDB_ONLINE** no servidor remoto, não será necessário usar o sinalizador **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="659e7-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="659e7-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="659e7-112">See also</span></span>

- [<span data-ttu-id="659e7-113">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="659e7-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="659e7-114">Abrir o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="659e7-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="659e7-115">Gerenciar mensagens em um OST sem solicitar uma sincronização do modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="659e7-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

