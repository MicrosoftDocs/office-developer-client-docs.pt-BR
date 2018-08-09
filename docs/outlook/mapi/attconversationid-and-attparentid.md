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
ms.openlocfilehash: 2fd3e66e3171c677465a533ede3001cd0b28c8aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766190"
---
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="ca358-103">attConversationID e attParentID</span><span class="sxs-lookup"><span data-stu-id="ca358-103">attConversationID and attParentID</span></span>

<span data-ttu-id="ca358-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca358-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca358-105">A chave de conversa de email de 3.1 de grupos de trabalho do Windows é uma cadeia de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="ca358-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="ca358-106">O equivalente MAPI é um valor binário.</span><span class="sxs-lookup"><span data-stu-id="ca358-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="ca358-107">Para fornecer compatibilidade com versões anteriores, a implementação de TNEF converte os dados binários em texto e adiciona um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="ca358-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ca358-108">As propriedades correspondentes no MAPI para que esses atributos TNEF são mapeados, PR_CONVERSATION_KEY e PR_PARENT_KEY, foram preteridos no Microsoft Exchange Server: uso de **PR_CONVERSATION_KEY**, o [PidTagConversationKey canônico Propriedade](pidtagconversationkey-canonical-property.md), persistir somente no Outlook para localizar **IPM. MessageManager** mensagens.</span><span class="sxs-lookup"><span data-stu-id="ca358-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ca358-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca358-109">Remarks</span></span>

<span data-ttu-id="ca358-110">A propriedade **PR_CONVERSATION_KEY** é o contrário obsoleto precursor do **PR_CONVERSATION_INDEX**, [Propriedade canônico PidTagConversationIndex](pidtagconversationindex-canonical-property.md) e **PR_CONVERSATION_TOPIC**, [Mapipidtagconversationtopic canônico Propriedade](pidtagconversationtopic-canonical-property.md), que deve ser usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ca358-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca358-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca358-111">See also</span></span>

- [<span data-ttu-id="ca358-112">Subárvore IPM</span><span class="sxs-lookup"><span data-stu-id="ca358-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="ca358-113">Pastas especiais de MAPI</span><span class="sxs-lookup"><span data-stu-id="ca358-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

