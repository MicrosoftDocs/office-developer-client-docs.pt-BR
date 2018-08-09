---
title: Suporte a texto RTF para provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770562"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="a7980-103">Suporte a texto RTF para provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="a7980-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="a7980-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7980-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7980-105">Alguns aplicativos de cliente permitem que os usuários utilizem o formato Rich Text (RTF) texto em suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="a7980-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="a7980-106">Se sua mensagem armazenar as necessidades do provedor para dar suporte ao texto RTF em mensagens, ele precisa lidar com a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), além da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a7980-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="a7980-107">Basicamente, isso significa armazenar ambas as propriedades e certificando-se de que **PR_BODY** contém uma versão de texto sem formatação do texto em **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a7980-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="a7980-108">A função [RTFSync](rtfsync.md) é útil para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="a7980-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="a7980-109">Há dois sinalizadores que podem ser definidos na propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do objeto repositório de mensagens que informam os clientes que eles podem esperar do provedor de repositório de mensagem com relação a **PR_BODY** e **PR_ RTF_COMPRESSED** propriedades em mensagens no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a7980-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="a7980-110">O sinalizador STORE_RTF_OK indica que o repositório pode gerar o valor da propriedade **PR_BODY** da propriedade **PR_RTF_COMPRESSED** dinamicamente, que libera os clientes da carga de sincronizá-los explicitamente.</span><span class="sxs-lookup"><span data-stu-id="a7980-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="a7980-111">O sinalizador STORE_UNCOMPRESSED_RTF indica que o provedor de armazenamento de mensagens pode oferecer suporte a dados descompactados em **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="a7980-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="a7980-112">Provedores de armazenamento de mensagem que não têm suporte para texto RTF necessário excluir a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) quando a propriedade **PR_BODY** é alterada para adequadamente interoperar com os aplicativos cliente que têm suporte para texto RTF .</span><span class="sxs-lookup"><span data-stu-id="a7980-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7980-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7980-113">See also</span></span>



[<span data-ttu-id="a7980-114">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="a7980-114">Message Store Features</span></span>](message-store-features.md)

