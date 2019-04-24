---
title: Carregando provedores de repositório de mensagens
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
# <a name="loading-message-store-providers"></a><span data-ttu-id="19709-103">Carregando provedores de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="19709-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="19709-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19709-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19709-105">Quando um aplicativo cliente abre um repositório de mensagens, o MAPI carrega a DLL do provedor de repositório de mensagens na memória.</span><span class="sxs-lookup"><span data-stu-id="19709-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="19709-106">Após o MAPI carregar a DLL, uma sequência muito específica de chamadas de método ocorrerá entre o provedor de armazenamento de mensagens e o MAPI.</span><span class="sxs-lookup"><span data-stu-id="19709-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="19709-107">Esta sequência de chamadas de método permite que o MAPI obtenha IMSProvider de nível superior [: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md)e [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces e permite que o provedor de repositório de mensagens obtenha um objeto de suporte MAPI.</span><span class="sxs-lookup"><span data-stu-id="19709-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="19709-108">Após a sequência de chamadas, o provedor do repositório de mensagens deve estar pronto para aceitar logons de clientes.</span><span class="sxs-lookup"><span data-stu-id="19709-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="19709-109">A sequência de chamadas quando uma DLL de provedor de mensagens é carregada é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="19709-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="19709-110">O cliente chama [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="19709-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="19709-111">Se o repositório de mensagens ainda não estiver aberto, o MAPI carregará a DLL do provedor de repositório e chamará o ponto de entrada do [MSProviderInit](msproviderinit.md) da dll.</span><span class="sxs-lookup"><span data-stu-id="19709-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="19709-112">Se o repositório de mensagens já estiver aberto, o MAPI ignorará as etapas 2 e 3 e, em seguida, usará a interface [IMSProvider: IUnknown](imsprovideriunknown.md) existente para concluir a etapa 4.</span><span class="sxs-lookup"><span data-stu-id="19709-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="19709-113">**MSProviderInit** cria e retorna um objeto **IMSProvider** .</span><span class="sxs-lookup"><span data-stu-id="19709-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="19709-114">Chamadas MAPI [IMSProvider:: logon](imsprovider-logon.md), passando o identificador de entrada do repositório de mensagens do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="19709-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="19709-115">**IMSProvider:: logon** cria e retorna uma interface [IMSLogon: IUnknown](imslogoniunknown.md) e uma interface [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) e, em seguida, chama o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) na interface [IMAPISupport: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="19709-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="19709-116">Se o identificador de entrada do repositório de mensagens do cliente se referir a um repositório de mensagens que já está aberto, o provedor de repositório de mensagens poderá retornar as interfaces existentes do **IMSLogon** e do **IMsgStore** e não precisará chamar **AddRef** em seu objeto support.</span><span class="sxs-lookup"><span data-stu-id="19709-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="19709-117">Se o cliente não tiver definido o sinalizador MAPI_NO_MAIL quando estiver conectado e não tiver definido o MDB_NO_MAIL na etapa 1, o MAPI fornecerá o identificador de entrada do repositório de mensagens ao spooler MAPI para que o spooler MAPI possa fazer logon no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="19709-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="19709-118">MAPI retorna a interface **IMsgStore** para o cliente.</span><span class="sxs-lookup"><span data-stu-id="19709-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="19709-119">O spooler MAPI chama [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="19709-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="19709-120">**IMSProvider:: SpoolerLogon** retorna as mesmas interfaces **IMSLogon** e **IMsgStore** da etapa 5.</span><span class="sxs-lookup"><span data-stu-id="19709-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="19709-121">Se a chamada de logon para o provedor de armazenamento de mensagens falhar porque uma senha incorreta foi fornecida e o provedor de repositório de mensagens não pode exibir uma interface para solicitar a senha correta, ele deve retornar MAPI_E_FAILONEPROVIDER do \*\*IMSProvider:: logon \*\*método.</span><span class="sxs-lookup"><span data-stu-id="19709-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="19709-122">Isso permitirá que os clientes solicitem ao usuário uma senha para tentar fazer logon no provedor de armazenamento de mensagens novamente, em vez de fazer com que o MAPI falhe o provedor para toda a sessão.</span><span class="sxs-lookup"><span data-stu-id="19709-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19709-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="19709-123">See also</span></span>



[<span data-ttu-id="19709-124">Desenvolver um provedor de repositórios de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="19709-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

