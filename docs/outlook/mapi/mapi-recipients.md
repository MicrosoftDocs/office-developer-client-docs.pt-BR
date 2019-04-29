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
ms.openlocfilehash: ebdaf47b4f20763574ffac73bddeb3eb4eeb95df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423689"
---
# <a name="mapi-recipients"></a>Destinatários MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada mensagem a ser transmitida tem um ou mais destinatários ou um conjunto de propriedades que descrevem onde a mensagem deve ser entregue. Como os destinatários são usados somente no contexto de uma mensagem, eles são considerados subobjetos de uma mensagem em vez de objetos MAPI separados. Clientes e provedores trabalham com destinatários usando a interface **IMessage** . Para obter mais informações, consulte [IMessage: IMAPIProp](imessageimapiprop.md).
  
Os clientes acessam os destinatários de uma mensagem por meio de sua tabela de destinatários. Cada mensagem tem uma tabela de destinatários que contém informações resumidas sobre cada um dos seus destinatários. As colunas incluídas na tabela dependem do estado da mensagem. Quando uma mensagem está em composição, seus destinatários podem ter apenas três colunas na tabela:
  
- Nome para exibição ou **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- Tipo de destinatário ou **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- Identificador de linha ou **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Depois que a mensagem passou no processo de resolução de nomes, cada destinatário também terá um identificador de entrada ou uma coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). E, quando a mensagem for enviada, as linhas na tabela de destinatários adicionarão mais duas colunas:
  
- Tipo de endereço ou **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- Responsabilidade de transporte ou **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Os clientes podem recuperar a tabela de destinatários de uma mensagem chamando o método **IMessage::** GetRecipientTable ou seu método **IMAPIProp:: OpenProperty** . Para obter mais informações, consulte [IMessage::](imessage-getrecipienttable.md) GetRecipientTable e [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). Espera-se que os provedores de repositório de mensagens ofereçam suporte a ambas as abordagens. A **** abordagem de OpenProperty requer que o cliente especifique IID_IMAPITable como o identificador de interface e **PR_MESSAGE_RECIPIENTS** como a marca de propriedade. **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) é uma propriedade de objeto Table que representa a tabela de destinatários de uma mensagem. Os provedores de repositório de mensagens são necessários para definir o **PR_MESSAGE_RECIPIENTS** para cada mensagem e incluí-lo na matriz de marcas de propriedade retornadas do método **IMAPIProp::** getproplist. Para obter mais informações, consulte [IMAPIProp::](imapiprop-getproplist.md)getproplist.
  
Para obter mais informações sobre como trabalhar com uma tabela de destinatários, consulte [tabelas de destinatários](recipient-tables.md).
  
Além de ser usado para acessar uma tabela de destinatários, o **PR_MESSAGE_RECIPIENTS** pode ser usado: 
  
- Com **IMAPIProp:: CopyTo** ou **IMAPIProp:: CopyProps** para excluir ou incluir destinatários ao copiar. Para obter mais informações, consulte, [IMAPIProp:: CopyTo](imapiprop-copyto.md) e [IMAPIProp:: CopyProps](imapiprop-copyprops.md).
    
- Em uma restrição de subobjeto para indicar que o restiction filho deve se aplicar aos destinatários.
    
Os clientes podem adicionar destinatários a uma mensagem copiando entradas do catálogo de endereços MAPI ou criando novas entradas. Essas novas entradas, chamadas de um, podem existir temporariamente ou serem salvas permanentemente em um contêiner modificável. Enquanto os destinatários obtidos do catálogo de endereços possuem identificadores de entrada associados ao seu provedor de catálogo de endereços, os destinatários únicos têm identificadores de entrada formatados por MAPI. Os provedores de transporte e os clientes associam identificadores de entrada únicos a vários tipos de endereços. 
  
Os provedores de transporte chamam **IMAPISupport:: CreateOneOff** para criar um identificador de entrada one-off para um endereço em uma mensagem de saída quando: 
  
- O endereço pertence a um gateway.
    
- O endereço não pode ser manipulado por um provedor de catálogos de endereços no perfil atual.
    
Para obter mais informações, consulte [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md).
  
Os clientes chamam **IAddrBook:: CreateOneOff** para criar um identificador de entrada one-off para um endereço em uma mensagem de entrada quando: 
  
- O endereço é formatado como um endereço one-off.
    
- O endereço é formatado como um endereço de Internet.
    
Para obter mais informações, consulte [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md).
  
Para obter mais informações sobre identificadores e endereços de entrada únicos, consulte [identificadores de entrada únicos](one-off-entry-identifiers.md) e [endereços únicos](one-off-addresses.md).
  
As propriedades de um destinatário são uma combinação de propriedades do catálogo de endereços e propriedades específicas para destinatários. Todos os destinatários têm as propriedades de endereço base, atribuídas por provedores de catálogo de endereços. Quando uma entrada é usada como um destinatário para uma mensagem de saída, as propriedades de endereço base são copiadas para a estrutura **das ADRLIST** que armazena as propriedades de todos os destinatários de uma mensagem. 
  
Duas propriedades que são definidas especificamente para destinatários são **PR_RECIPIENT_TYPE** e **PR_RESPONSIBILITY**. **PR_RECIPIENT_TYPE** indica se um destinatário é um principal, uma cópia carbono, uma cópia oculta ou um destinatário de reenvio. Os três primeiros tipos são atribuídos aos destinatários nas mensagens que estão sendo enviadas pela primeira vez. 
  
Se um destinatário não recebe a mensagem e uma tentativa é feita para reenviá-la, o destinatário é copiado e seu tipo é definido como MAPI_P1 para indicar que se trata de um destinatário de reenvio. Se apenas alguns destinatários receberem uma mensagem, suas propriedades **PR_RECIPIENT_TYPE** serão marcadas com a adição do sinalizador MAPI_SUBMITTED quando a mensagem for reenviada. Os clientes são necessários para lidar com destinatários primários ou destinatários com seus **PR_RECIPIENT_TYPE** definidos como MAPI_TO. Todos os outros tipos são opcionais. 
  
 **PR_RESPONSIBILITY** é definido para indicar ao provedor de transporte se ele deve ou não controlar o envio ao destinatário. Quando uma mensagem de saída é enviada pela primeira vez, todos os destinatários definem **PR_RESPONSIBILITY** como false. Como um provedor de transporte alega a responsabilidade de enviar para um ou mais destinatários, suas propriedades **PR_RESPONSIBILITY** são definidas como true. 
  

