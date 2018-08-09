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
ms.openlocfilehash: c8d46ac6f47eb4dc68aebfa4562403ef1b738213
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766387"
---
# <a name="deleting-a-message"></a><span data-ttu-id="c8d00-103">Excluir uma mensagem</span><span class="sxs-lookup"><span data-stu-id="c8d00-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="c8d00-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8d00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8d00-105">Um cliente pode excluir uma mensagem quando ele é aberto e o usuário é lê-lo, ou quando ela é fechada e o usuário está exibindo a tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c8d00-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="c8d00-106">Para proteger um usuário removam inadvertidamente uma mensagem, MAPI define a exclusão da mensagem como um processo de duas etapas:</span><span class="sxs-lookup"><span data-stu-id="c8d00-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="c8d00-107">Marcar uma mensagem para exclusão, movendo-o para a pasta que foi designada como a pasta Itens excluídos — a pasta cujo identificador de entrada é armazenado na propriedade **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c8d00-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="c8d00-108">Remove a mensagem chamando o método [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) .</span><span class="sxs-lookup"><span data-stu-id="c8d00-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="c8d00-109">Quando um usuário escolher excluir uma mensagem em uma pasta diferente da pasta Itens excluídos, você deve marcá-la para exclusão.</span><span class="sxs-lookup"><span data-stu-id="c8d00-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="c8d00-110">Somente quando o usuário seleciona a mensagens de dentro da pasta Itens excluídos devem as mensagens ser removidas fisicamente a estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8d00-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="c8d00-111">Você pode solicitar o usuário para verificar que o usuário realmente foi projetado para executar a exclusão.</span><span class="sxs-lookup"><span data-stu-id="c8d00-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="c8d00-112">**Para excluir uma mensagem**</span><span class="sxs-lookup"><span data-stu-id="c8d00-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="c8d00-113">Com o usuário, confirme que a exclusão iminente é intencional.</span><span class="sxs-lookup"><span data-stu-id="c8d00-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="c8d00-114">Determine a pasta pai da pasta a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c8d00-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="c8d00-115">Se for a pasta Itens excluídos ou uma subpasta dentro da pasta Itens excluídos, chame [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) para remover a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c8d00-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="c8d00-116">Se a pasta não está contida dentro da pasta Itens excluídos, chame [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) com o sinalizador MESSAGE_MOVE definido realocar a mensagem para a pasta Itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="c8d00-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

