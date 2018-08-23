---
title: Suporte ao objeto de acesso e comparação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f33dcedae5ffe30b85a58d5248d239be81c8efc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575277"
---
# <a name="supporting-object-access-and-comparison"></a>Suporte ao objeto de acesso e comparação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de serviços podem usar os métodos [IMAPISupport::OpenEntry](imapisupport-openentry.md) e [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para abrir e comparar objetos que pertencem ao seu provedor ou para outros provedores: 
  
Como [IMAPISession::OpenEntry](imapisession-openentry.md) para clientes, provedores podem usar o método de **OpenEntry** do objeto seus suporte para acessar qualquer objeto tempo eles sabem identificador de entrada do objeto. Ao contrário do método de sessão, o método de suporte requer que você especifique um identificador de entrada válida no parâmetro _lpEntryID_ . Ele não pode ser NULL. 
  
Para ilustrar como um provedor de transporte pode usar **IMAPISupport::OpenEntry**, considere o seguinte cenário. O provedor de transporte recebeu uma mensagem formatada em formato Rich Text e não sabe se o destinatário de destino pode lidar com esse formato. Antes de entregar a mensagem, o provedor de transporte precisa fazer o seguinte:
  
1. Chame o método de [IMessage::GetRecipientTable](imessage-getrecipienttable.md) da mensagem para acessar a tabela de destinatários e o identificador de entrada do destinatário, sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
2. Passe o identificador de entrada para **IMAPISupport::OpenEntry** para abrir o destinatário, normalmente um uma lista de usuário ou de distribuição de mensagens. O parâmetro _lpInterface_ deve ser definido como NULL, porque o provedor não pode saber antes do tempo, o tipo de objeto do destinatário. O suporte ao método do objeto **OpenEntry** chama [IMAPISession::OpenEntry](imapisession-openentry.md) para determinar o provedor de catálogo de endereços responsável pelo destinatário. O objeto de sessão, em seguida, chama o método de **OpenEntry** do provedor de catálogo de endereço apropriado para abrir o destinatário e retornar um ponteiro de interface para o provedor de transporte. 
    
3. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do destinatário para recuperar sua propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Se **PR_SEND_RICH_INFO** for definido como TRUE, o destinatário pode lidar com texto formatado. 
    
Se você abrir vários objetos de outros fornecedores, você pode precisar descobrir se os dois identificadores de entrada se referir ao mesmo objeto. Por exemplo, talvez você tenha um identificador de entrada de curto prazo e um identificador de entrada de longo prazo e desses identificadores podem ou não podem identificar o mesmo objeto. Para evitar o processamento redundante, chame o método de [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) para comparar desses identificadores de entrada. Você deve usar esse método para comparação de identificador de entrada porque os identificadores de entrada não podem ser comparados diretamente. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

