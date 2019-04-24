---
title: Acesso e comparação de objetos de suporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349606"
---
# <a name="supporting-object-access-and-comparison"></a>Acesso e comparação de objetos de suporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de serviços podem usar os métodos [IMAPISupport:: OpenEntry](imapisupport-openentry.md) e [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) para abrir e comparar objetos que pertencem ao provedor ou a outros provedores: 
  
Como [IMAPISession:: OpenEntry](imapisession-openentry.md) para clientes, os provedores podem usar o método **OpenEntry** do objeto support para acessar qualquer objeto, desde que eles saibam o identificador de entrada do objeto. Ao contrário do método de sessão, o método de suporte exige que você especifique um identificador de entrada válido no parâmetro _lpEntryID_ . Ele não pode ser nulo. 
  
Para ilustrar como um provedor de transporte pode usar **IMAPISupport:: OpenEntry**, considere o cenário a seguir. O provedor de transporte recebeu uma mensagem formatada no formato Rich Text e não sabe se o destinatário de destino pode lidar com esse formato. Antes de entregar a mensagem, o provedor de transporte precisa fazer o seguinte:
  
1. Chame o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable da mensagem para acessar a tabela de destinatários e o identificador de entrada do destinatário, sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. Passe o identificador de entrada para **IMAPISupport:: OpenEntry** para abrir o destinatário, geralmente um usuário de mensagens ou uma lista de distribuição. O parâmetro _lpInterface_ deve ser definido como NULL porque o provedor não pode saber antecipadamente o tipo de objeto do destinatário. O método **OpenEntry** do objeto support chama [IMAPISession:: OpenEntry](imapisession-openentry.md) para determinar o provedor do catálogo de endereços responsável pelo destinatário. O objeto Session, em seguida, chama o método **OpenEntry** do provedor de catálogo de endereços apropriado para abrir o destinatário e retornar um ponteiro de interface para o provedor de transporte. 
    
3. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do destinatário para recuperar sua propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Se **PR_SEND_RICH_INFO** for definido como true, o destinatário poderá lidar com o texto formatado. 
    
Se você tiver aberto vários objetos de outros provedores, talvez seja necessário descobrir se dois identificadores de entrada se referem ao mesmo objeto. Por exemplo, você pode ter um identificador de entrada de curto prazo e um identificador de entrada de longo prazo e esses identificadores podem ou não identificar o mesmo objeto. Para evitar o processamento redundante, chame o método [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) para comparar esses identificadores de entrada. Você deve usar esse método para comparação de identificador de entrada porque os identificadores de entrada não podem ser comparados diretamente. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviço MAPI](mapi-service-providers.md)

