---
title: Carregar provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398392"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="55c2a-103">Carregar provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="55c2a-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="55c2a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55c2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55c2a-105">Quando um aplicativo cliente abre um armazenamento de mensagens, MAPI carrega a DLL do provedor de repositório a mensagem na memória.</span><span class="sxs-lookup"><span data-stu-id="55c2a-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="55c2a-106">Depois de MAPI carrega a DLL, uma sequência muito específica de chamadas de método ocorre entre o provedor de armazenamento de mensagem e MAPI.</span><span class="sxs-lookup"><span data-stu-id="55c2a-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="55c2a-107">Esta sequência de chamada do método permite MAPI obter um nível superior [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), e [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces e permite que o provedor de armazenamento de mensagem obter um objeto de suporte MAPI.</span><span class="sxs-lookup"><span data-stu-id="55c2a-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="55c2a-108">Após a sequência de chamadas, o provedor de armazenamento de mensagem deve estar pronto para aceitar logons de clientes.</span><span class="sxs-lookup"><span data-stu-id="55c2a-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="55c2a-109">A sequência de chamadas quando um provedor de mensagem que dll é carregada é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="55c2a-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="55c2a-110">O cliente chama [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="55c2a-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="55c2a-111">Se o armazenamento de mensagens já não estiver aberto, MAPI carrega a DLL do provedor de armazenamento e chama o ponto de entrada da DLL [MSProviderInit](msproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="55c2a-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="55c2a-112">Se o armazenamento de mensagens já estiver aberto, MAPI ignora as etapas 2 e 3 e, em seguida, usa existentes [IMSProvider: IUnknown](imsprovideriunknown.md) interface para concluir a etapa 4.</span><span class="sxs-lookup"><span data-stu-id="55c2a-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="55c2a-113">**MSProviderInit** cria e retorna um objeto **IMSProvider** .</span><span class="sxs-lookup"><span data-stu-id="55c2a-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="55c2a-114">Chamadas de MAPI [IMSProvider::Logon](imsprovider-logon.md), passando o identificador de entrada de repositório de mensagens do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="55c2a-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="55c2a-115">**IMSProvider::Logon** cria e retorna um [IMSLogon: IUnknown](imslogoniunknown.md) interface e um [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interface e, em seguida, chama o método [AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) em seu [IMAPISupport: IUnknown](imapisupportiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="55c2a-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="55c2a-116">Se a mensagem do cliente armazena o identificador de entrada se refere a um armazenamento de mensagens que já está aberto, o provedor de armazenamento de mensagens pode retornar as interfaces **IMSLogon** e **IMsgStore** existentes e não precisam chamar **AddRef** em seu objeto de suporte.</span><span class="sxs-lookup"><span data-stu-id="55c2a-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="55c2a-117">Se o cliente não definir o sinalizador MAPI_NO_MAIL quando ele conectado e ele não definiu a MDB_NO_MAIL na etapa 1, MAPI dá identificador de entrada do armazenamento de mensagens para o spooler MAPI modo o MAPI spooler pode fazer logon no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="55c2a-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="55c2a-118">MAPI retorna a interface de **IMsgStore** para o cliente.</span><span class="sxs-lookup"><span data-stu-id="55c2a-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="55c2a-119">O MAPI spooler chama [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="55c2a-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="55c2a-120">**IMSProvider::SpoolerLogon** retorna as mesmas interfaces **IMSLogon** e **IMsgStore** da etapa 5.</span><span class="sxs-lookup"><span data-stu-id="55c2a-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="55c2a-121">Se a chamada de logon para a mensagem armazenar provedor falhar porque uma senha incorreta foi fornecida e o provedor de armazenamento de mensagem não é possível exibir uma interface pedir a senha correta, ele deve retornar MAPI_E_FAILONEPROVIDER do \*\*IMSProvider::Logon \*\*método.</span><span class="sxs-lookup"><span data-stu-id="55c2a-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="55c2a-122">Isso permitirá que os clientes solicitar ao usuário uma senha para tentar fazer logon no provedor de armazenamento de mensagem novamente, em vez de causando MAPI falha do provedor de toda a sessão.</span><span class="sxs-lookup"><span data-stu-id="55c2a-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55c2a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="55c2a-123">See also</span></span>



[<span data-ttu-id="55c2a-124">Desenvolver um provedor de repositórios de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="55c2a-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

