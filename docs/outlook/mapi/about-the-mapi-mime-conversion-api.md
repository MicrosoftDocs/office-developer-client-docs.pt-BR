---
title: Sobre a API de conversão MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766100"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="16ec8-103">Sobre a API de conversão MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="16ec8-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="16ec8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16ec8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16ec8-105">A API de conversão de MIME MAPI permite que os provedores de email converter entre os objetos MIME e mensagens MAPI.</span><span class="sxs-lookup"><span data-stu-id="16ec8-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="16ec8-106">Ele fornece definições constantes, identificadores de classe e os identificadores de interface conforme mostrado na [Constantes de MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="16ec8-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="16ec8-107">Provedores de email devem criar uma instância de **[IConverterSession](iconvertersessioniunknown.md)** chamando-se a função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="16ec8-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

