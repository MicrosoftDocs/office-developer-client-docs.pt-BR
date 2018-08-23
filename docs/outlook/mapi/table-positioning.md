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
ms.openlocfilehash: f7b2baa8cd78fbb8ace72fd0edb7c77f4c02a4c8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583859"
---
# <a name="table-positioning"></a><span data-ttu-id="9a74d-103">Posicionamento de tabelas</span><span class="sxs-lookup"><span data-stu-id="9a74d-103">Table Positioning</span></span>

  
  
<span data-ttu-id="9a74d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a74d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a74d-105">A posição atual dentro de uma tabela sempre é indicada por um cursor.</span><span class="sxs-lookup"><span data-stu-id="9a74d-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="9a74d-106">Não há um cursor para cada modo de exibição de uma tabela; seu valor é definido por implementador da tabela.</span><span class="sxs-lookup"><span data-stu-id="9a74d-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="9a74d-107">Quando um provedor de cliente ou de serviço usando a tabela faz uma chamada para alterar a posição da tabela, o valor do cursor é redefinido.</span><span class="sxs-lookup"><span data-stu-id="9a74d-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="9a74d-108">Posição de uma tabela pode ser alterada com:</span><span class="sxs-lookup"><span data-stu-id="9a74d-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="9a74d-109">Um indicador.</span><span class="sxs-lookup"><span data-stu-id="9a74d-109">A bookmark.</span></span>
    
- <span data-ttu-id="9a74d-110">Um valor fracionário.</span><span class="sxs-lookup"><span data-stu-id="9a74d-110">A fractional value.</span></span>
    
- <span data-ttu-id="9a74d-111">Um filtro.</span><span class="sxs-lookup"><span data-stu-id="9a74d-111">A filter.</span></span>
    

