---
title: Definir uma posição de tabela com um valor fracionado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 104de38a41408091a6fbb69995de4f41f6fea6a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770386"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="052e6-103">Definir uma posição de tabela com um valor fracionado</span><span class="sxs-lookup"><span data-stu-id="052e6-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="052e6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="052e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="052e6-105">Os usuários da tabela podem mover para uma posição que representa um percentual aproximado de linhas em relação à total.</span><span class="sxs-lookup"><span data-stu-id="052e6-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="052e6-106">Em vez de mover para uma linha exata, esse método de posicionamento divide a tabela em partes com base em frações.</span><span class="sxs-lookup"><span data-stu-id="052e6-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="052e6-107">Os usuários da tabela podem mover, por exemplo, para o ponto de meia vias de uma tabela ou na linha que é 7/8 da maneira como a tabela.</span><span class="sxs-lookup"><span data-stu-id="052e6-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="052e6-108">**Para mover o cursor um número aproximado de linhas**</span><span class="sxs-lookup"><span data-stu-id="052e6-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="052e6-109">Chame [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="052e6-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="052e6-110">**SeekRowApprox** move para a linha que representa um percentual específico de linhas em relação ao início da tabela.</span><span class="sxs-lookup"><span data-stu-id="052e6-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="052e6-111">Essa porcentagem é especificada nos parâmetros _ulNumerator_ e _ulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="052e6-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="052e6-112">**SeekRowApprox** é usado com frequência para implementar as barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="052e6-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="052e6-113">**Para determinar a posição de uma tabela aproximado**</span><span class="sxs-lookup"><span data-stu-id="052e6-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="052e6-114">Chame [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="052e6-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="052e6-115">**QueryPosition** pode ser usado para informar ao usuário da posição atual.</span><span class="sxs-lookup"><span data-stu-id="052e6-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="052e6-116">Ele define um valor fracionário com base no número de linhas na tabela e o número da linha atual.</span><span class="sxs-lookup"><span data-stu-id="052e6-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="052e6-117">Espere que esse valor representa uma aproximação.</span><span class="sxs-lookup"><span data-stu-id="052e6-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="052e6-118">Implementadores de tabela são incentivados não para calcular a posição exata como implementações precisas podem ser caras de invocar, especialmente em tabelas categorizadas.</span><span class="sxs-lookup"><span data-stu-id="052e6-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="052e6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="052e6-119">See also</span></span>



[<span data-ttu-id="052e6-120">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="052e6-120">MAPI Tables</span></span>](mapi-tables.md)

