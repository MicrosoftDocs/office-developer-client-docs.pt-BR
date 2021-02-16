---
title: Selecionando uma pasta de recebimento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428414"
---
# <a name="selecting-a-receive-folder"></a>Selecionando uma pasta de recebimento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma pasta de recebimento é onde as mensagens de entrada de uma classe específica são colocadas. Para mensagens de IPM e de relatório relacionadas, MAPI atribui a Caixa de Entrada como a pasta de recebimento padrão. Para mensagens de relatório relacionadas e IPC, MAPI atribui a pasta raiz do armazenamento de mensagens como a pasta de recebimento padrão. Você pode alterar essas atribuições ou fazer atribuições adicionais para outras classes de mensagem. Fazer atribuições de pasta de recebimento explícitas para as classes de mensagens com suporte do cliente é opcional.
  
Quando uma classe de mensagem de entrada não tem uma pasta de recebimento atribuída, o provedor de armazenamento de mensagens usa automaticamente a pasta de recebimento para a classe que corresponde ao prefixo mais longo possível da classe de entrada. Por exemplo, se seu cliente receber uma mensagem do IPM de classe. Note.MyDocument e a única pasta de recebimento estabelecida é a Caixa de Entrada para mensagens IPM. Essa mensagem será colocada na Caixa de Entrada porque iPM. Note.MyDocument é derivado do IPM de classe base.
  
Quando você estiver atribuindo uma pasta de recebimento para mensagens IPC, nunca use uma pasta da subárvore do IPM. Essas pastas devem ser reservadas apenas para mensagens IPM. Em vez disso, use uma pasta que está contida na pasta raiz do armazenamento de mensagens. 
  
 **Para criar uma pasta de recebimento para uma classe de mensagem do IPM**
  
1. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) . 
    
2. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) **com PR_IPM_SUBTREE_ENTRYID** como o identificador de entrada para abrir a pasta raiz da subárvore do IPM no repositório de mensagens. 
    
3. Chame [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento. 
    
4. Chame [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para sua classe de mensagem do IPM. 
    
 **Para criar uma pasta de recebimento para uma classe de mensagem IPC**
  
1. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo para abrir a pasta raiz do repositório de mensagens. 
    
2. Chame [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento. 
    
3. Chame [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para sua classe de mensagem IPC. 
    
Atribua a pasta de recebimento que você usa para mensagens para mensagens de relatório relacionadas. Por exemplo, se seu cliente receber IPM. Anote as mensagens, configurar uma pasta de recebimento para o IPM futuro. Anote as mensagens e a mesma pasta de recebimento para futuras mensagens Report.IPM.Note.
  

