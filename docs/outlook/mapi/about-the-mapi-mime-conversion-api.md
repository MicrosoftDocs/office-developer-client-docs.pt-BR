---
title: Sobre a API de conversão MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575263"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="701d5-103">Sobre a API de conversão MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="701d5-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="701d5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="701d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="701d5-105">A API de conversão de MIME MAPI permite que os provedores de email converter entre os objetos MIME e mensagens MAPI.</span><span class="sxs-lookup"><span data-stu-id="701d5-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="701d5-106">Ele fornece definições constantes, identificadores de classe e os identificadores de interface conforme mostrado na [Constantes de MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="701d5-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="701d5-107">Provedores de email devem criar uma instância de **[IConverterSession](iconvertersessioniunknown.md)** chamando-se a função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="701d5-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

