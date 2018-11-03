---
title: Enumeração LockTypeEnum (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 771ce7a5a7f0a6721703953029b7bc8de9f0f251
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936571"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="75754-102">Enumeração LockTypeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="75754-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="75754-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="75754-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75754-104">Especifica o tipo de bloqueio de registro usado ao abrir um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="75754-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75754-105">Nome</span><span class="sxs-lookup"><span data-stu-id="75754-105">Name</span></span></p></th>
<th><p><span data-ttu-id="75754-106">Valor</span><span class="sxs-lookup"><span data-stu-id="75754-106">Value</span></span></p></th>
<th><p><span data-ttu-id="75754-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="75754-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75754-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="75754-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="75754-109">3</span><span class="sxs-lookup"><span data-stu-id="75754-109">3</span></span></p></td>
<td><p><span data-ttu-id="75754-p101">Concorrência otimista baseada no código de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="75754-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75754-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="75754-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="75754-113">5</span><span class="sxs-lookup"><span data-stu-id="75754-113">5</span></span></p></td>
<td><p><span data-ttu-id="75754-114">Ativa atualizações otimistas em lotes (somente espaços de trabalho de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="75754-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75754-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="75754-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="75754-116">1</span><span class="sxs-lookup"><span data-stu-id="75754-116">1</span></span></p></td>
<td><p><span data-ttu-id="75754-p102">Concorrência otimista baseada nos valores dos registros. O cursor compara os valores de dados de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez (somente espaços de trabalho de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="75754-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <span data-ttu-id="75754-p103">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="75754-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75754-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="75754-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="75754-122">2</span><span class="sxs-lookup"><span data-stu-id="75754-122">2</span></span></p></td>
<td><p><span data-ttu-id="75754-p104">Concorrência pessimista. O cursor usa o nível mais baixo de bloqueio, suficiente para garantir que o registro possa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="75754-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

