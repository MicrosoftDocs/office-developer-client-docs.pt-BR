---
title: Método Cancel (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e80763ddad86a63aec605371b58ffeab383681dd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944015"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="17bac-102">Método Cancel (ADO)</span><span class="sxs-lookup"><span data-stu-id="17bac-102">Cancel method (ADO)</span></span>

<span data-ttu-id="17bac-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="17bac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17bac-104">Cancela a execução de uma chamada de método assíncrona pendente.</span><span class="sxs-lookup"><span data-stu-id="17bac-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="17bac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17bac-105">Syntax</span></span>

<span data-ttu-id="17bac-106">*objeto*. Cancelar</span><span class="sxs-lookup"><span data-stu-id="17bac-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="17bac-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="17bac-107">Remarks</span></span>

<span data-ttu-id="17bac-108">Use o método **Cancel** para terminar a execução de uma chamada de método assíncrono (ou seja, um método chamado com a opção **adAsyncConnect**, **adAsyncExecute** ou **adAsyncFetch** ).</span><span class="sxs-lookup"><span data-stu-id="17bac-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="17bac-109">A tabela a seguir mostra a tarefa que será terminada quando o método **Cancel** for usado em um tipo de objeto específico.</span><span class="sxs-lookup"><span data-stu-id="17bac-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="17bac-110">
Se o <em>objeto</em> for um</span><span class="sxs-lookup"><span data-stu-id="17bac-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="17bac-111">A última chamada assíncrona deste método será terminada</span><span class="sxs-lookup"><span data-stu-id="17bac-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17bac-112"><a href="command-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="17bac-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="17bac-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execução</a></span><span class="sxs-lookup"><span data-stu-id="17bac-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17bac-114"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="17bac-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="17bac-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> ou <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="17bac-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17bac-116"><a href="record-object-ado.md">Objeto Record</a></span><span class="sxs-lookup"><span data-stu-id="17bac-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="17bac-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> ou <a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="17bac-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17bac-118"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="17bac-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="17bac-119"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="17bac-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17bac-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="17bac-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="17bac-121"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="17bac-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

