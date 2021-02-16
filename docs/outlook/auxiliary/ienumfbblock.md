---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317623"
---
# <a name="ienumfbblock"></a><span data-ttu-id="1ba7e-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="1ba7e-102">IEnumFBBlock</span></span>

<span data-ttu-id="1ba7e-103">Oferece suporte ao acesso e enumeração de blocos de disponibilidade de dados de um usuário em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1ba7e-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1ba7e-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ba7e-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="1ba7e-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="1ba7e-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ba7e-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="1ba7e-107">Fornecido por:</span><span class="sxs-lookup"><span data-stu-id="1ba7e-107">Provided by:</span></span>  <br/> |<span data-ttu-id="1ba7e-108">Provedor de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="1ba7e-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="1ba7e-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="1ba7e-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1ba7e-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="1ba7e-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1ba7e-111">Vtable order</span><span class="sxs-lookup"><span data-stu-id="1ba7e-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1ba7e-112">Next</span><span class="sxs-lookup"><span data-stu-id="1ba7e-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="1ba7e-113">Obtém o próximo número específico de blocos de disponibilidade de dados em uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="1ba7e-114">Skip</span><span class="sxs-lookup"><span data-stu-id="1ba7e-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="1ba7e-115">Pula um número específico de blocos de disponibilidade de dados.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="1ba7e-116">Reset</span><span class="sxs-lookup"><span data-stu-id="1ba7e-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="1ba7e-117">Redefine o enumerador configurando o cursor para o início.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="1ba7e-118">Clone</span><span class="sxs-lookup"><span data-stu-id="1ba7e-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="1ba7e-119">Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definindo o cursor para o início do enumerador.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="1ba7e-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="1ba7e-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="1ba7e-121">Restringe a enumeração para um período específico.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ba7e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba7e-122">Remarks</span></span>

<span data-ttu-id="1ba7e-123">Uma enumeração contém blocos disponibilidade de dados que não ficam sobrepostos no período.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="1ba7e-124">Quando há itens sobrepostos em um calendário, o Outlook mescla esses itens para formar blocos de disponibilidade não sobrepostos na enumeração com base nesta ordem de prioridade: ausência temporária, ocupado, provisório.</span><span class="sxs-lookup"><span data-stu-id="1ba7e-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="1ba7e-125">Um provedor de disponibilidade obtém essa interface e a enumeração em um intervalo de tempo para o usuário por meio de [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="1ba7e-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ba7e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ba7e-126">See also</span></span>

- [<span data-ttu-id="1ba7e-127">Sobre a API do serviço de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="1ba7e-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="1ba7e-128">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="1ba7e-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="1ba7e-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="1ba7e-129">IFreeBusyData</span></span>](ifreebusydata.md)

