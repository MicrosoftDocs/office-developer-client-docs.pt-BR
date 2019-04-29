---
title: Abrir um repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 665c14b285db166e4f2a421d46e57f23e2f7ad52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432370"
---
# <a name="opening-a-message-store"></a>Abrir um repositório de mensagens

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Dependendo do perfil, um cliente precisará abrir um ou mais repositórios de mensagens durante uma sessão típica. Abrir um repositório de mensagens significa obter acesso a um ponteiro para sua implementação do [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) . A interface **IMsgStore** fornece métodos para notificação, fazer atribuições de pasta e acessar pastas e mensagens. 
  
Os clientes abrem repositórios de mensagens no logon e quando um perfil está sendo modificado. Se o cliente permitir que os usuários adicionem repositórios de mensagens ao perfil durante uma sessão ativa, você poderá abri-los imediatamente ou ignorá-los até a próxima sessão. Ao se registrar para notificações na tabela de repositório de mensagens, você será alertado sobre a disponibilidade de um novo repositório de mensagens.
  
Para abrir um repositório de mensagens, você deve ter seu identificador de entrada disponível. A maioria dos clientes acessa os identificadores de entrada para os repositórios de mensagens que desejam abrir por meio da tabela do repositório de mensagens. No enTanto, alguns repositórios de mensagens documentam o formato de seus identificadores de entrada, permitindo que os clientes ignorem a tabela do repositório de mensagens e construam o identificador de entrada necessário. Eles podem passar esse identificador de entrada diretamente para [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) e MAPI cria automaticamente uma seção de perfil para o provedor sem associá-lo a qualquer serviço de mensagens. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Recuperar um identificador de entrada da tabela do repositório de mensagens
  
1. Chame [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela do repositório de mensagens. 
    
2. Call **IMAPITable::** SetColumns para limitar a tabela a um pequeno conjunto de colunas que inclui as seguintes colunas: 
    
   - **PR_PROVIDER_DISPLAY** ou **PR_DISPLAY_NAME**
   - Propriedades **PR_ENTRYID** 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Criar uma restrição para filtrar a linha que representa o repositório de mensagens a ser aberto. Para obter mais informações sobre como procurar o repositório de mensagens padrão, consulte [abrindo o repositório de mensagens padrão](opening-the-default-message-store.md). Para procurar um repositório de mensagens por nome, aplique qualquer uma das seguintes restrições de propriedade:
    
   - Corresponder **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) com o nome geral desse tipo de repositório de mensagens. Por exemplo, PR_PROVIDER_DISPLAY pode ser definido como "pastas pessoais".
    
   - Corresponder **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) com o **MAPIUID** específico para este tipo de repositório de mensagens. 
    
   - Corresponder **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome desse repositório de mensagens específico. Por exemplo, **PR_DISPLAY_NAME** pode ser definido como "minhas mensagens para o ano fiscal 2010". 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar a linha apropriada da tabela do repositório de mensagens. O identificador de entrada da linha será incluído na matriz de valor da propriedade para o membro **aRow** do conjunto de linhas apontado pelo parâmetro _pprows_ . 
    
5. Chame [FreeProws](freeprows.md) para liberar o conjunto de linhas apontado por _pprows_.
    
6. Libere a tabela do repositório de mensagens chamando seu método **IUnknown:: Release** . 
    
Se você tiver criado um identificador de entrada personalizada para que o repositório de mensagens seja aberto, chame a função [WrapStoreEntryID](wrapstoreentryid.md) para convertê-lo em um identificador de entrada padrão. 
  
Depois que você tiver um identificador de entrada do repositório de mensagens, chame um dos seguintes métodos para abri-lo:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Chame **OpenMsgStore** se você precisar especificar uma variedade de opções especiais para o repositório de mensagens. O **OpenMsgStore** permite que você suprime a exibição de caixas de diálogo, identifique o repositório de mensagens como temporário ou como um repositório de não-mensagens, defina níveis de acesso e para adiar erros. O **OpenEntry** permite que você defina níveis de acesso e adie erros. 
  
Definir o sinalizador MDB_NO_MAIL indica ao MAPI que o repositório de mensagens não será usado para enviar ou receber mensagens. O MAPI não informa o spooler MAPI sobre a existência deste repositório de mensagens. O sinalizador MDB_TEMPORARY designa um repositório de mensagens como temporários, indicando que não pode ser usado para armazenar informações permanentes. Repositórios de mensagens temporários não aparecem na tabela do repositório de mensagens. 
  
## <a name="see-also"></a>Confira também

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

