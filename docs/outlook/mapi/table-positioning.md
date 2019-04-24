---
title: Posicionamento de tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 656f696c58e9b62e7e601d7f531870b8c385e862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345651"
---
# <a name="table-positioning"></a><span data-ttu-id="12757-103">Posicionamento de tabelas</span><span class="sxs-lookup"><span data-stu-id="12757-103">Table Positioning</span></span>

  
  
<span data-ttu-id="12757-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12757-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12757-105">A posição atual dentro de uma tabela é sempre indicada por um cursor.</span><span class="sxs-lookup"><span data-stu-id="12757-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="12757-106">Há um cursor para cada modo de exibição de uma tabela; o valor é definido pelo implementador da tabela.</span><span class="sxs-lookup"><span data-stu-id="12757-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="12757-107">Quando um cliente ou provedor de serviço que usa a tabela faz uma chamada para alterar a posição da tabela, o valor do cursor é redefinido.</span><span class="sxs-lookup"><span data-stu-id="12757-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="12757-108">A posição de uma tabela pode ser alterada com:</span><span class="sxs-lookup"><span data-stu-id="12757-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="12757-109">Um indicador.</span><span class="sxs-lookup"><span data-stu-id="12757-109">A bookmark.</span></span>
    
- <span data-ttu-id="12757-110">Um valor fracionário.</span><span class="sxs-lookup"><span data-stu-id="12757-110">A fractional value.</span></span>
    
- <span data-ttu-id="12757-111">Um filtro.</span><span class="sxs-lookup"><span data-stu-id="12757-111">A filter.</span></span>
    

