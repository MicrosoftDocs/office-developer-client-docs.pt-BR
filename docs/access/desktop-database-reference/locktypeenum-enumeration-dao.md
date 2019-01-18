---
title: Enumeração LockTypeEnum (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c2d355e2a16df632d6952802914c1f921b5e9719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719523"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="bbded-102">Enumeração LockTypeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="bbded-102">LockTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="bbded-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbded-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbded-104">Especifica o tipo de bloqueio de registro usado ao abrir um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="bbded-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbded-105">Nome</span><span class="sxs-lookup"><span data-stu-id="bbded-105">Name</span></span></p></th>
<th><p><span data-ttu-id="bbded-106">Valor</span><span class="sxs-lookup"><span data-stu-id="bbded-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bbded-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbded-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbded-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="bbded-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="bbded-109">3</span><span class="sxs-lookup"><span data-stu-id="bbded-109">3</span></span></p></td>
<td><p><span data-ttu-id="bbded-p101">Concorrência otimista baseada no código de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="bbded-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbded-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="bbded-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="bbded-113">5</span><span class="sxs-lookup"><span data-stu-id="bbded-113">5</span></span></p></td>
<td><p><span data-ttu-id="bbded-114">Ativa atualizações otimistas em lotes (somente espaços de trabalho de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bbded-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbded-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="bbded-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="bbded-116">1</span><span class="sxs-lookup"><span data-stu-id="bbded-116">1</span></span></p></td>
<td><p><span data-ttu-id="bbded-p102">Concorrência otimista baseada nos valores dos registros. O cursor compara os valores de dados de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez (somente espaços de trabalho de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bbded-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <span data-ttu-id="bbded-p103">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bbded-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbded-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="bbded-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="bbded-122">2</span><span class="sxs-lookup"><span data-stu-id="bbded-122">2</span></span></p></td>
<td><p><span data-ttu-id="bbded-p104">Concorrência pessimista. O cursor usa o nível mais baixo de bloqueio, suficiente para garantir que o registro possa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="bbded-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

