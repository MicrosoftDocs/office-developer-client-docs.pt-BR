---
title: Converter o código DAO em ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720335"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="9d8b1-102">Converter o código DAO em ADO</span><span class="sxs-lookup"><span data-stu-id="9d8b1-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="9d8b1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d8b1-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="9d8b1-104">Versões da biblioteca DAO anteriores à versão 3.6 não são fornecidas ou são suportadas no Access.</span><span class="sxs-lookup"><span data-stu-id="9d8b1-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="9d8b1-105">DAO para mapa de objeto ADO</span><span class="sxs-lookup"><span data-stu-id="9d8b1-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d8b1-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="9d8b1-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="9d8b1-107"><strong>O ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="9d8b1-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="9d8b1-108"><strong>Observação</strong></span><span class="sxs-lookup"><span data-stu-id="9d8b1-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d8b1-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="9d8b1-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-110">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9d8b1-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d8b1-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="9d8b1-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-112">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9d8b1-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d8b1-113">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="9d8b1-113">Database</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-114">Connection</span><span class="sxs-lookup"><span data-stu-id="9d8b1-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d8b1-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="9d8b1-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="9d8b1-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d8b1-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="9d8b1-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="9d8b1-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-119">Recupera um conjunto de ponteiros para os registros no recordset.</span><span class="sxs-lookup"><span data-stu-id="9d8b1-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d8b1-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="9d8b1-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-121">Static</span><span class="sxs-lookup"><span data-stu-id="9d8b1-121">Static</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-122">Recupera registros completos mas um recordset estático pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9d8b1-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d8b1-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="9d8b1-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-124">Keyset com opção adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="9d8b1-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d8b1-125">Field</span><span class="sxs-lookup"><span data-stu-id="9d8b1-125">Field</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-126">Field</span><span class="sxs-lookup"><span data-stu-id="9d8b1-126">Field</span></span></p></td>
<td><p><span data-ttu-id="9d8b1-127">Quando mencionado em um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="9d8b1-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="9d8b1-128">DAO</span><span class="sxs-lookup"><span data-stu-id="9d8b1-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="9d8b1-129">Abrir um Recordset</span><span class="sxs-lookup"><span data-stu-id="9d8b1-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="9d8b1-130">Editar um Recordset</span><span class="sxs-lookup"><span data-stu-id="9d8b1-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="9d8b1-131">ADO</span><span class="sxs-lookup"><span data-stu-id="9d8b1-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="9d8b1-132">Abrir um Recordset</span><span class="sxs-lookup"><span data-stu-id="9d8b1-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="9d8b1-133">Editar um Recordset</span><span class="sxs-lookup"><span data-stu-id="9d8b1-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="9d8b1-134">Deslocamento do foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem usar primeiro o método **CancelUpdate** implicitamente executa o método **Update** .</span><span class="sxs-lookup"><span data-stu-id="9d8b1-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="9d8b1-135">Sobre os colaboradores</span><span class="sxs-lookup"><span data-stu-id="9d8b1-135">About the contributors</span></span>

<span data-ttu-id="9d8b1-136">**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="9d8b1-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="9d8b1-137">UtterAccess é o fórum principal de wiki e de ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9d8b1-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="9d8b1-138">Escolhendo entre o DAO e ADO</span><span class="sxs-lookup"><span data-stu-id="9d8b1-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

