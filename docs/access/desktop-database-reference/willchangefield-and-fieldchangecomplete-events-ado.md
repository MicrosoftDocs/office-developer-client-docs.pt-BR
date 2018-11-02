---
title: Eventos WillChangeField e FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2967b6670ad96752e7ce47d82227fad70335e1f6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927400"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="1d20f-102">Eventos WillChangeField e FieldChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="1d20f-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>


<span data-ttu-id="1d20f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d20f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d20f-p101">O evento **WillChangeField** é chamado antes que uma operação pendente altere o valor de um ou mais objetos [Field](field-object-ado.md) em [Recordset](recordset-object-ado.md). O evento **FieldChangeComplete** é chamado depois que o valor de um ou mais objetos **Field** tiver sido alterado.</span><span class="sxs-lookup"><span data-stu-id="1d20f-p101">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md). The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d20f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d20f-106">Syntax</span></span>

<span data-ttu-id="1d20f-107">De*cFields*, *campos*, de WillChangeField *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1d20f-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="1d20f-108">FieldChangeComplete*cFields*, *campos*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1d20f-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="1d20f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d20f-109">Parameters</span></span>

  - <span data-ttu-id="1d20f-110">*cFields*</span><span class="sxs-lookup"><span data-stu-id="1d20f-110">*cFields*</span></span>

  - <span data-ttu-id="1d20f-111">Um **Long** que indica o número de objetos **Field** em *Fields*.</span><span class="sxs-lookup"><span data-stu-id="1d20f-111">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>

  - <span data-ttu-id="1d20f-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="1d20f-112">*Fields*</span></span>

  - <span data-ttu-id="1d20f-113">Para **WillChangeField**, o parâmetro *campos* é uma matriz de **variantes** que contém os objetos **Field** com os valores originais.</span><span class="sxs-lookup"><span data-stu-id="1d20f-113">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span>  
      
    <span data-ttu-id="1d20f-114">Para **FieldChangeComplete**, o parâmetro *campos* é uma matriz de **variantes** que contém os objetos **Field** com os valores alterados.</span><span class="sxs-lookup"><span data-stu-id="1d20f-114">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>

  - <span data-ttu-id="1d20f-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="1d20f-115">*pError*</span></span>

  - <span data-ttu-id="1d20f-p102">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="1d20f-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="1d20f-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="1d20f-118">*adStatus*</span></span>

  - [<span data-ttu-id="1d20f-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="1d20f-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="1d20f-p103">Quando **WillChangeField** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida. Será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="1d20f-p103">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="1d20f-122">Quando **FieldChangeComplete** for cancelado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida ou como **adStatusErrorsOccurred** se a operação tiver falhado.</span><span class="sxs-lookup"><span data-stu-id="1d20f-122">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="1d20f-123">Antes que **WillChangeField** seja retornado, configure esse parâmetro como **adStatusCancel** para solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="1d20f-123">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="1d20f-124">Antes que **FieldChangeComplete** seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1d20f-124">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="1d20f-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1d20f-125">*pRecordset*</span></span>

  - <span data-ttu-id="1d20f-p104">Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="1d20f-p104">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d20f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d20f-128">Remarks</span></span>

<span data-ttu-id="1d20f-129">O evento **WillChangeField** ou **FieldChangeComplete** pode ocorrer ao definir a propriedade [Value](value-property-ado.md) e chamar o método [Update](update-method-ado.md) com os parâmetros de matriz do valor e campo.</span><span class="sxs-lookup"><span data-stu-id="1d20f-129">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

