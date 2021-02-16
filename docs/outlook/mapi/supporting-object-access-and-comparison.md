---
title: Suporte ao acesso e à comparação de objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429030"
---
# <a name="supporting-object-access-and-comparison"></a>Suporte ao acesso e comparação de objetos

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de serviços podem usar os métodos [IMAPISupport::OpenEntry](imapisupport-openentry.md) e [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para abrir e comparar objetos que pertencem ao provedor ou a outros provedores: 
  
Assim [como IMAPISession::OpenEntry](imapisession-openentry.md) para clientes, os provedores podem usar o método **OpenEntry** do objeto de suporte para acessar qualquer objeto desde que saibam o identificador de entrada do objeto. Ao contrário do método de sessão, o método de suporte exige que você especifique um identificador de entrada válido no _parâmetro lpEntryID._ Não pode ser NULL. 
  
Para ilustrar como um provedor de transporte pode usar **IMAPISupport::OpenEntry,** considere o cenário a seguir. O provedor de transporte recebeu uma mensagem formatada no Formato Rich Text e não sabe se o destinatário de destino pode lidar com esse formato. Antes de entregar a mensagem, o provedor de transporte precisa fazer o seguinte:
  
1. Chame o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) da mensagem para acessar a tabela do destinatário e o identificador de entrada do destinatário, sua **propriedade PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. Passe o identificador de entrada **para IMAPISupport::OpenEntry** para abrir o destinatário, normalmente um usuário de mensagens ou uma lista de distribuição. O  _parâmetro lpInterface_ deve ser definido como NULL porque o provedor não pode saber com antecedência o tipo de objeto do destinatário. O método **OpenEntry** do objeto de suporte chama [IMAPISession::OpenEntry](imapisession-openentry.md) para determinar o provedor de agendas responsável pelo destinatário. Em seguida, o objeto session chama o método **OpenEntry** do provedor de agendas apropriado para abrir o destinatário e retornar um ponteiro de interface para o provedor de transporte. 
    
3. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do **destinatário** para recuperar sua PR_SEND_RICH_INFO ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) . Se **PR_SEND_RICH_INFO** for definido como TRUE, o destinatário poderá manipular texto formatado. 
    
Se tiver aberto vários objetos de outros provedores, talvez seja necessário descobrir se dois identificadores de entrada se referem ao mesmo objeto. Por exemplo, você pode ter um identificador de entrada de curto prazo e um identificador de entrada de longo prazo e esses identificadores podem ou não identificar o mesmo objeto. Para evitar o processamento redundante, chame o método [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para comparar esses identificadores de entrada. Você deve usar esse método para comparação do identificador de entrada porque os identificadores de entrada não podem ser comparados diretamente. 
  
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

