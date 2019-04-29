---
title: Definir a posição da tabela com um valor fracionário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437333"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="ce8e2-103">Definir a posição da tabela com um valor fracionário</span><span class="sxs-lookup"><span data-stu-id="ce8e2-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="ce8e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce8e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce8e2-105">Tabela os usuários podem mover para uma posição que representa uma porcentagem aproximada de linhas em relação ao total.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="ce8e2-106">Em vez de mover para uma linha exata, esse método de posicionamento divide a tabela em partes com base em frações.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="ce8e2-107">Tabela os usuários podem mover, por exemplo, para o ponto de meia-forma da tabela ou para a linha que é 7/8 da forma pela tabela.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="ce8e2-108">**Para mover o cursor um número aproximado de linhas**</span><span class="sxs-lookup"><span data-stu-id="ce8e2-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="ce8e2-109">Call [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="ce8e2-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="ce8e2-110">**SeekRowApprox** move para a linha que representa uma porcentagem específica de linhas em relação ao início da tabela.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="ce8e2-111">Essa porcentagem é especificada nos parâmetros _ulNumerator_ e _ulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="ce8e2-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="ce8e2-112">O **SeekRowApprox** é usado com frequência para implementar barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="ce8e2-113">**Para determinar a posição aproximada de uma tabela**</span><span class="sxs-lookup"><span data-stu-id="ce8e2-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="ce8e2-114">Call [IMAPITable:: QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="ce8e2-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="ce8e2-115">**QueryPosition** pode ser usado para informar o usuário sobre a posição atual.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="ce8e2-116">Ele define um valor fracionário com base no número de linhas na tabela e o número da linha atual.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="ce8e2-117">Espero que esse valor represente uma aproximação.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="ce8e2-118">Os implementadores de tabela são incentivados a não calcular a posição exata, pois as implementações precisas podem ser caras para invocar, especialmente em tabelas categorizadas.</span><span class="sxs-lookup"><span data-stu-id="ce8e2-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ce8e2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce8e2-119">See also</span></span>



[<span data-ttu-id="ce8e2-120">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="ce8e2-120">MAPI Tables</span></span>](mapi-tables.md)

