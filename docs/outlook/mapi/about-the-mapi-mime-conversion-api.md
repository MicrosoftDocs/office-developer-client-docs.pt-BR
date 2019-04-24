---
title: Sobre a API de conversão MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321816"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="1d8e9-103">Sobre a API de conversão MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="1d8e9-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="1d8e9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d8e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d8e9-105">A API de conversão MAPI-MIME permite que os provedores de email convertam objetos MIME e mensagens MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d8e9-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="1d8e9-106">Ele fornece definições constantes, identificadores de classe e identificadores de interface, conforme mostrado nas [constantes MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1d8e9-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="1d8e9-107">Os provedores de email devem Cocriar uma instância do **[IConverterSession](iconvertersessioniunknown.md)** chamando a função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="1d8e9-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

