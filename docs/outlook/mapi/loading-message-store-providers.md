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
# <a name="loading-message-store-providers"></a>Carregar provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um aplicativo cliente abre um armazenamento de mensagens, MAPI carrega a DLL do provedor de repositório a mensagem na memória. Depois de MAPI carrega a DLL, uma sequência muito específica de chamadas de método ocorre entre o provedor de armazenamento de mensagem e MAPI. Esta sequência de chamada do método permite MAPI obter um nível superior [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), e [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces e permite que o provedor de armazenamento de mensagem obter um objeto de suporte MAPI. Após a sequência de chamadas, o provedor de armazenamento de mensagem deve estar pronto para aceitar logons de clientes. 
  
A sequência de chamadas quando um provedor de mensagem que dll é carregada é da seguinte maneira:
  
1. O cliente chama [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Se o armazenamento de mensagens já não estiver aberto, MAPI carrega a DLL do provedor de armazenamento e chama o ponto de entrada da DLL [MSProviderInit](msproviderinit.md) . Se o armazenamento de mensagens já estiver aberto, MAPI ignora as etapas 2 e 3 e, em seguida, usa existentes [IMSProvider: IUnknown](imsprovideriunknown.md) interface para concluir a etapa 4. 
    
3. **MSProviderInit** cria e retorna um objeto **IMSProvider** . 
    
4. Chamadas de MAPI [IMSProvider::Logon](imsprovider-logon.md), passando o identificador de entrada de repositório de mensagens do aplicativo cliente.
    
5. **IMSProvider::Logon** cria e retorna um [IMSLogon: IUnknown](imslogoniunknown.md) interface e um [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interface e, em seguida, chama o método [AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) em seu [IMAPISupport: IUnknown](imapisupportiunknown.md) interface. Se a mensagem do cliente armazena o identificador de entrada se refere a um armazenamento de mensagens que já está aberto, o provedor de armazenamento de mensagens pode retornar as interfaces **IMSLogon** e **IMsgStore** existentes e não precisam chamar **AddRef** em seu objeto de suporte. 
    
6. Se o cliente não definir o sinalizador MAPI_NO_MAIL quando ele conectado e ele não definiu a MDB_NO_MAIL na etapa 1, MAPI dá identificador de entrada do armazenamento de mensagens para o spooler MAPI modo o MAPI spooler pode fazer logon no armazenamento de mensagens.
    
7. MAPI retorna a interface de **IMsgStore** para o cliente. 
    
8. O MAPI spooler chama [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** retorna as mesmas interfaces **IMSLogon** e **IMsgStore** da etapa 5. 
    
> [!NOTE]
> Se a chamada de logon para a mensagem armazenar provedor falhar porque uma senha incorreta foi fornecida e o provedor de armazenamento de mensagem não é possível exibir uma interface pedir a senha correta, ele deve retornar MAPI_E_FAILONEPROVIDER do **IMSProvider::Logon **método. Isso permitirá que os clientes solicitar ao usuário uma senha para tentar fazer logon no provedor de armazenamento de mensagem novamente, em vez de causando MAPI falha do provedor de toda a sessão. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

