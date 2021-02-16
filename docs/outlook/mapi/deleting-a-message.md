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
# <a name="deleting-a-message"></a><span data-ttu-id="1c351-103">Excluindo uma mensagem</span><span class="sxs-lookup"><span data-stu-id="1c351-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="1c351-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c351-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c351-105">Um cliente pode excluir uma mensagem quando ela estiver aberta e o usuário a estiver lendo ou quando estiver fechada e o usuário estiver exibindo o índice.</span><span class="sxs-lookup"><span data-stu-id="1c351-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="1c351-106">Para proteger um usuário de remover inadvertidamente uma mensagem, o MAPI define a exclusão de mensagens como um processo de duas etapas:</span><span class="sxs-lookup"><span data-stu-id="1c351-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="1c351-107">Marque uma mensagem para exclusão movendo-a para a pasta que foi designada como a pasta Itens Excluídos — a pasta cujo identificador de entrada é armazenado na propriedade **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="1c351-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="1c351-108">Remova a mensagem chamando o [método IMAPIFolder::D eleteMessages.](imapifolder-deletemessages.md)</span><span class="sxs-lookup"><span data-stu-id="1c351-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="1c351-109">Quando um usuário optar por excluir uma mensagem em uma pasta diferente da pasta Itens Excluídos, marque-a para exclusão.</span><span class="sxs-lookup"><span data-stu-id="1c351-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="1c351-110">Somente quando um usuário seleciona mensagens de dentro da pasta Itens Excluídos caso as mensagens sejam fisicamente removidas da estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1c351-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="1c351-111">Você pode solicitar ao usuário para verificar se o usuário realmente pretendia executar a exclusão.</span><span class="sxs-lookup"><span data-stu-id="1c351-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="1c351-112">**Para excluir uma mensagem**</span><span class="sxs-lookup"><span data-stu-id="1c351-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="1c351-113">Confirme com o usuário que a exclusão iminente é intencional.</span><span class="sxs-lookup"><span data-stu-id="1c351-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="1c351-114">Determine o pai da pasta a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="1c351-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="1c351-115">Se for a pasta Itens Excluídos ou uma subpasta dentro da pasta Itens Excluídos, chame [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) para remover a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c351-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="1c351-116">Se a pasta não estiver contida na pasta Itens [Excluídos, chame IMAPIFolder::CopyMessages](imapifolder-copymessages.md) com o sinalizador MESSAGE_MOVE definido para realocar a mensagem para a pasta Itens Excluídos.</span><span class="sxs-lookup"><span data-stu-id="1c351-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

