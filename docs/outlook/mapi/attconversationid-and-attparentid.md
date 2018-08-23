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
ms.openlocfilehash: 14b93a952e4776716c333dc730144b55bcc61259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582711"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="ff3dc-103">attConversationID e attParentID</span><span class="sxs-lookup"><span data-stu-id="ff3dc-103">attConversationID and attParentID</span></span>

<span data-ttu-id="ff3dc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff3dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff3dc-105">A chave de conversa de email de 3.1 de grupos de trabalho do Windows é uma cadeia de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="ff3dc-106">O equivalente MAPI é um valor binário.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="ff3dc-107">Para fornecer compatibilidade com versões anteriores, a implementação de TNEF converte os dados binários em texto e adiciona um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ff3dc-108">As propriedades correspondentes no MAPI para que esses atributos TNEF são mapeados, PR_CONVERSATION_KEY e PR_PARENT_KEY, foram preteridos no Microsoft Exchange Server: uso de **PR_CONVERSATION_KEY**, o [PidTagConversationKey canônico Propriedade](pidtagconversationkey-canonical-property.md), persistir somente no Outlook para localizar **IPM. MessageManager** mensagens.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ff3dc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff3dc-109">Remarks</span></span>

<span data-ttu-id="ff3dc-110">A propriedade **PR_CONVERSATION_KEY** é o contrário obsoleto precursor do **PR_CONVERSATION_INDEX**, [Propriedade canônico PidTagConversationIndex](pidtagconversationindex-canonical-property.md) e **PR_CONVERSATION_TOPIC**, [Mapipidtagconversationtopic canônico Propriedade](pidtagconversationtopic-canonical-property.md), que deve ser usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ff3dc-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff3dc-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff3dc-111">See also</span></span>

- [<span data-ttu-id="ff3dc-112">Subárvore IPM</span><span class="sxs-lookup"><span data-stu-id="ff3dc-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="ff3dc-113">Pastas especiais de MAPI</span><span class="sxs-lookup"><span data-stu-id="ff3dc-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

