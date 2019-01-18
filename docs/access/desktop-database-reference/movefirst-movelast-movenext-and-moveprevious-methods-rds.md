---
title: Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716030"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="46ed3-102">Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (RDS)</span><span class="sxs-lookup"><span data-stu-id="46ed3-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>

<span data-ttu-id="46ed3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="46ed3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46ed3-104">Move para o primeiro, o último, o próximo ou o registro anterior em um objeto [Recordset](recordset-object-ado.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="46ed3-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ed3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46ed3-105">Syntax</span></span>

<span data-ttu-id="46ed3-106">*DataControl*. Conjunto de registros. {</span><span class="sxs-lookup"><span data-stu-id="46ed3-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="46ed3-107">Métodos MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="46ed3-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="46ed3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46ed3-108">Parameters</span></span>

|<span data-ttu-id="46ed3-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="46ed3-109">Parameter</span></span>|<span data-ttu-id="46ed3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="46ed3-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="46ed3-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="46ed3-111">*DataControl*</span></span> |<span data-ttu-id="46ed3-112">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="46ed3-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="46ed3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="46ed3-113">Remarks</span></span>

<span data-ttu-id="46ed3-114">Você pode usar os métodos **Move** com o **RDS. DataControl** objeto para navegar pelos registros de dados nos controles ligados a dados em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="46ed3-114">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> 

<span data-ttu-id="46ed3-115">Por exemplo, suponha que você exiba um **Recordset** em uma grade ligando a um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="46ed3-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="46ed3-116">Em seguida, é possível incluir botões Primeiro, Último, Próximo e Anterior que os usuários podem clicar para mover-se para o primeiro, o último, o próximo ou o registro anterior no **Recordset** exibido.</span><span class="sxs-lookup"><span data-stu-id="46ed3-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="46ed3-117">Isso é feito chamando-se os métodos **MoveFirst**, **MoveLast**, **MoveNext** e **MovePrevious** do objeto **RDS.DataControl** nos procedimentos onClick dos botões Primeiro, Último, Próximo e Anterior, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="46ed3-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="46ed3-118">O [Exemplo de Catálogo de Endereços](address-book-navigation-buttons.md) mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="46ed3-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

