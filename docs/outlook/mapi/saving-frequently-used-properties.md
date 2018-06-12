---
title: Salvando frequentemente usados propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a5fa4510f0bcad69bc17b8ac19433f66ec763fba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770285"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="37624-103">Salvando frequentemente usados propriedades</span><span class="sxs-lookup"><span data-stu-id="37624-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="37624-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="37624-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="37624-105">Melhorar o desempenho armazenando dados que leva tempo e recursos para recuperar e são acessados com frequência.</span><span class="sxs-lookup"><span data-stu-id="37624-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="37624-106">Usar memória extra, em alguns casos, pode ser a melhor opção que repetido recuperações.</span><span class="sxs-lookup"><span data-stu-id="37624-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="37624-107">Use cuidado e atendimento médico, ao criar um cache para armazenar esses dados.</span><span class="sxs-lookup"><span data-stu-id="37624-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="37624-108">Tenha em mente que um cache criado de forma inadequada pode afetar negativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="37624-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="37624-109">Por exemplo, mais interpessoais clientes de mensagens (IPM) necessário exibir e abrir a subárvore IPM de pastas muitas vezes durante uma sessão típica.</span><span class="sxs-lookup"><span data-stu-id="37624-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="37624-110">Você pode melhorar o desempenho, armazenando os identificadores de entrada para cada uma dessas pastas.</span><span class="sxs-lookup"><span data-stu-id="37624-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

