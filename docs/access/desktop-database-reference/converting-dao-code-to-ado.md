---
title: Converter o código DAO em ADO
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461975"
---
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="550e5-102">Converter o código DAO em ADO</span><span class="sxs-lookup"><span data-stu-id="550e5-102">Converting DAO Code to ADO</span></span>

<span data-ttu-id="550e5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="550e5-103">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="550e5-104">Versões da biblioteca DAO anteriores à versão 3.6 não são fornecidas ou são suportadas no Access.</span><span class="sxs-lookup"><span data-stu-id="550e5-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="550e5-105">DAO para mapa de objeto ADO</span><span class="sxs-lookup"><span data-stu-id="550e5-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="550e5-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="550e5-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="550e5-107"><strong>ADO(ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="550e5-107"><strong>ADO(ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="550e5-108"><strong>Observação</strong></span><span class="sxs-lookup"><span data-stu-id="550e5-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="550e5-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="550e5-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="550e5-110">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="550e5-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="550e5-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="550e5-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="550e5-112">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="550e5-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="550e5-113">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="550e5-113">Database</span></span></p></td>
<td><p><span data-ttu-id="550e5-114">Connection</span><span class="sxs-lookup"><span data-stu-id="550e5-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="550e5-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="550e5-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="550e5-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="550e5-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="550e5-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="550e5-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="550e5-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="550e5-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="550e5-119">Recupera um conjunto de ponteiros para os registros no conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="550e5-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="550e5-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="550e5-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="550e5-121">Static</span><span class="sxs-lookup"><span data-stu-id="550e5-121">Static</span></span></p></td>
<td><p><span data-ttu-id="550e5-122">Recupera registros completos mas um conjunto de registros Static não pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="550e5-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="550e5-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="550e5-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="550e5-124">Keyset com opção adCmdTableDirect</span><span class="sxs-lookup"><span data-stu-id="550e5-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="550e5-125">Field</span><span class="sxs-lookup"><span data-stu-id="550e5-125">Field</span></span></p></td>
<td><p><span data-ttu-id="550e5-126">Field</span><span class="sxs-lookup"><span data-stu-id="550e5-126">Field</span></span></p></td>
<td><p><span data-ttu-id="550e5-127">Quando mencionado em um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="550e5-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="550e5-128">DAO</span><span class="sxs-lookup"><span data-stu-id="550e5-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="550e5-129">Abrir um Recordset</span><span class="sxs-lookup"><span data-stu-id="550e5-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="550e5-130">Editar um Recordset</span><span class="sxs-lookup"><span data-stu-id="550e5-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="550e5-131">ADO</span><span class="sxs-lookup"><span data-stu-id="550e5-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="550e5-132">Abrir um Recordset</span><span class="sxs-lookup"><span data-stu-id="550e5-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="550e5-133">Editar um Recordset</span><span class="sxs-lookup"><span data-stu-id="550e5-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="550e5-134">O deslocamento do foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem usar primeiro o método **CancelUpdate** executará implicitamente o método **Update**.</span><span class="sxs-lookup"><span data-stu-id="550e5-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="550e5-135">Sobre os colaboradores</span><span class="sxs-lookup"><span data-stu-id="550e5-135">About the contributors</span></span>

<span data-ttu-id="550e5-136">**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="550e5-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="550e5-137">UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="550e5-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="550e5-138">Escolhendo entre o DAO e ADO</span><span class="sxs-lookup"><span data-stu-id="550e5-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)



