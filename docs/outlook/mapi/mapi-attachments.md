---
title: Anexos de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fd8075d2fddb7ada6803c869cbbd282c464e75bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585875"
---
# <a name="mapi-attachments"></a>Anexos de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns provedores de armazenamento de mensagem permitem que os clientes associar informações adicionadas na forma de arquivos, objetos OLE, mensagens ou dados binários de mensagens. Essas informações adicionadas são chamadas de anexos da mensagem. Como anexos são criados, mantidos e acessados apenas por meio de suas mensagens, eles são considerados subobjetos de mensagem. Em vez de um identificador de entrada de acesso, anexos tem um conhecido número sequencial como um número de anexo. Esse número identifica exclusivamente o anexo dentro de sua mensagem, mas não necessariamente dentro do repositório de mensagem. Duas mensagens diferentes podem ter diferentes anexos com o mesmo número de anexo. Números de anexo somente são válidos desde que a mensagem é aberta e são armazenados na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
  
Para acessar informações de resumo sobre todos os anexos da mensagem, clientes recuperam sua tabela de anexo. A tabela de anexo inclui informações que os clientes podem usar para acessar um anexo diretamente, como seu número de anexo e a chave do registro. Os clientes podem recuperar uma tabela de anexo por:
  
- Chamando **IMessage::GetAttachmentTable**. Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
- Chamando **IMAPIProp::OpenProperty**. Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Provedores de armazenamento de mensagem esperados para dar suporte a essas duas abordagens. A abordagem de **OpenProperty** requer que o chamador Especifica IID_IMAPITable como o identificador de interface e **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) como a marca de propriedade. **PR_MESSAGE_ATTACHMENTS** é uma propriedade de objeto de tabela que representa a tabela de anexos da mensagem. Provedores de armazenamento de mensagem são necessárias para definir **PR_MESSAGE_ATTACHMENTS** para cada mensagem e incluí-lo na matriz de marcas de propriedade retornado pelo método **IMAPIProp::GetPropList** . Para obter mais informações, consulte [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 **PR_MESSAGE_ATTACHMENTS** pode ser usado: 
  
- Com **IMAPIProp::OpenProperty** para acessar uma tabela de anexo ou destinatário. 
    
- Com **IMAPIProp::CopyTo** ou **IMAPIProp::CopyProps** para excluir ou incluir anexos ao copiar. Para obter mais informações, consulte [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Uma restrição subobjeto para indicar que a restrição filho deve ser aplicadas aos anexos.
    
Para obter mais informações, consulte [As tabelas de anexo](attachment-tables.md).
  

