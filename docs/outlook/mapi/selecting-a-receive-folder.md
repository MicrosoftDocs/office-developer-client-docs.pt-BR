---
title: Escolher uma pasta de recebimento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a4245b5dd1b70d4cf695190c65b447cf92566ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574479"
---
# <a name="selecting-a-receive-folder"></a>Escolher uma pasta de recebimento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma pasta de recebimento é onde as mensagens recebidas de uma determinada classe são colocadas. Para IPM e mensagens de relatório relacionado, MAPI atribui a caixa de entrada, como o padrão de pasta de recebimento. Para CPI e mensagens de relatório relacionado, MAPI atribui a pasta raiz do armazenamento de mensagens, como o padrão de pasta de recebimento. Você pode alterar essas atribuições ou fazer atribuições adicionais para outras classes de mensagem. Fazendo explícitas receber atribuições de pasta para seu cliente com suporte a mensagem classes é opcional.
  
Quando uma classe de mensagem de entrada não tiver uma pasta de recebimento atribuída, o provedor de armazenamento de mensagem usa automaticamente a pasta de recebimento para a classe que corresponde ao prefixo possível mais longo da classe recebida. Por exemplo, se o seu cliente recebe uma mensagem da classe IPM. Recebe Note.MyDocument e a única pasta que tenha sido estabelecida é a caixa de entrada para mensagens IPM, esta mensagem será colocada na caixa de entrada porque IPM. Note.MyDocument derivada da classe base IPM.
  
Quando você estiver atribuindo uma pasta de recebimento de mensagens de CPI, nunca use uma pasta de subárvore IPM. Essas pastas devem ser reservadas para apenas para mensagens IPM. Use uma pasta que está contida dentro da pasta raiz do repositório de mensagem. 
  
 **Para criar uma pasta de recebimento para uma classe de mensagem IPM**
  
1. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) com **PR_IPM_SUBTREE_ENTRYID** como o identificador de entrada para abrir a pasta de raiz da subárvore IPM no repositório de mensagem. 
    
3. [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento de chamadas. 
    
4. Chame [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta à sua classe de mensagem IPM. 
    
 **Para criar uma pasta de recebimento para uma classe de mensagem CPI**
  
1. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo para abrir a pasta raiz do repositório de mensagem. 
    
2. [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento de chamadas. 
    
3. Chame [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para a classe de mensagem do CPI. 
    
Atribua a pasta de recebimento que você usa para mensagens para mensagens de relatório relacionado. Por exemplo, se o seu cliente recebe IPM. Pasta de recebimento de mensagens de anotação, definir um para futura IPM. Mensagens de observação e o mesmo receberão a pasta para as mensagens futuras do Report.IPM.Note.
  

