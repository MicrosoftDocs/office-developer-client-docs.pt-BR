---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765839"
---
# <a name="ienumfbblock"></a><span data-ttu-id="4c6ea-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="4c6ea-102">IEnumFBBlock</span></span>

<span data-ttu-id="4c6ea-103">Suporta acessando e enumerando blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4c6ea-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4c6ea-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c6ea-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="4c6ea-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="4c6ea-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4c6ea-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4c6ea-107">Provided by:</span><span class="sxs-lookup"><span data-stu-id="4c6ea-107">Provided by:</span></span>  <br/> |<span data-ttu-id="4c6ea-108">Provedor de livre/ocupado</span><span class="sxs-lookup"><span data-stu-id="4c6ea-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="4c6ea-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="4c6ea-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4c6ea-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="4c6ea-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4c6ea-111">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="4c6ea-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4c6ea-112">Next</span><span class="sxs-lookup"><span data-stu-id="4c6ea-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="4c6ea-113">Obtém o próximo número especificado de blocos de informações de disponibilidade de dados em uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="4c6ea-114">Ignorar</span><span class="sxs-lookup"><span data-stu-id="4c6ea-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="4c6ea-115">Ignora um número especificado de blocos de informações de disponibilidade de dados.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="4c6ea-116">Reset</span><span class="sxs-lookup"><span data-stu-id="4c6ea-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="4c6ea-117">Redefine o enumerador, definindo o cursor para o início.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="4c6ea-118">Clone</span><span class="sxs-lookup"><span data-stu-id="4c6ea-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="4c6ea-119">Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definir o cursor para o início do enumerador.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="4c6ea-120">Restringir</span><span class="sxs-lookup"><span data-stu-id="4c6ea-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="4c6ea-121">Restringe a enumeração para um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c6ea-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c6ea-122">Remarks</span></span>

<span data-ttu-id="4c6ea-123">Uma enumeração contém blocos de informações de disponibilidade de dados que não se sobreponham em tempo.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="4c6ea-124">Quando houver sobreposição de itens em um calendário, o Outlook mescla desses itens para formar não sobrepostos blocos de livre/ocupado na enumeração com base nesta ordem de precedência: fora do escritório, ocupado, provisório.</span><span class="sxs-lookup"><span data-stu-id="4c6ea-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="4c6ea-125">Um provedor de livre/ocupado obtém essa interface e a enumeração para um intervalo de tempo para um usuário por meio de [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="4c6ea-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c6ea-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c6ea-126">See also</span></span>

- [<span data-ttu-id="4c6ea-127">Sobre a API do serviço de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4c6ea-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="4c6ea-128">Constantes (API de livre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="4c6ea-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="4c6ea-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="4c6ea-129">IFreeBusyData</span></span>](ifreebusydata.md)

