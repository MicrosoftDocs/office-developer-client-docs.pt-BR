---
title: Selecionar uma pasta de recebimento
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
# <a name="selecting-a-receive-folder"></a>Selecionar uma pasta de recebimento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma pasta de recebimento é onde as mensagens de entrada de uma determinada classe são colocadas. Para as mensagens IPM e de relatórios relacionados, o MAPI atribui a caixa de entrada como a pasta de recebimento padrão. Para mensagens de relatório relacionadas e IPC, o MAPI atribui a pasta raiz do repositório de mensagens como a pasta de recebimento padrão. Você pode alterar essas atribuições ou fazer atribuições adicionais para outras classes de mensagens. Fazer atribuições explícitas de pastas de recebimento para as classes de mensagens com suporte do cliente é opcional.
  
Quando uma classe de mensagens de entrada não tem uma pasta de recebimento atribuída, o provedor de armazenamento de mensagens usa automaticamente a pasta de recebimento da classe que corresponde ao prefixo mais longo possível da classe de entrada. Por exemplo, se o cliente receber uma mensagem da classe IPM. Note. myDocument e a única pasta de recebimento estabelecida é a caixa de entrada de mensagens IPM, esta mensagem será colocada na caixa de entrada porque IPM. Note. mydocument deriva da classe base IPM.
  
Quando você estiver atribuindo uma pasta de recebimento para mensagens IPC, nunca use uma pasta da sub-árvore IPM. Essas pastas devem ser reservadas apenas para mensagens IPM. Use em vez de uma pasta contida na pasta raiz do repositório de mensagens. 
  
 **Para criar uma pasta de recebimento para uma classe de mensagem IPM**
  
1. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) com **PR_IPM_SUBTREE_ENTRYID** como o identificador de entrada para abrir a pasta raiz da sub-árvore IPM no repositório de mensagens. 
    
3. Chame [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento. 
    
4. Chame [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para sua classe de mensagem IPM. 
    
 **Para criar uma pasta de recebimento para uma classe de mensagem de IPC**
  
1. Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) com um identificador de entrada nulo para abrir a pasta raiz do repositório de mensagens. 
    
2. Chame [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) para criar a pasta de recebimento. 
    
3. Chame [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) para mapear a nova pasta para sua classe de mensagens de IPC. 
    
Atribua a pasta de recebimento que você usa para mensagens de relatórios relacionados. Por exemplo, se o cliente receber IPM. Observação mensagens, configure uma pasta de recebimento para o futuro IPM. Mensagens de observação e a mesma pasta de recebimento para mensagens de relatórios. IPM.
  

