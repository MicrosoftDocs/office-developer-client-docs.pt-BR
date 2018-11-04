---
title: Evento EndOfRecordset (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36babff0c6de48e0539375caaad367698906e3fd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950184"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="23499-102">Evento EndOfRecordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="23499-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="23499-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="23499-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23499-104">O evento **EndOfRecordset** é chamado quando houver uma tentativa de mover para uma linha após o final do [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="23499-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="23499-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23499-105">Syntax</span></span>

<span data-ttu-id="23499-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="23499-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="23499-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23499-107">Parameters</span></span>

|<span data-ttu-id="23499-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="23499-108">Parameter</span></span>|<span data-ttu-id="23499-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="23499-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="23499-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="23499-110">*fMoreData*</span></span> |<span data-ttu-id="23499-111">Uma **VARIANT\_BOOL** valor que, se definida como VARIANT\_TRUE, indica que mais linhas foram adicionadas ao **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="23499-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="23499-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="23499-112">*adStatus*</span></span> |<span data-ttu-id="23499-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="23499-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="23499-114">Quando **EndOfRecordset** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="23499-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="23499-115">Será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação que provocou esse evento.</span><span class="sxs-lookup"><span data-stu-id="23499-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="23499-116">Antes que **EndOfRecordset** seja retornado, configure esse parâmetro como **adStatusUnwantedEvent** para impedir as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="23499-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="23499-117">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="23499-117">*pRecordset*</span></span> | <span data-ttu-id="23499-p102">Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="23499-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="23499-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="23499-120">Remarks</span></span>

<span data-ttu-id="23499-121">Pode ocorrer um evento **EndOfRecordset** se a operação [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) falhar.</span><span class="sxs-lookup"><span data-stu-id="23499-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="23499-122">Esse manipulador eventos é chamada quando é feita uma tentativa de mover após o final do objeto **Recordset**, talvez como resultado de chamar **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="23499-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="23499-123">No entanto, enquanto estiver nesse evento, você poderia recuperar mais registros de um banco de dados e anexá-los final do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="23499-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="23499-124">Nesse caso, defina *fMoreData* como VARIANT\_TRUE e o retorno de **EndOfRecordset**.</span><span class="sxs-lookup"><span data-stu-id="23499-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="23499-125">Em seguida, chame **MoveNext** novamente para acessar os registros recém-recuperados.</span><span class="sxs-lookup"><span data-stu-id="23499-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

