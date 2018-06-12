---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d8c6699ac1bc5687b1c885d156535e5b54b93140
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766199"
---
# <a name="attattachrenddata"></a><span data-ttu-id="20d1b-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="20d1b-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="20d1b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20d1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20d1b-105">O atributo **attAttachRenddata** é codificado como uma estrutura **RENDDATA** que descreve como e onde o anexo é processado no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="20d1b-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="20d1b-106">A estrutura **RENDDATA** é simplesmente codificada no stream TNEF como bytes **sizeof(RENDDATA)** começando com o primeiro membro da estrutura **RENDDATA** .</span><span class="sxs-lookup"><span data-stu-id="20d1b-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="20d1b-107">Se o valor do membro de **dwFlags** da estrutura **RENDDATA** é definido como **MAC_BINARY**, em seguida, os dados do anexo a seguir são armazenados no formato MacBinary; Caso contrário, os dados do anexo são codificados como de costume.</span><span class="sxs-lookup"><span data-stu-id="20d1b-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

