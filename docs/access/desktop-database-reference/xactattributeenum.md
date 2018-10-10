---
title: XactAttributeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a44546a63583a03bd40b9e86405c3d560b3a94e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464654"
---
# <a name="xactattributeenum"></a><span data-ttu-id="7f1df-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="7f1df-102">XactAttributeEnum</span></span>


<span data-ttu-id="7f1df-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f1df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f1df-104">Especifica os atributos de transação de um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7f1df-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f1df-105">Constant</span><span class="sxs-lookup"><span data-stu-id="7f1df-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7f1df-106">Valor</span><span class="sxs-lookup"><span data-stu-id="7f1df-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7f1df-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f1df-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f1df-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="7f1df-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="7f1df-109">262144</span><span class="sxs-lookup"><span data-stu-id="7f1df-109">262144</span></span></p></td>
<td><p><span data-ttu-id="7f1df-p101">Executa a manutenção de anulações — ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> inicia automaticamente uma nova transação. Nem todos os provedores oferecem suporte para isso.</span><span class="sxs-lookup"><span data-stu-id="7f1df-p101">Performs retaining aborts — that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction. Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f1df-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="7f1df-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="7f1df-113">131072</span><span class="sxs-lookup"><span data-stu-id="7f1df-113">131072</span></span></p></td>
<td><p><span data-ttu-id="7f1df-p102">Executa a manutenção de confirmações — ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> inicia automaticamente uma nova transação. Nem todos os provedores oferecem suporte para isso.</span><span class="sxs-lookup"><span data-stu-id="7f1df-p102">Performs retaining commits — that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction. Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7f1df-116">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="7f1df-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="7f1df-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7f1df-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f1df-118">Constante</span><span class="sxs-lookup"><span data-stu-id="7f1df-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f1df-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="7f1df-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f1df-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="7f1df-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

