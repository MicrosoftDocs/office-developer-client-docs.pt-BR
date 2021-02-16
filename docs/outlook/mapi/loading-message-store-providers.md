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
# <a name="loading-message-store-providers"></a>Carregando provedores de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um aplicativo cliente abre um armazenamento de mensagens, o MAPI carrega a DLL do provedor de armazenamento de mensagens na memória. Depois que o MAPI carrega a DLL, ocorre uma sequência muito específica de chamadas de método entre o provedor do armazenamento de mensagens e o MAPI. Essa sequência de chamada de método permite que MAPI obter [IMSProvider de](imsprovideriunknown.md)nível superior : IUnknown , [IMSLogon : IUnknown](imslogoniunknown.md)e [IMsgStore : interfaces IMAPIProp](imsgstoreimapiprop.md) e permite que o provedor de repositório de mensagens obter um objeto de suporte MAPI. Após a sequência de chamada, o provedor de armazenamento de mensagens deve estar pronto para aceitar logons de clientes. 
  
A sequência de chamada quando uma DLL do provedor de mensagens é carregada é a seguinte:
  
1. O cliente chama [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Se o armazenamento de mensagens ainda não estiver aberto, o MAPI carregará a DLL do provedor de armazenamento e chamará o ponto de entrada [MSProviderInit](msproviderinit.md) da DLL. Se o armazenamento de mensagens já estiver aberto, o MAPI ignorará as etapas 2 e 3 e usará a interface [IMSProvider : IUnknown](imsprovideriunknown.md) existente para concluir a etapa 4. 
    
3. **MSProviderInit** cria e retorna **um objeto IMSProvider.** 
    
4. MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.
    
5. **IMSProvider::Logon** cria e retorna um [IMSLogon : interface IUnknown](imslogoniunknown.md) e [IMsgStore : interface IMAPIProp](imsgstoreimapiprop.md) e chama o método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) em seu [IMAPISupport : interface IUnknown.](imapisupportiunknown.md) Se o identificador de entrada do repositório de mensagens do cliente se referir a um repositório de mensagens que já está aberto, o provedor de repositório de mensagens poderá retornar interfaces **IMSLogon** e **IMsgStore** existentes e não precisará chamar **AddRef** em seu objeto de suporte. 
    
6. Se o cliente não definiu o sinalizador MAPI_NO_MAIL quando fez logoff e não definiu o MDB_NO_MAIL na etapa 1, o MAPI fornece o identificador de entrada do armazenamento de mensagens para o spooler MAPI para que o spooler MAPI possa fazer logoff no armazenamento de mensagens.
    
7. MAPI returns the **IMsgStore** interface to the client. 
    
8. O spooler MAPI chama [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** retorna as mesmas interfaces **IMSLogon** e **IMsgStore** da etapa 5. 
    
> [!NOTE]
> Se a chamada de logon para o provedor de armazenamento de mensagens falhar porque uma senha incorreta foi fornecida e o provedor do armazenamento de mensagens não puder exibir uma interface para solicitar a senha correta, ela deverá retornar MAPI_E_FAILONEPROVIDER do método **IMSProvider::Logon.** Isso permitirá que os clientes solicitam ao usuário uma senha para tentar fazer logon no provedor de armazenamento de mensagens novamente, em vez de fazer com que o MAPI falhe no provedor de toda a sessão. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

