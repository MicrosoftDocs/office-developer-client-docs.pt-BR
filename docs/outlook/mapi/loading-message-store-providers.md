---
title: Carregando provedores de armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307802"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="a0f19-103">Carregando provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="a0f19-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="a0f19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0f19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0f19-105">Quando um aplicativo cliente abre um armazenamento de mensagens, o MAPI carrega a DLL do provedor de armazenamento de mensagens na memória.</span><span class="sxs-lookup"><span data-stu-id="a0f19-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="a0f19-106">Depois que o MAPI carrega a DLL, ocorre uma sequência muito específica de chamadas de método entre o provedor do armazenamento de mensagens e o MAPI.</span><span class="sxs-lookup"><span data-stu-id="a0f19-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="a0f19-107">Essa sequência de chamada de método permite que MAPI obter [IMSProvider de](imsprovideriunknown.md)nível superior : IUnknown , [IMSLogon : IUnknown](imslogoniunknown.md)e [IMsgStore : interfaces IMAPIProp](imsgstoreimapiprop.md) e permite que o provedor de repositório de mensagens obter um objeto de suporte MAPI.</span><span class="sxs-lookup"><span data-stu-id="a0f19-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="a0f19-108">Após a sequência de chamada, o provedor de armazenamento de mensagens deve estar pronto para aceitar logons de clientes.</span><span class="sxs-lookup"><span data-stu-id="a0f19-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="a0f19-109">A sequência de chamada quando uma DLL do provedor de mensagens é carregada é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="a0f19-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="a0f19-110">O cliente chama [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="a0f19-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="a0f19-111">Se o armazenamento de mensagens ainda não estiver aberto, o MAPI carregará a DLL do provedor de armazenamento e chamará o ponto de entrada [MSProviderInit](msproviderinit.md) da DLL.</span><span class="sxs-lookup"><span data-stu-id="a0f19-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="a0f19-112">Se o armazenamento de mensagens já estiver aberto, o MAPI ignorará as etapas 2 e 3 e usará a interface [IMSProvider : IUnknown](imsprovideriunknown.md) existente para concluir a etapa 4.</span><span class="sxs-lookup"><span data-stu-id="a0f19-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="a0f19-113">**MSProviderInit** cria e retorna **um objeto IMSProvider.**</span><span class="sxs-lookup"><span data-stu-id="a0f19-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="a0f19-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span><span class="sxs-lookup"><span data-stu-id="a0f19-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="a0f19-115">**IMSProvider::Logon** cria e retorna um [IMSLogon : interface IUnknown](imslogoniunknown.md) e [IMsgStore : interface IMAPIProp](imsgstoreimapiprop.md) e chama o método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) em seu [IMAPISupport : interface IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a0f19-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="a0f19-116">Se o identificador de entrada do repositório de mensagens do cliente se referir a um repositório de mensagens que já está aberto, o provedor de repositório de mensagens poderá retornar interfaces **IMSLogon** e **IMsgStore** existentes e não precisará chamar **AddRef** em seu objeto de suporte.</span><span class="sxs-lookup"><span data-stu-id="a0f19-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="a0f19-117">Se o cliente não definiu o sinalizador MAPI_NO_MAIL quando fez logoff e não definiu o MDB_NO_MAIL na etapa 1, o MAPI fornece o identificador de entrada do armazenamento de mensagens para o spooler MAPI para que o spooler MAPI possa fazer logoff no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a0f19-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="a0f19-118">MAPI returns the **IMsgStore** interface to the client.</span><span class="sxs-lookup"><span data-stu-id="a0f19-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="a0f19-119">O spooler MAPI chama [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="a0f19-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="a0f19-120">**IMSProvider::SpoolerLogon** retorna as mesmas interfaces **IMSLogon** e **IMsgStore** da etapa 5.</span><span class="sxs-lookup"><span data-stu-id="a0f19-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a0f19-121">Se a chamada de logon para o provedor de armazenamento de mensagens falhar porque uma senha incorreta foi fornecida e o provedor do armazenamento de mensagens não puder exibir uma interface para solicitar a senha correta, ela deverá retornar MAPI_E_FAILONEPROVIDER do método **IMSProvider::Logon.**</span><span class="sxs-lookup"><span data-stu-id="a0f19-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="a0f19-122">Isso permitirá que os clientes solicitam ao usuário uma senha para tentar fazer logon no provedor de armazenamento de mensagens novamente, em vez de fazer com que o MAPI falhe no provedor de toda a sessão.</span><span class="sxs-lookup"><span data-stu-id="a0f19-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0f19-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0f19-123">See also</span></span>



[<span data-ttu-id="a0f19-124">Desenvolver um provedor de repositórios de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="a0f19-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

