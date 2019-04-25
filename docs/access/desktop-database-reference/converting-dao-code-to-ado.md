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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295517"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="b329a-102">Converter o código DAO em ADO</span><span class="sxs-lookup"><span data-stu-id="b329a-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="b329a-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b329a-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="b329a-104">As versões da biblioteca DAO anteriores à versão 3.6 não são fornecidas e nem têm suporte no Access.</span><span class="sxs-lookup"><span data-stu-id="b329a-104">Versions of the DAO library prior to 3.6 are not provided or supported in Microsoft Access 2010.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="b329a-105">De DAO para mapa de objeto ADO</span><span class="sxs-lookup"><span data-stu-id="b329a-105">DAO to ADO object Map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b329a-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="b329a-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="b329a-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="b329a-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="b329a-108"><strong>Observação</strong></span><span class="sxs-lookup"><span data-stu-id="b329a-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b329a-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="b329a-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="b329a-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b329a-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b329a-111">Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="b329a-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="b329a-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b329a-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b329a-113">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="b329a-113">Database</span></span></p></td>
<td><p><span data-ttu-id="b329a-114">Conexão</span><span class="sxs-lookup"><span data-stu-id="b329a-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b329a-115">Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="b329a-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="b329a-116">Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="b329a-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b329a-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="b329a-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="b329a-118">Conjunto de chaves</span><span class="sxs-lookup"><span data-stu-id="b329a-118">Keyset cursors</span></span></p></td>
<td><p><span data-ttu-id="b329a-119">Recupera um conjunto de ponteiros para os registros no conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="b329a-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b329a-120">Tipo de instantâneo</span><span class="sxs-lookup"><span data-stu-id="b329a-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="b329a-121">Estático</span><span class="sxs-lookup"><span data-stu-id="b329a-121">Static</span></span></p></td>
<td><p><span data-ttu-id="b329a-122">Recupera registros completos, mas um conjunto de registros Estáticos não pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="b329a-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b329a-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="b329a-123">TableType</span></span></p></td>
<td><p><span data-ttu-id="b329a-124">Conjunto de chaves com opção adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="b329a-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b329a-125">Campo</span><span class="sxs-lookup"><span data-stu-id="b329a-125">Field</span></span></p></td>
<td><p><span data-ttu-id="b329a-126">Campo</span><span class="sxs-lookup"><span data-stu-id="b329a-126">Field</span></span></p></td>
<td><p><span data-ttu-id="b329a-127">Quando mencionado em um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="b329a-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="b329a-128">DAO</span><span class="sxs-lookup"><span data-stu-id="b329a-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="b329a-129">Abrir um Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="b329a-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="b329a-130">Editar um Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="b329a-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="b329a-131">ADO</span><span class="sxs-lookup"><span data-stu-id="b329a-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="b329a-132">Abrir um Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="b329a-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="b329a-133">Editar um Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="b329a-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="b329a-134">O deslocamento do foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem usar primeiro o método **CancelUpdate** executará implicitamente o método **Update**.</span><span class="sxs-lookup"><span data-stu-id="b329a-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="b329a-135">Sobre os colaboradores</span><span class="sxs-lookup"><span data-stu-id="b329a-135">About the contributors</span></span>

<span data-ttu-id="b329a-136">**Link fornecido pela** comunidade [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="b329a-136">**Link provided byCommunity Member Icon** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="b329a-137">UtterAccess é o fórum principal de wiki e de ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b329a-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="b329a-138">Escolher entre DAO e ADO</span><span class="sxs-lookup"><span data-stu-id="b329a-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

