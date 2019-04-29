---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427133"
---
# <a name="attattachrenddata"></a><span data-ttu-id="06af0-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="06af0-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="06af0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06af0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06af0-105">O atributo **attAttachRenddata** é codificado como uma estrutura **RENDDATA** que descreve como e onde o anexo é renderizado no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="06af0-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="06af0-106">A estrutura **RENDDATA** é simplesmente codificada no fluxo TNEF como **sizeof (RENDDATA)** bytes, começando com o primeiro membro da estrutura **RENDDATA** .</span><span class="sxs-lookup"><span data-stu-id="06af0-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="06af0-107">Se o valor do membro **dwFlags** da estrutura **RENDDATA** for definido como **MAC_BINARY**, os dados do seguinte anexo serão armazenados no formato MacBinary; caso contrário, os dados de anexo serão codificados como de costume.</span><span class="sxs-lookup"><span data-stu-id="06af0-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

