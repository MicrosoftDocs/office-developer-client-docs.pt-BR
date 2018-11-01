---
title: Enumeração LockTypeEnum (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0e12f8d60ee3147eb456df302122a5b7eac684d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879925"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="8103b-102">Enumeração LockTypeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="8103b-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="8103b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8103b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8103b-104">Especifica o tipo de bloqueio de registro usado ao abrir um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="8103b-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8103b-105">Nome</span><span class="sxs-lookup"><span data-stu-id="8103b-105">Name</span></span></p></th>
<th><p><span data-ttu-id="8103b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8103b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8103b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8103b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8103b-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="8103b-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="8103b-109">3</span><span class="sxs-lookup"><span data-stu-id="8103b-109">3</span></span></p></td>
<td><p><span data-ttu-id="8103b-p101">Concorrência otimista baseada no código de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="8103b-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8103b-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="8103b-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="8103b-113">5</span><span class="sxs-lookup"><span data-stu-id="8103b-113">5</span></span></p></td>
<td><p><span data-ttu-id="8103b-114">Ativa atualizações otimistas em lotes (somente espaços de trabalho de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8103b-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8103b-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="8103b-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="8103b-116">1</span><span class="sxs-lookup"><span data-stu-id="8103b-116">1</span></span></p></td>
<td><p><span data-ttu-id="8103b-p102">Concorrência otimista baseada nos valores dos registros. O cursor compara os valores de dados de registros antigos e novos, para determinar se foram feitas alterações desde que o registro foi acessado pela última vez (somente espaços de trabalho de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="8103b-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="8103b-p103">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8103b-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8103b-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="8103b-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="8103b-122">2</span><span class="sxs-lookup"><span data-stu-id="8103b-122">2</span></span></p></td>
<td><p><span data-ttu-id="8103b-p104">Concorrência pessimista. O cursor usa o nível mais baixo de bloqueio, suficiente para garantir que o registro possa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="8103b-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

