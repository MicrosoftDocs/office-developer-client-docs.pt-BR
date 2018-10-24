---
title: Destinatários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6af54b773b875531437a275f14c961a06ef799ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569516"
---
# <a name="mapi-recipients"></a>Destinatários MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todas as mensagens sejam transmitidas tem um ou mais destinatários, ou um conjunto de propriedades que descrevem a qual a mensagem deve ser entregue. Como os destinatários são usados apenas no contexto de uma mensagem, eles são considerados subobjetos de uma mensagem em vez de objetos separados de MAPI. Clientes e provedores trabalham com destinatários usando a interface **IMessage** . Para obter mais informações, consulte [IMessage: IMAPIProp](imessageimapiprop.md).
  
Os clientes acessam os destinatários da mensagem por meio de sua tabela de destinatário. Cada mensagem tem uma tabela de destinatários que contém informações de resumo sobre cada um dos seus destinatários. As colunas incluídas na tabela dependem do estado da mensagem. Quando uma mensagem está sob composição, seus destinatários podem ter apenas três colunas na tabela:
  
- Nome para exibição ou **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- Tipo de destinatário ou **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- Identificador de linha, ou **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Depois que a mensagem passou o processo de resolução de nomes, cada destinatário também terão um identificador de entrada ou coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). E quando a mensagem foi enviada, as linhas na tabela de destinatário adicionará duas ou mais colunas:
  
- Tipo de endereço ou **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- Responsabilidade de transporte ou **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Os clientes podem recuperar a tabela de destinatário da mensagem chamando seu método **IMessage::GetRecipientTable** ou seu método de **IMAPIProp::OpenProperty** . Para obter mais informações, consulte [IMessage::GetRecipientTable](imessage-getrecipienttable.md) e [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Provedores de armazenamento de mensagem esperados para dar suporte a essas duas abordagens. A abordagem de **OpenProperty** requer que o cliente especifica IID_IMAPITable como o identificador de interface e **PR_MESSAGE_RECIPIENTS** como a marca de propriedade. **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) é uma propriedade de objeto de tabela que representa a tabela de destinatário da mensagem. Provedores de armazenamento de mensagem são necessárias para definir **PR_MESSAGE_RECIPIENTS** para cada mensagem e incluí-lo na matriz de marcas de propriedade retornado pelo método **IMAPIProp::GetPropList** . Para obter mais informações, consulte [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
Para obter mais informações sobre como trabalhar com uma tabela de destinatário, consulte [As tabelas de destinatário](recipient-tables.md).
  
Além do que está sendo usado para acessar uma tabela de destinatário, **PR_MESSAGE_RECIPIENTS** podem ser usados: 
  
- Com **IMAPIProp::CopyTo** ou **IMAPIProp::CopyProps** para excluir ou incluir destinatários ao copiar. Para mais informações, consulte [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Uma restrição subobjeto para indicar que a restrição de filho deve ser aplicadas aos destinatários.
    
Os clientes podem adicionar destinatários a uma mensagem Copiando entradas do catálogo de endereços MAPI ou pela criação de novas entradas. Essas novas entradas, chamadas algo isolado, podem existir temporariamente ou salvas permanentemente em um contêiner pode ser modificado. Enquanto os destinatários que serão executados do catálogo de endereços têm identificadores de entrada associados ao seu provedor de catálogo de endereços, destinatários únicos têm identificadores de entrada formatados pelo MAPI. Identificadores de entrada únicos associe de clientes com vários tipos de endereços e provedores de transporte. 
  
**IMAPISupport::CreateOneOff** para criar um identificador de entrada únicos para um endereço em uma saída de chamada de provedores de transporte de mensagem quando: 
  
- O endereço pertence a um gateway.
    
- O endereço não pode ser manipulado por um fornecedor de catálogo de endereços no perfil atual.
    
Para obter mais informações, consulte [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Clientes chamar **IAddrBook::CreateOneOff** para criar um identificador de entrada únicos para um endereço em uma entrada de mensagem quando: 
  
- O endereço é formatado como um endereço one-off.
    
- O endereço é formatado como um endereço de Internet.
    
Para obter mais informações, consulte [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).
  
Para obter mais informações sobre identificadores de entrada únicos e endereços, consulte [Identificadores de entrada únicos](one-off-entry-identifiers.md) e [Endereços únicos](one-off-addresses.md).
  
As propriedades de um destinatário são uma combinação de propriedades do catálogo de endereços e destinatários propriedades específicas. Todos os destinatários tem as propriedades de um endereço base, atribuídas por provedores de catálogo de endereços. Quando uma entrada é usada como um destinatário de uma mensagem de saída, as propriedades de um endereço base são copiadas para a estrutura **ADRLIST** que contém as propriedades de todos os destinatários da mensagem. 
  
Duas propriedades que são definidas especificamente para os destinatários são **PR_RECIPIENT_TYPE** e **PR_RESPONSIBILITY**. **PR_RECIPIENT_TYPE** indica se um destinatário é primário, cópia carbono, cópia oculta ou um destinatário de reenvio. Os três primeiros tipos são atribuídos a destinatários em mensagens que estão sendo enviadas pela primeira vez. 
  
Se um destinatário não receber a mensagem e é feita uma tentativa de enviá-lo novamente, o destinatário é copiado e seu tipo está definido para MAPI_P1 para indicar que se trata de um destinatário de reenvio. Se apenas alguns dos destinatários recebem uma mensagem, suas propriedades **PR_RECIPIENT_TYPE** são marcadas com a adição do sinalizador MAPI_SUBMITTED quando a mensagem é enviada novamente. Os clientes são necessários para lidar com destinatários principais ou destinatários com seus **PR_RECIPIENT_TYPE** definido como MAPI_TO. Todos os outros tipos são opcionais. 
  
 **PR_RESPONSIBILITY** é definida para indicar ao provedor de transporte se ou não deve lidar enviando ao destinatário. Quando uma mensagem de saída é enviada pela primeira vez, todos os destinatários defina **PR_RESPONSIBILITY** como FALSE. Como um provedor de transporte de responsabilidade para enviar a um ou mais dos destinatários de declarações, suas propriedades **PR_RESPONSIBILITY** estiverem definidas como TRUE. 
  

