---
title: Eventos WillChangeField e FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c6f6d0f44000c0e40f93b7acfc461c7e3fb4e9c
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949835"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="06017-102">Eventos WillChangeField e FieldChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="06017-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>

<span data-ttu-id="06017-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="06017-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06017-p101">O evento **WillChangeField** é chamado antes que uma operação pendente altere o valor de um ou mais objetos [Field](field-object-ado.md) em [Recordset](recordset-object-ado.md). O evento **FieldChangeComplete** é chamado depois que o valor de um ou mais objetos **Field** tiver sido alterado.</span><span class="sxs-lookup"><span data-stu-id="06017-p101">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md). The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="06017-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06017-106">Syntax</span></span>

<span data-ttu-id="06017-107">De*cFields*, *campos*, de WillChangeField *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="06017-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="06017-108">FieldChangeComplete*cFields*, *campos*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="06017-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="06017-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06017-109">Parameters</span></span>

|<span data-ttu-id="06017-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="06017-110">Parameter</span></span>|<span data-ttu-id="06017-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="06017-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="06017-112">*cFields*</span><span class="sxs-lookup"><span data-stu-id="06017-112">*cFields*</span></span> |<span data-ttu-id="06017-113">Um **Long** que indica o número de objetos **Field** em *Fields*.</span><span class="sxs-lookup"><span data-stu-id="06017-113">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>|
|<span data-ttu-id="06017-114">*Fields*</span><span class="sxs-lookup"><span data-stu-id="06017-114">*Fields*</span></span> |<span data-ttu-id="06017-115">Para **WillChangeField**, o parâmetro *campos* é uma matriz de **variantes** que contém os objetos **Field** com os valores originais.</span><span class="sxs-lookup"><span data-stu-id="06017-115">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span> <br/><br/><span data-ttu-id="06017-116">Para **FieldChangeComplete**, o parâmetro *campos* é uma matriz de **variantes** que contém os objetos **Field** com os valores alterados.</span><span class="sxs-lookup"><span data-stu-id="06017-116">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>|
|<span data-ttu-id="06017-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="06017-117">*pError*</span></span> |<span data-ttu-id="06017-p102">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="06017-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="06017-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="06017-120">*adStatus*</span></span> |<span data-ttu-id="06017-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="06017-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="06017-122">Quando **WillChangeField** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="06017-122">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="06017-123">Será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="06017-123">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="06017-124">Quando **FieldChangeComplete** for cancelado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida ou como **adStatusErrorsOccurred** se a operação tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="06017-124">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="06017-125">Antes que **WillChangeField** seja retornado, configure esse parâmetro como **adStatusCancel** para solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="06017-125">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="06017-126">Antes que **FieldChangeComplete** seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="06017-126">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="06017-127">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="06017-127">*pRecordset*</span></span> |<span data-ttu-id="06017-p104">Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="06017-p104">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="06017-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="06017-130">Remarks</span></span>

<span data-ttu-id="06017-131">O evento **WillChangeField** ou **FieldChangeComplete** pode ocorrer ao definir a propriedade [Value](value-property-ado.md) e chamar o método [Update](update-method-ado.md) com os parâmetros de matriz do valor e campo.</span><span class="sxs-lookup"><span data-stu-id="06017-131">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

