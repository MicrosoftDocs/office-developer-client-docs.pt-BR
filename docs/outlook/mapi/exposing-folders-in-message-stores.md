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
# <a name="exposing-folders-in-message-stores"></a>Expor pastas em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedor de armazenamento de cada mensagem deve apresentar uma interface de [IMAPIFolder](imapifolderimapicontainer.md) de nível superior para os aplicativos cliente. A pasta de nível superior corresponde ao repositório de toda a mensagem; Ele fornece acesso às pastas que os usuários veem como o conteúdo do armazenamento de mensagens. Além disso, a pasta de nível superior é frequentemente usada como pasta para mensagens de CPI e como a pasta de recebimento padrão do qual ler relatórios são enviados. Provedores de armazenamento de mensagem também devem apresentar uma subárvore IPM — um conjunto de pastas usadas para armazenar mensagens IPM — para os aplicativos cliente. 
  
Aplicativos cliente podem abrir a pasta de nível superior chamando o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com 0 e NULL para os parâmetros _cbEntryId_ e _lpEntryId_ , respectivamente. Na maioria dos casos, no entanto, os aplicativos cliente abram o conjunto de pastas que contêm mensagens IPM. 
  
Para obter uma lista de pastas na árvore de pastas da loja mensagem IPM, use o procedimento a seguir:
  
1. Use sua sessão MAPI para chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
    
2. Use o ponteiro de banco de dados de mensagem resultante para chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. Chame o método [IMsgStore::OpenEntry](imsgstore-openentry.md) com o identificador de entrada para obter um ponteiro **IMAPIFolder** . 
    
4. Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obter um índice de conteúdo da pasta. 
    
5. Chame o método [IMAPITable:: QueryRows](imapitable-queryrows.md) para listar as pastas na pasta de nível superior. 
    
Clientes MAPI usam essas pastas para acessar outros objetos folder e objetos de mensagem no repositório de mensagem. **IMAPIFolder**e sua interface pai [IMAPIContainer](imapicontainerimapiprop.md), contêm os métodos que seu provedor de armazenamento de mensagem deve implementar para preencher pastas com objetos de mensagem e responde a solicitações de cliente para operar nas mensagens.
  
## <a name="see-also"></a>Confira também



[Implementar pastas em repositórios de mensagens](implementing-folders-in-message-stores.md)

