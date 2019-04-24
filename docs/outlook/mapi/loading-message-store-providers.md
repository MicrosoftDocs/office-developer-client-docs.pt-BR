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
# <a name="loading-message-store-providers"></a>Carregando provedores de repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um aplicativo cliente abre um repositório de mensagens, o MAPI carrega a DLL do provedor de repositório de mensagens na memória. Após o MAPI carregar a DLL, uma sequência muito específica de chamadas de método ocorrerá entre o provedor de armazenamento de mensagens e o MAPI. Esta sequência de chamadas de método permite que o MAPI obtenha IMSProvider de nível superior [: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md)e [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces e permite que o provedor de repositório de mensagens obtenha um objeto de suporte MAPI. Após a sequência de chamadas, o provedor do repositório de mensagens deve estar pronto para aceitar logons de clientes. 
  
A sequência de chamadas quando uma DLL de provedor de mensagens é carregada é a seguinte:
  
1. O cliente chama [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md).
    
2. Se o repositório de mensagens ainda não estiver aberto, o MAPI carregará a DLL do provedor de repositório e chamará o ponto de entrada do [MSProviderInit](msproviderinit.md) da dll. Se o repositório de mensagens já estiver aberto, o MAPI ignorará as etapas 2 e 3 e, em seguida, usará a interface [IMSProvider: IUnknown](imsprovideriunknown.md) existente para concluir a etapa 4. 
    
3. **MSProviderInit** cria e retorna um objeto **IMSProvider** . 
    
4. Chamadas MAPI [IMSProvider:: logon](imsprovider-logon.md), passando o identificador de entrada do repositório de mensagens do aplicativo cliente.
    
5. **IMSProvider:: logon** cria e retorna uma interface [IMSLogon: IUnknown](imslogoniunknown.md) e uma interface [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) e, em seguida, chama o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) na interface [IMAPISupport: IUnknown](imapisupportiunknown.md) . Se o identificador de entrada do repositório de mensagens do cliente se referir a um repositório de mensagens que já está aberto, o provedor de repositório de mensagens poderá retornar as interfaces existentes do **IMSLogon** e do **IMsgStore** e não precisará chamar **AddRef** em seu objeto support. 
    
6. Se o cliente não tiver definido o sinalizador MAPI_NO_MAIL quando estiver conectado e não tiver definido o MDB_NO_MAIL na etapa 1, o MAPI fornecerá o identificador de entrada do repositório de mensagens ao spooler MAPI para que o spooler MAPI possa fazer logon no repositório de mensagens.
    
7. MAPI retorna a interface **IMsgStore** para o cliente. 
    
8. O spooler MAPI chama [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider:: SpoolerLogon** retorna as mesmas interfaces **IMSLogon** e **IMsgStore** da etapa 5. 
    
> [!NOTE]
> Se a chamada de logon para o provedor de armazenamento de mensagens falhar porque uma senha incorreta foi fornecida e o provedor de repositório de mensagens não pode exibir uma interface para solicitar a senha correta, ele deve retornar MAPI_E_FAILONEPROVIDER do **IMSProvider:: logon **método. Isso permitirá que os clientes solicitem ao usuário uma senha para tentar fazer logon no provedor de armazenamento de mensagens novamente, em vez de fazer com que o MAPI falhe o provedor para toda a sessão. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

