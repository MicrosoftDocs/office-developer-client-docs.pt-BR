---
title: Salvar uma mensagem na caixa de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e79133ed4928495dcf75b59877a82d3228773883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586281"
---
# <a name="saving-a-message-in-the-inbox"></a>Salvar uma mensagem na caixa de entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para armazenar uma mensagem na caixa de entrada sem quaisquer destinatários**
  
1. Chame [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar o identificador de entrada da caixa de entrada. 
    
2. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a caixa de entrada e recuperar um ponteiro para ele. 
    
3. Chame o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) da caixa de entrada para criar a mensagem. 
    
4. Chamar o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da mensagem para adicionar a configuração **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) e **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) propriedades. 
    
5. Criar cada anexo, defina suas propriedades e salvá-lo. Para obter informações detalhadas sobre como adicionar anexos de mensagens, consulte [Criando um anexo da mensagem](creating-a-message-attachment.md).
    
6. Chame **IMessage::SaveChanges** para salvar a mensagem. Neste ponto, ele aparecerá na tabela de conteúdo de caixa de entrada. 
    
Se você deseja salvar uma mensagem intermittantly antes de ele ter que aparecem na tabela de conteúdo da caixa de entrada, criá-lo em vez disso, em uma pasta oculta como a pasta raiz da subárvore IPM e depois movê-lo para a caixa de entrada. 
  

