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
  
Dependendo do perfil, um cliente precisará abrir um ou mais armazenamentos de mensagens durante uma sessão típica. Abrir um repositório de mensagens significa obter acesso a um ponteiro para sua [IMsgStore : implementação IMAPIProp.](imsgstoreimapiprop.md) A interface **IMsgStore** fornece métodos para notificação, atribuição de pastas e acesso a pastas e mensagens. 
  
Os clientes abrem os armazenamentos de mensagens no logon e quando um perfil está sendo modificado. Se o cliente permitir que os usuários adicionem armazenamentos de mensagens ao perfil durante uma sessão ativa, você poderá abri-los imediatamente ou ignorá-los até a próxima sessão. Ao se registrar para notificações na tabela do armazenamento de mensagens, você será alertado sobre a disponibilidade de um novo armazenamento de mensagens.
  
Para abrir um armazenamento de mensagens, você deve ter seu identificador de entrada disponível. A maioria dos clientes acessa os identificadores de entrada para os armazenamentos de mensagens que desejam abrir por meio da tabela do armazenamento de mensagens. No entanto, alguns armazenamentos de mensagens documentam o formato de seus identificadores de entrada, permitindo que os clientes ignorem a tabela do armazenamento de mensagens e construam o identificador de entrada necessário. Eles podem passar esse identificador de entrada diretamente para [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) e MAPI cria automaticamente uma seção de perfil para o provedor sem associá-la a nenhum serviço de mensagem. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Recuperar um identificador de entrada da tabela do armazenamento de mensagens
  
1. Chame [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela do armazenamento de mensagens. 
    
2. Chame **IMAPITable::SetColumns** para limitar a tabela a um pequeno conjunto de colunas que inclui as seguintes colunas: 
    
   - **PR_PROVIDER_DISPLAY** ou **PR_DISPLAY_NAME**
   - **PR_ENTRYID** propriedades 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Crie uma restrição para filtrar a linha que representa o armazenamento de mensagens a ser aberto. Para obter mais informações sobre como procurar o armazenamento de mensagens padrão, consulte [Abrindo o Armazenamento de Mensagens Padrão.](opening-the-default-message-store.md) Para procurar um armazenamento de mensagens por nome, aplique qualquer uma das seguintes restrições de propriedade:
    
   - Corresponder **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) com o nome geral desse tipo de armazenamento de mensagens. Por exemplo, PR_PROVIDER_DISPLAY pode ser definido como "Pastas Particulares".
    
   - Corresponder **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) com **o MAPIUID** específico para esse tipo de repositório de mensagens. 
    
   - Corresponder **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome desse armazenamento de mensagens específico. Por exemplo, **PR_DISPLAY_NAME** pode ser definido como "Minhas Mensagens para o Ano Fiscal de 2010". 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar a linha apropriada da tabela do armazenamento de mensagens. O identificador de entrada para a linha será incluído na matriz de valores de propriedade para o membro **aRow** do conjunto de linhas apontado pelo _parâmetro pprows._ 
    
5. Chame [FreeProws para](freeprows.md) liberar o conjunto de linhas apontado por  _pprows_.
    
6. Libere a tabela do armazenamento de mensagens chamando seu **método IUnknown::Release.** 
    
Se você criou um identificador de entrada personalizado para o repositório de mensagens ser aberto, chame a função [WrapStoreEntryID](wrapstoreentryid.md) para convertê-lo em um identificador de entrada padrão. 
  
Depois de ter o identificador de entrada de um armazenamento de mensagens, chame um dos seguintes métodos para abri-lo:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Chame **OpenMsgStore** se precisar especificar uma variedade de opções especiais para o repositório de mensagens. **OpenMsgStore** permite suprimir a exibição de caixas de diálogo, identificar o repositório de mensagens como temporário ou como um repositório não-desassecado, definir níveis de acesso e adiar erros. **OpenEntry** permite que você somente de definir níveis de acesso e adiar erros. 
  
A definição MDB_NO_MAIL sinalizador de MDB_NO_MAIL indica ao MAPI que o armazenamento de mensagens não será usado para envio ou recebimento de mensagens. O MAPI não informa o spooler MAPI sobre a existência desse armazenamento de mensagens. O MDB_TEMPORARY sinalizador designa um armazenamento de mensagens como temporário, indicando que ele não pode ser usado para armazenar informações permanentes. Os armazenamentos temporários de mensagens não aparecem na tabela do armazenamento de mensagens. 
  
## <a name="see-also"></a>Confira também

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

