---
title: Suporte a texto RTF para provedores de repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349613"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="aaa69-103">Suporte a texto RTF para provedores de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="aaa69-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="aaa69-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaa69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaa69-105">Alguns aplicativos cliente permitem que os usuários usem texto em formato Rich Text (RTF) em suas mensagens.</span><span class="sxs-lookup"><span data-stu-id="aaa69-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="aaa69-106">Se o seu provedor de repositório de mensagens precisa suportar texto RTF em mensagens, ele precisa manipular a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), além da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aaa69-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="aaa69-107">Basicamente, isso significa armazenar as duas propriedades e certificar-se de que **PR_BODY** contém uma versão de texto sem formatação do texto no **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="aaa69-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="aaa69-108">A função [RTFSync](rtfsync.md) é útil para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="aaa69-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="aaa69-109">Há dois sinalizadores que podem ser definidos na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do objeto Message Store que informa aos clientes o que eles podem esperar do provedor de armazenamento de mensagens em relação ao **PR_BODY** e ao **PR_ RTF_COMPRESSED** Propriedades em mensagens no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="aaa69-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="aaa69-110">O sinalizador STORE_RTF_OK indica que o repositório pode gerar o valor da propriedade **PR_BODY** da propriedade **PR_RTF_COMPRESSED** dinamicamente, o que alivia os clientes do ônus de sincronizá-los explicitamente.</span><span class="sxs-lookup"><span data-stu-id="aaa69-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="aaa69-111">O sinalizador STORE_UNCOMPRESSED_RTF indica que o provedor de repositório de mensagens pode dar suporte a dados não compactados no **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="aaa69-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="aaa69-112">Provedores de repositório de mensagens que não dão suporte a texto RTF precisam excluir a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) quando a propriedade **PR_BODY** é alterada para interoperar corretamente com aplicativos clientes que oferecem suporte a texto RTF .</span><span class="sxs-lookup"><span data-stu-id="aaa69-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aaa69-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="aaa69-113">See also</span></span>



[<span data-ttu-id="aaa69-114">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="aaa69-114">Message Store Features</span></span>](message-store-features.md)

