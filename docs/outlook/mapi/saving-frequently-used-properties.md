---
title: Salvando propriedades usadas com frequência
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424550"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="c500d-103">Salvando propriedades usadas com frequência</span><span class="sxs-lookup"><span data-stu-id="c500d-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="c500d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c500d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c500d-105">Melhore o desempenho, armazenar dados que demoram tempo e recursos para recuperar e são acessados com frequência.</span><span class="sxs-lookup"><span data-stu-id="c500d-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="c500d-106">Às vezes, usar memória extra pode ser uma opção melhor que recuperações repetidas.</span><span class="sxs-lookup"><span data-stu-id="c500d-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="c500d-107">Seja cuidadoso ao criar um cache para armazenar esses dados.</span><span class="sxs-lookup"><span data-stu-id="c500d-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="c500d-108">Tenha em mente que um cache mal projetado pode afetar negativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="c500d-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="c500d-109">Por exemplo, a maioria dos clientes de mensagem interpersonal (IPM) precisa exibir e abrir a subárvore IPM de pastas muitas vezes durante uma sessão típica.</span><span class="sxs-lookup"><span data-stu-id="c500d-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="c500d-110">Você pode melhorar o desempenho, armazenar os identificadores de entrada para cada uma dessas pastas.</span><span class="sxs-lookup"><span data-stu-id="c500d-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

