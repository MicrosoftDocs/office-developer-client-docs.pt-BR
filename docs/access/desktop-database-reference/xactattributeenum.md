---
title: XactAttributeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 28b81c45921120b8a3cd8768d22559355d8ff623
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870489"
---
# <a name="xactattributeenum"></a><span data-ttu-id="8c338-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="8c338-102">XactAttributeEnum</span></span>

<span data-ttu-id="8c338-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c338-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c338-104">Especifica os atributos de transação de um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8c338-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c338-105">Constant</span><span class="sxs-lookup"><span data-stu-id="8c338-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8c338-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8c338-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8c338-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c338-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c338-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-109">262144</span><span class="sxs-lookup"><span data-stu-id="8c338-109">262144</span></span></p></td>
<td><p><span data-ttu-id="8c338-110">Realiza anulações reter; ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automaticamente inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="8c338-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="8c338-111">Nem todos os provedores dar suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="8c338-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-113">131072</span><span class="sxs-lookup"><span data-stu-id="8c338-113">131072</span></span></p></td>
<td><p><span data-ttu-id="8c338-114">Realiza confirmações reter; ou seja, chamar <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automaticamente inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="8c338-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="8c338-115">Nem todos os provedores dar suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="8c338-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8c338-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8c338-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="8c338-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8c338-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c338-118">Constante</span><span class="sxs-lookup"><span data-stu-id="8c338-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c338-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="8c338-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="8c338-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

