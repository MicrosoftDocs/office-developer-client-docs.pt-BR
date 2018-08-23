---
title: Excluir uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ad891a9884e72aa352dc114232cd5951c590272f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585098"
---
# <a name="deleting-a-message"></a>Excluir uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode excluir uma mensagem quando ele é aberto e o usuário é lê-lo, ou quando ela é fechada e o usuário está exibindo a tabela de conteúdo. Para proteger um usuário removam inadvertidamente uma mensagem, MAPI define a exclusão da mensagem como um processo de duas etapas:
  
1. Marcar uma mensagem para exclusão, movendo-o para a pasta que foi designada como a pasta Itens excluídos — a pasta cujo identificador de entrada é armazenado na propriedade **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)). 
    
2. Remove a mensagem chamando o método [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) . 
    
Quando um usuário escolher excluir uma mensagem em uma pasta diferente da pasta Itens excluídos, você deve marcá-la para exclusão. Somente quando o usuário seleciona a mensagens de dentro da pasta Itens excluídos devem as mensagens ser removidas fisicamente a estação de trabalho. Você pode solicitar o usuário para verificar que o usuário realmente foi projetado para executar a exclusão.
  
 **Para excluir uma mensagem**
  
1. Com o usuário, confirme que a exclusão iminente é intencional.
    
2. Determine a pasta pai da pasta a ser excluído. Se for a pasta Itens excluídos ou uma subpasta dentro da pasta Itens excluídos, chame [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) para remover a mensagem. 
    
3. Se a pasta não está contida dentro da pasta Itens excluídos, chame [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) com o sinalizador MESSAGE_MOVE definido realocar a mensagem para a pasta Itens excluídos. 
    

