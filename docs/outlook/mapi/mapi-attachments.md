---
title: Anexos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417830"
---
# <a name="mapi-attachments"></a>Anexos MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns provedores de armazenamento de mensagens permitem que os clientes associem informações adicionadas na forma de arquivos, objetos OLE, mensagens ou dados binários a mensagens. Essas informações adicionadas são chamadas de anexo de uma mensagem. Como os anexos são criados, mantidos e acessados somente por meio de suas mensagens, eles são considerados subobjetos de mensagem. Em vez de ter um identificador de entrada para acesso, os anexos têm um número sequencial conhecido como número de anexo. Esse número identifica exclusivamente o anexo dentro de sua mensagem, mas não necessariamente no armazenamento de mensagens. Duas mensagens diferentes podem ter anexos diferentes com o mesmo número de anexo. Os números de anexo só são válidos enquanto a mensagem está aberta e são armazenados na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
  
Para acessar informações de resumo sobre todos os anexos de uma mensagem, os clientes recuperam sua tabela de anexos. A tabela de anexos inclui informações que os clientes podem usar para acessar um anexo diretamente, como seu número de anexo e chave de registro. Os clientes podem recuperar uma tabela de anexos:
  
- Chamando **IMessage::GetAttachmentTable**. Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
- Chamando **IMAPIProp::OpenProperty**. Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Espera-se que os provedores de armazenamento de mensagens deem suporte a essas duas abordagens. A **abordagem OpenProperty** exige que o chamador especifique IID_IMAPITable como o identificador da interface e **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) como a marca de propriedade. **PR_MESSAGE_ATTACHMENTS** é uma propriedade de objeto de tabela que representa a tabela de anexos de uma mensagem. Os provedores de armazenamento  de mensagens são necessários para definir PR_MESSAGE_ATTACHMENTS para cada mensagem e incluí-la na matriz de marcas de propriedade retornadas do método **IMAPIProp::GetPropList.** Para obter mais informações, [consulte IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 **PR_MESSAGE_ATTACHMENTS** pode ser usado: 
  
- Com **IMAPIProp::OpenProperty** para acessar uma tabela de anexos ou destinatários. 
    
- Com **IMAPIProp::CopyTo** ou **IMAPIProp::CopyProps** para excluir ou incluir anexos ao copiar. Para obter mais informações, [consulte IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Em uma restrição de subobjeto para indicar que a restrição filha deve se aplicar a anexos.
    
Para obter mais informações, consulte [Tabelas de anexos.](attachment-tables.md)
  

