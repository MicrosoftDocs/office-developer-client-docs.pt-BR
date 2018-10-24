---
title: Salvar propriedades usadas com frequência
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5ef0da0c617bffc3820c7cd43f66ea07be2ad4a9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580457"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="1f2c2-103">Salvar propriedades usadas com frequência</span><span class="sxs-lookup"><span data-stu-id="1f2c2-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="1f2c2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f2c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f2c2-105">Melhorar o desempenho armazenando dados que leva tempo e recursos para recuperar e são acessados com frequência.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="1f2c2-106">Usar memória extra, em alguns casos, pode ser a melhor opção que repetido recuperações.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="1f2c2-107">Use cuidado e atendimento médico, ao criar um cache para armazenar esses dados.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="1f2c2-108">Tenha em mente que um cache criado de forma inadequada pode afetar negativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="1f2c2-109">Por exemplo, mais interpessoais clientes de mensagens (IPM) necessário exibir e abrir a subárvore IPM de pastas muitas vezes durante uma sessão típica.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="1f2c2-110">Você pode melhorar o desempenho, armazenando os identificadores de entrada para cada uma dessas pastas.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

