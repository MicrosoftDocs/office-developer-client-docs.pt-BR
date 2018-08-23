---
title: Abrindo um armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4bab31dbcd1f7139980d7df5559c1ee52a6f167f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563643"
---
# <a name="opening-a-message-store"></a>Abrindo um armazenamento de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Dependendo do perfil, um cliente precisará abrir um ou mais armazenamentos de mensagem durante uma sessão típica. Abrir um repositório de mensagem significa que tenha acesso a um ponteiro para seu [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) implementação. A interface **IMsgStore** fornece métodos para fazer atribuições de pasta e o acesso às pastas e mensagens de notificação. 
  
Clientes abrem armazenamentos de mensagem no logon e um perfil está sendo modificado. Se seu cliente permite que os usuários adicionem armazenamentos de mensagens ao perfil durante uma sessão ativa, você pode abri-los imediatamente ou ignorá-las até a sessão seguinte. Registrando para notificações na tabela de repositório de mensagens, você receberá um alerta para a disponibilidade de um novo repositório de mensagem.
  
Para abrir um armazenamento de mensagens, você deve ter seu identificador de entrada disponível. A maioria dos clientes acessar os identificadores de entrada para os repositórios de mensagem que desejam abrir através da tabela de repositório de mensagens. No entanto, alguns mensagem armazena o formato dos seus identificadores de entrada, habilitando clientes a fim de ignorar a tabela de repositório de mensagens e construir o identificador de entrada necessários do documento. Eles podem passar esse identificador de entrada diretamente ao [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) e MAPI cria automaticamente uma seção de perfil para o provedor sem associá-la a qualquer serviço de mensagem. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Recuperar um identificador de entrada da tabela de repositório de mensagens
  
1. Chame [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela de repositório de mensagens. 
    
2. Chame **IMAPITable::SetColumns** para limitar a tabela a um conjunto pequeno de coluna que inclui as seguintes colunas: 
    
   - **PR_PROVIDER_DISPLAY** ou **PR_DISPLAY_NAME**
   - Propriedades **PR_ENTRYID** 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Construa uma restrição para filtrar a linha que representa o armazenamento de mensagens a ser aberto. Para obter mais informações sobre procurando o armazenamento de mensagens padrão, consulte [abrindo o armazenamento de mensagens padrão](opening-the-default-message-store.md). Para procurar um armazenamento de mensagens pelo nome, aplica qualquer uma das seguintes restrições de propriedade:
    
   - Correspondência **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) com o nome geral para esse tipo de armazenamento de mensagens. Por exemplo, PR_PROVIDER_DISPLAY pode ser definido como "Pastas particulares".
    
   - Correspondência **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) com o específico **MAPIUID** para esse tipo de armazenamento de mensagens. 
    
   - Correspondência **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome para este armazenamento de mensagens específico. Por exemplo, **PR_DISPLAY_NAME** pode ser definido como "Minhas mensagens para o Ano Fiscal 2010". 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar a linha apropriada da tabela de repositório de mensagem. O identificador de entrada para a linha será incluído na matriz de valores de propriedade para o membro **aRow** do conjunto de linha apontado pelo parâmetro _pprows_ . 
    
5. Chame [FreeProws](freeprows.md) para liberar o conjunto de linhas apontado pela _pprows_.
    
6. A tabela de repositório de mensagens chamando seu método **IUnknown:: Release** do lançamento. 
    
Se você tiver criado um identificador de entrada personalizado para o armazenamento de mensagens a ser aberto, chame a função de [WrapStoreEntryID](wrapstoreentryid.md) para convertê-lo em um identificador de entrada padrão. 
  
Depois que tiver o identificador de entrada de um armazenamento de mensagens, ligue para um dos seguintes métodos para abri-lo:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Chame **OpenMsgStore** se você precisar especificar uma variedade de opções especiais para o armazenamento de mensagens. **OpenMsgStore** permite que você para suprimir a exibição das caixas de diálogo, identificar o armazenamento de mensagens, como temporária ou como um repositório nonmessaging, definir níveis de acesso e para adiar a erros. **OpenEntry** permite apenas definir níveis de acesso e adie erros. 
  
Definindo o MDB_NO_MAIL sinalizador indica MAPI que o armazenamento de mensagens não será usado para enviar ou receber mensagens. MAPI não informar o spooler de MAPI sobre a existência deste armazenamento de mensagens. O sinalizador MDB_TEMPORARY designa um armazenamento de mensagens como temporário, indicando que não pode ser usado para armazenar informações permanentes. Repositórios de mensagem temporária não aparecem na tabela de repositório de mensagens. 
  
## <a name="see-also"></a>Confira também

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

