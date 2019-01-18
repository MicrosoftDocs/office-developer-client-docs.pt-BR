---
title: XactAttributeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718550"
---
# <a name="xactattributeenum"></a><span data-ttu-id="07ee4-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="07ee4-102">XactAttributeEnum</span></span>

<span data-ttu-id="07ee4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="07ee4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07ee4-104">Especifica os atributos de transação de um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="07ee4-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07ee4-105">Constant</span><span class="sxs-lookup"><span data-stu-id="07ee4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="07ee4-106">Valor</span><span class="sxs-lookup"><span data-stu-id="07ee4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="07ee4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="07ee4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07ee4-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="07ee4-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="07ee4-109">262144</span><span class="sxs-lookup"><span data-stu-id="07ee4-109">262144</span></span></p></td>
<td><p><span data-ttu-id="07ee4-110">Realiza anulações reter; ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automaticamente inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="07ee4-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="07ee4-111">Nem todos os provedores dar suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="07ee4-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07ee4-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="07ee4-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="07ee4-113">131072</span><span class="sxs-lookup"><span data-stu-id="07ee4-113">131072</span></span></p></td>
<td><p><span data-ttu-id="07ee4-114">Realiza confirmações reter; ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automaticamente inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="07ee4-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="07ee4-115">Nem todos os provedores dar suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="07ee4-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="07ee4-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="07ee4-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="07ee4-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="07ee4-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07ee4-118">Constante</span><span class="sxs-lookup"><span data-stu-id="07ee4-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07ee4-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="07ee4-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07ee4-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="07ee4-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

