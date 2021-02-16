---
title: Excluindo uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433161"
---
# <a name="deleting-a-message"></a>Excluindo uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode excluir uma mensagem quando ela estiver aberta e o usuário a estiver lendo ou quando estiver fechada e o usuário estiver exibindo o índice. Para proteger um usuário de remover inadvertidamente uma mensagem, o MAPI define a exclusão de mensagens como um processo de duas etapas:
  
1. Marque uma mensagem para exclusão movendo-a para a pasta que foi designada como a pasta Itens Excluídos — a pasta cujo identificador de entrada é armazenado na propriedade **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) . 
    
2. Remova a mensagem chamando o [método IMAPIFolder::D eleteMessages.](imapifolder-deletemessages.md) 
    
Quando um usuário optar por excluir uma mensagem em uma pasta diferente da pasta Itens Excluídos, marque-a para exclusão. Somente quando um usuário seleciona mensagens de dentro da pasta Itens Excluídos caso as mensagens sejam fisicamente removidas da estação de trabalho. Você pode solicitar ao usuário para verificar se o usuário realmente pretendia executar a exclusão.
  
 **Para excluir uma mensagem**
  
1. Confirme com o usuário que a exclusão iminente é intencional.
    
2. Determine o pai da pasta a ser excluída. Se for a pasta Itens Excluídos ou uma subpasta dentro da pasta Itens Excluídos, chame [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) para remover a mensagem. 
    
3. Se a pasta não estiver contida na pasta Itens [Excluídos, chame IMAPIFolder::CopyMessages](imapifolder-copymessages.md) com o sinalizador MESSAGE_MOVE definido para realocar a mensagem para a pasta Itens Excluídos. 
    

