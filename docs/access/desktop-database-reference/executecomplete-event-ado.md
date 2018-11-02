---
title: Evento ExecuteComplete (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58683a8721ede0e7535b159f095b44bc6db6c1b7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926728"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="667d2-102">Evento ExecuteComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="667d2-102">ExecuteComplete event (ADO)</span></span>


<span data-ttu-id="667d2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="667d2-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="667d2-104">O evento **ExecuteComplete** é chamado depois que um comando terminar a execução.</span><span class="sxs-lookup"><span data-stu-id="667d2-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="667d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="667d2-105">Syntax</span></span>

<span data-ttu-id="667d2-106">Do ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="667d2-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="667d2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="667d2-107">Parameters</span></span>

  - <span data-ttu-id="667d2-108">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="667d2-108">*RecordsAffected*</span></span>

  - <span data-ttu-id="667d2-109">Um valor **Long** que indica o número de registros afetados pelo comando.</span><span class="sxs-lookup"><span data-stu-id="667d2-109">A **Long** value indicating the number of records affected by the command.</span></span>

  - <span data-ttu-id="667d2-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="667d2-110">*pError*</span></span>

  - <span data-ttu-id="667d2-p101">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="667d2-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="667d2-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="667d2-113">*adStatus*</span></span>

  - [<span data-ttu-id="667d2-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="667d2-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="667d2-115">Antes que esse evento seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="667d2-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="667d2-116">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="667d2-116">*pCommand*</span></span>

  - <span data-ttu-id="667d2-p102">O objeto [Command](command-object-ado.md) que foi executado. Contém um objeto **Command** mesmo ao chamar **Connection.Execute** ou **Recordset.Open** sem criar explicitamente um **Command**, nesses casos o objeto **Command** será criado internamente por ADO.</span><span class="sxs-lookup"><span data-stu-id="667d2-p102">The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>

  - <span data-ttu-id="667d2-119">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="667d2-119">*pRecordset*</span></span>

  - <span data-ttu-id="667d2-p103">Um objeto [Recordset](recordset-object-ado.md) que é o resultado do comando executado. Esse **Recordset** pode estar vazio. Você nunca deve destruir esse objeto Recordset a partir dessa rotina de tratamento de eventos. Tal procedimento resultará em uma Violação de Acesso quando o ADO tentar acessar um objeto que não exista mais.</span><span class="sxs-lookup"><span data-stu-id="667d2-p103">A [Recordset](recordset-object-ado.md) object that is the result of the executed command. This **Recordset** may be empty. You should never destroy this Recordset object from within this event handler. Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>

  - <span data-ttu-id="667d2-124">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="667d2-124">*pConnection*</span></span>

  - <span data-ttu-id="667d2-p104">Um objeto [Connection](connection-object-ado.md). A conexão sobre a qual a operação foi executada.</span><span class="sxs-lookup"><span data-stu-id="667d2-p104">A [Connection](connection-object-ado.md) object. The connection over which the operation was executed.</span></span>

## <a name="remarks"></a><span data-ttu-id="667d2-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="667d2-127">Remarks</span></span>

<span data-ttu-id="667d2-128">Um evento **ExecuteComplete** pode ocorrer devido aos métodos **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) ou **Recordset.**[NextRecordset](nextrecordset-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="667d2-128">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

