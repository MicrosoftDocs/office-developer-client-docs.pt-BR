---
title: Evento EndOfRecordset (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293557"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="389f6-102">Evento EndOfRecordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="389f6-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="389f6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="389f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="389f6-104">O evento **EndOfRecordset** é chamado quando houver uma tentativa de mover para uma linha após o final do [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="389f6-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="389f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="389f6-105">Syntax</span></span>

<span data-ttu-id="389f6-106">EndOfRecordset*fMoreData*, *adStatus*, \*\* precaboset</span><span class="sxs-lookup"><span data-stu-id="389f6-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="389f6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="389f6-107">Parameters</span></span>

|<span data-ttu-id="389f6-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="389f6-108">Parameter</span></span>|<span data-ttu-id="389f6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="389f6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="389f6-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="389f6-110">*fMoreData*</span></span> |<span data-ttu-id="389f6-111">Um **valor\_booliano Variant** que, se definido como\_Variant true, indica que mais linhas foram adicionadas ao **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="389f6-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="389f6-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="389f6-112">*adStatus*</span></span> |<span data-ttu-id="389f6-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="389f6-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="389f6-114">Quando **EndOfRecordset** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="389f6-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="389f6-115">Será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação que provocou esse evento.</span><span class="sxs-lookup"><span data-stu-id="389f6-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="389f6-116">Antes que **EndOfRecordset** seja retornado, configure esse parâmetro como **adStatusUnwantedEvent** para impedir as notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="389f6-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="389f6-117">*precaboset*</span><span class="sxs-lookup"><span data-stu-id="389f6-117">*pRecordset*</span></span> | <span data-ttu-id="389f6-p102">Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="389f6-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="389f6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="389f6-120">Remarks</span></span>

<span data-ttu-id="389f6-121">Pode ocorrer um evento **EndOfRecordset** se a operação [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) falhar.</span><span class="sxs-lookup"><span data-stu-id="389f6-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="389f6-122">Esse manipulador eventos é chamada quando é feita uma tentativa de mover após o final do objeto **Recordset**, talvez como resultado de chamar **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="389f6-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="389f6-123">No entanto, enquanto estiver nesse evento, você poderia recuperar mais registros de um banco de dados e anexá-los final do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="389f6-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="389f6-124">Nesse caso, defina *fMoreData* como Variant\_true e retorne de **EndOfRecordset**.</span><span class="sxs-lookup"><span data-stu-id="389f6-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="389f6-125">Em seguida, chame **MoveNext** novamente para acessar os registros recém-recuperados.</span><span class="sxs-lookup"><span data-stu-id="389f6-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

