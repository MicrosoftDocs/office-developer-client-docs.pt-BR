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
# <a name="exposing-folders-in-message-stores"></a>Expor pastas em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todo provedor de repositórios de mensagens deve apresentar uma interface [IMAPIFolder](imapifolderimapicontainer.md) de nível superior para aplicativos clientes. A pasta de nível superior corresponde ao a todo o repositórios de mensagens; ela fornece acesso às pastas que os usuários veem como o conteúdo do repositório de mensagens. Além disso, a pasta de nível superior é usada com frequência como pasta de recebimento padrão para mensagens IPC, e como a pasta da qual os relatórios de leitura são enviados. Os provedores de repositórios de mensagens também devem apresentar uma subárvore IPM — um conjunto de pastas usado para guardar mensagens IPM — para aplicativos clientes. 
  
Os aplicativos cliente podem abrir a pasta de nível superior chamando o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com 0 e NULO para os parâmetros _cbEntryId_ e _lpEntryId_, respectivamente. Na maioria dos casos, no entanto, os aplicativos clientes abrem o conjunto de pastas que contém mensagens IPM. 
  
Para obter uma lista de pastas na árvore de pastas IPM do repositório de mensagens, use o procedimento a seguir:
  
1. Usar a sessão MAPI para chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). 
    
2. Use o ponteiro do banco de dados resultante mensagem para chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. Chame o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com o identificador de entrada para obter um ponteiro **IMAPIFolder**. 
    
4. Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obter uma tabela do conteúdo da pasta. 
    
5. Chame o método [IMAPITable::QueryRows](imapitable-queryrows.md) para listar as pastas na pasta de nível superior. 
    
Os clientes MAPI usam essas pastas para acessar outros objetos de pasta e objetos de mensagem no repositório de mensagens. **IMAPIFolder**e sua interface do pai [IMAPIContainer](imapicontainerimapiprop.md) contêm os métodos que seu provedor de repositório de mensagens precisa implementar para preencher as pastas com objetos de mensagem e responder a solicitações de clientes para operar nas mensagens.
  
## <a name="see-also"></a>Confira também



[Implementar pastas em repositórios de mensagens](implementing-folders-in-message-stores.md)

