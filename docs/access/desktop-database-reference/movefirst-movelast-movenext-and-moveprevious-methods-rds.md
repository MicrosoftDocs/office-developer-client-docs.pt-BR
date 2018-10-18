---
title: Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 02c6bc5ab4cc8357d7f349eb1698c2e6a026e173
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602850"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="abe7d-102">Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (RDS)</span><span class="sxs-lookup"><span data-stu-id="abe7d-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span></span>


<span data-ttu-id="abe7d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="abe7d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="abe7d-104">Move para o primeiro, o último, o próximo ou o registro anterior em um objeto [Recordset](recordset-object-ado.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="abe7d-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abe7d-105">Syntax</span></span>

<span data-ttu-id="abe7d-106">*DataControl*. Conjunto de registros. {</span><span class="sxs-lookup"><span data-stu-id="abe7d-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="abe7d-107">Métodos MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="abe7d-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="abe7d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abe7d-108">Parameters</span></span>

  - <span data-ttu-id="abe7d-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="abe7d-109">*DataControl*</span></span>

  - <span data-ttu-id="abe7d-110">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="abe7d-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="abe7d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="abe7d-111">Remarks</span></span>

<span data-ttu-id="abe7d-112"><<<<<<< Cabeça você pode usar os métodos **Move** com o **RDS. DataControl** objeto para navegar pelos registros de dados nos controles ligados a dados em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="abe7d-112"><<<<<<< HEAD You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a Web page.</span></span> <span data-ttu-id="abe7d-113">Por exemplo, suponha que você exiba um **Recordset** em uma grade ligando a um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="abe7d-113">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="abe7d-114">Em seguida, é possível incluir botões Primeiro, Último, Próximo e Anterior que os usuários podem clicar para mover-se para o primeiro, o último, o próximo ou o registro anterior no **Recordset** exibido.</span><span class="sxs-lookup"><span data-stu-id="abe7d-114">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="abe7d-115">Isso é feito chamando-se os métodos **MoveFirst**, **MoveLast**, **MoveNext** e **MovePrevious** do objeto **RDS.DataControl** nos procedimentos onClick dos botões Primeiro, Último, Próximo e Anterior, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="abe7d-115">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="abe7d-116">O [Exemplo de Catálogo de Endereços](address-book-navigation-buttons.md) mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="abe7d-116">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>
<span data-ttu-id="abe7d-117">=== Você pode usar os métodos **Move** com o **RDS. DataControl** objeto para navegar pelos registros de dados nos controles ligados a dados em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="abe7d-117">======= You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> <span data-ttu-id="abe7d-118">Por exemplo, suponha que você exiba um **Recordset** em uma grade ligando a um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="abe7d-118">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="abe7d-119">Em seguida, é possível incluir botões Primeiro, Último, Próximo e Anterior que os usuários podem clicar para mover-se para o primeiro, o último, o próximo ou o registro anterior no **Recordset** exibido.</span><span class="sxs-lookup"><span data-stu-id="abe7d-119">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="abe7d-120">Isso é feito chamando-se os métodos **MoveFirst**, **MoveLast**, **MoveNext** e **MovePrevious** do objeto **RDS.DataControl** nos procedimentos onClick dos botões Primeiro, Último, Próximo e Anterior, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="abe7d-120">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="abe7d-121">O [Exemplo de Catálogo de Endereços](address-book-navigation-buttons.md) mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="abe7d-121">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>
>>>>>>> <span data-ttu-id="abe7d-122">mestre</span><span class="sxs-lookup"><span data-stu-id="abe7d-122">master</span></span>

