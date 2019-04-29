---
title: Salvar uma mensagem na caixa de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407890"
---
# <a name="saving-a-message-in-the-inbox"></a>Salvar uma mensagem na caixa de entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para armazenar uma mensagem na caixa de entrada sem nenhum destinatário**
  
1. Chame [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar o identificador de entrada da caixa de entrada. 
    
2. Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir a caixa de entrada e recuperar um ponteiro para ela. 
    
3. Chame o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) da caixa de entrada para criar a mensagem. 
    
4. Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps da mensagem para adicionar o **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) e **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) Propriedades. 
    
5. Crie cada anexo, defina suas propriedades e salve-o. Para obter informações detalhadas sobre como adicionar anexos a mensagens, consulte [Creating a Message Attachment](creating-a-message-attachment.md).
    
6. Chame **IMessage:: SaveChanges** para salvar a mensagem. Nesse ponto, ele aparecerá na tabela de conteúdo da caixa de entrada. 
    
Se você deseja salvar um intermittantly de mensagem antes de exibi-lo na tabela de conteúdo da caixa de entrada, crie-o em uma pasta oculta, como a pasta raiz da sub-árvore IPM e, em seguida, mova-o para a caixa de entrada. 
  

