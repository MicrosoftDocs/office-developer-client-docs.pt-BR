---
title: Posicionamento de tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cec0b3584c6c19abb5f7421f1db0b06c877bb9ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770577"
---
# <a name="table-positioning"></a><span data-ttu-id="fcec8-103">Posicionamento de tabelas</span><span class="sxs-lookup"><span data-stu-id="fcec8-103">Table Positioning</span></span>

  
  
<span data-ttu-id="fcec8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fcec8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fcec8-105">A posição atual dentro de uma tabela sempre é indicada por um cursor.</span><span class="sxs-lookup"><span data-stu-id="fcec8-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="fcec8-106">Não há um cursor para cada modo de exibição de uma tabela; seu valor é definido por implementador da tabela.</span><span class="sxs-lookup"><span data-stu-id="fcec8-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="fcec8-107">Quando um provedor de cliente ou de serviço usando a tabela faz uma chamada para alterar a posição da tabela, o valor do cursor é redefinido.</span><span class="sxs-lookup"><span data-stu-id="fcec8-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="fcec8-108">Posição de uma tabela pode ser alterada com:</span><span class="sxs-lookup"><span data-stu-id="fcec8-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="fcec8-109">Um indicador.</span><span class="sxs-lookup"><span data-stu-id="fcec8-109">A bookmark.</span></span>
    
- <span data-ttu-id="fcec8-110">Um valor fracionário.</span><span class="sxs-lookup"><span data-stu-id="fcec8-110">A fractional value.</span></span>
    
- <span data-ttu-id="fcec8-111">Um filtro.</span><span class="sxs-lookup"><span data-stu-id="fcec8-111">A filter.</span></span>
    

