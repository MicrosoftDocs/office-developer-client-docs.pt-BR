---
title: attConversationID e attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Última modificação: 12 de março de 2013'
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318414"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="5046f-103">attConversationID e attParentID</span><span class="sxs-lookup"><span data-stu-id="5046f-103">attConversationID and attParentID</span></span>

<span data-ttu-id="5046f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5046f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5046f-105">A chave de conversa de email do Windows para Workgroups 3,1 é uma cadeia de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="5046f-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="5046f-106">O equivalente MAPI é um valor binário.</span><span class="sxs-lookup"><span data-stu-id="5046f-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="5046f-107">Para fornecer compatibilidade com versões anteriores, a implementação do TNEF converte os dados binários em texto e adiciona um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="5046f-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5046f-108">As propriedades correspondentes em MAPI para as quais esses atributos TNEF são mapeados, PR_CONVERSATION_KEY e PR_PARENT_KEY, foram preteridos no Microsoft Exchange Server: o uso de **PR_CONVERSATION_KEY**, o [PidTagConversationKey canônica Propriedade](pidtagconversationkey-canonical-property.md), persiste no Outlook somente para localizar \*\*IPM. \*\*Mensagens de MessageManager.</span><span class="sxs-lookup"><span data-stu-id="5046f-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5046f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5046f-109">Remarks</span></span>

<span data-ttu-id="5046f-110">A propriedade **PR_CONVERSATION_KEY** é o precursor obsoleto do **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Propriedade canônica](pidtagconversationindex-canonical-property.md) e **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic canônica Propriedade](pidtagconversationtopic-canonical-property.md), que deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="5046f-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5046f-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="5046f-111">See also</span></span>

- [<span data-ttu-id="5046f-112">SubÁrvore IPM</span><span class="sxs-lookup"><span data-stu-id="5046f-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="5046f-113">Pastas especiais MAPI</span><span class="sxs-lookup"><span data-stu-id="5046f-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

