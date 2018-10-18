---
<span data-ttu-id="c9ef1-101"><<<<<<< Título cabeça: conversão de código DAO para ADO TOCTitle: conversão de código DAO para ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: ms.date 48544585: 18/09/2015 === título: converter DAO código ADO TOCTitle: código DAO converter ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: ms.date 48544585: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="c9ef1-101"><<<<<<< HEAD title: Converting DAO Code to ADO TOCTitle: Converting DAO Code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 09/18/2015 ======= title: Convert DAO code to ADO TOCTitle: Convert DAO code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="c9ef1-102">mtps_version mestre: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="c9ef1-102">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="c9ef1-103">vbaac10.chm5267115 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="c9ef1-103">vbaac10.chm5267115 f1_categories:</span></span>
- <span data-ttu-id="c9ef1-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="c9ef1-104">Office.Version=v15</span></span>
---

<span data-ttu-id="c9ef1-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9ef1-105"><<<<<<< HEAD</span></span>
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="c9ef1-106">Converter o código DAO em ADO</span><span class="sxs-lookup"><span data-stu-id="c9ef1-106">Converting DAO Code to ADO</span></span>
=======
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="c9ef1-107">Converter o código DAO em ADO</span><span class="sxs-lookup"><span data-stu-id="c9ef1-107">Convert DAO code to ADO</span></span>
>>>>>>> <span data-ttu-id="c9ef1-108">mestre</span><span class="sxs-lookup"><span data-stu-id="c9ef1-108">master</span></span>

<span data-ttu-id="c9ef1-109">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9ef1-109">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="c9ef1-110">Versões da biblioteca DAO anteriores à versão 3.6 não são fornecidas ou são suportadas no Access.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-110">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="c9ef1-111">DAO para mapa de objeto ADO</span><span class="sxs-lookup"><span data-stu-id="c9ef1-111">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9ef1-112"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="c9ef1-112"><strong>DAO</strong></span></span></p></th>
<span data-ttu-id="c9ef1-113"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9ef1-113"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="c9ef1-114"><strong>ADO(ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="c9ef1-114"><strong>ADO(ADODB)</strong></span></span></p></th>
=======
<th><p><span data-ttu-id="c9ef1-115"><strong>O ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="c9ef1-115"><strong>ADO (ADODB)</strong></span></span></p></th><span data-ttu-id="c9ef1-116">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="c9ef1-116">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="c9ef1-117"><strong>Observação</strong></span><span class="sxs-lookup"><span data-stu-id="c9ef1-117"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9ef1-118">DBEngine</span><span class="sxs-lookup"><span data-stu-id="c9ef1-118">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c9ef1-119">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ef1-120">Workspace</span><span class="sxs-lookup"><span data-stu-id="c9ef1-120">Workspace</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c9ef1-121">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ef1-122">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="c9ef1-122">Database</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-123">Connection</span><span class="sxs-lookup"><span data-stu-id="c9ef1-123">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ef1-124">Recordset</span><span class="sxs-lookup"><span data-stu-id="c9ef1-124">Recordset</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-125">Recordset</span><span class="sxs-lookup"><span data-stu-id="c9ef1-125">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ef1-126">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="c9ef1-126">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-127">Keyset</span><span class="sxs-lookup"><span data-stu-id="c9ef1-127">Keyset</span></span></p></td>
<span data-ttu-id="c9ef1-128"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9ef1-128"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="c9ef1-129">Recupera um conjunto de ponteiros para os registros no conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c9ef1-129">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="c9ef1-130">Recupera um conjunto de ponteiros para os registros no recordset.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-130">Retrieves a set of pointers to the records in the recordset.</span></span></p></td><span data-ttu-id="c9ef1-131">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="c9ef1-131">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ef1-132">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="c9ef1-132">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-133">Static</span><span class="sxs-lookup"><span data-stu-id="c9ef1-133">Static</span></span></p></td>
<span data-ttu-id="c9ef1-134"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9ef1-134"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="c9ef1-135">Recupera registros completos mas um conjunto de registros Static não pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-135">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ef1-136">Table-Type</span><span class="sxs-lookup"><span data-stu-id="c9ef1-136">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-137">Keyset com opção adCmdTableDirect</span><span class="sxs-lookup"><span data-stu-id="c9ef1-137">Keyset with adCmdTableDirect Option</span></span></p></td>
=======
<td><p><span data-ttu-id="c9ef1-138">Recupera registros completos mas um recordset estático pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-138">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ef1-139">Table-Type</span><span class="sxs-lookup"><span data-stu-id="c9ef1-139">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-140">Keyset com opção adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-140">Keyset with adCmdTableDirect option.</span></span></p></td><span data-ttu-id="c9ef1-141">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="c9ef1-141">
>>>>>>> master</span></span>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ef1-142">Field</span><span class="sxs-lookup"><span data-stu-id="c9ef1-142">Field</span></span></p></td>
<td><p><span data-ttu-id="c9ef1-143">Field</span><span class="sxs-lookup"><span data-stu-id="c9ef1-143">Field</span></span></p></td>
<span data-ttu-id="c9ef1-144"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9ef1-144"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="c9ef1-145">Quando mencionado em um conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c9ef1-145">When referred to in a recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="c9ef1-146">Quando mencionado em um conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-146">When referred to in a recordset.</span></span></p></td><span data-ttu-id="c9ef1-147">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="c9ef1-147">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="c9ef1-148">DAO</span><span class="sxs-lookup"><span data-stu-id="c9ef1-148">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="c9ef1-149">Abrir um Recordset</span><span class="sxs-lookup"><span data-stu-id="c9ef1-149">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="c9ef1-150">Editar um Recordset</span><span class="sxs-lookup"><span data-stu-id="c9ef1-150">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="c9ef1-151">ADO</span><span class="sxs-lookup"><span data-stu-id="c9ef1-151">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="c9ef1-152">Abrir um Recordset</span><span class="sxs-lookup"><span data-stu-id="c9ef1-152">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="c9ef1-153">Editar um Recordset</span><span class="sxs-lookup"><span data-stu-id="c9ef1-153">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
<span data-ttu-id="c9ef1-154"><<<<<<< Cabeça movendo foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem primeiro usando o método **CancelUpdate** executará implicitamente o método **Update** .</span><span class="sxs-lookup"><span data-stu-id="c9ef1-154"><<<<<<< HEAD Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>
> <span data-ttu-id="c9ef1-155">=== Deslocamento do foco do registro atual por meio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sem usar primeiro o método **CancelUpdate** implicitamente executa o método **Update** .</span><span class="sxs-lookup"><span data-stu-id="c9ef1-155">======= Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>
>>>>>>> <span data-ttu-id="c9ef1-156">mestre</span><span class="sxs-lookup"><span data-stu-id="c9ef1-156">master</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="c9ef1-157">Sobre os colaboradores</span><span class="sxs-lookup"><span data-stu-id="c9ef1-157">About the contributors</span></span>

<span data-ttu-id="c9ef1-158">**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="c9ef1-158">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="c9ef1-159">UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-159">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="c9ef1-160">Escolhendo entre o DAO e ADO</span><span class="sxs-lookup"><span data-stu-id="c9ef1-160">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<span data-ttu-id="c9ef1-161"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9ef1-161"><<<<<<< HEAD</span></span>

=======
<br/>
>>>>>>> <span data-ttu-id="c9ef1-162">mestre</span><span class="sxs-lookup"><span data-stu-id="c9ef1-162">master</span></span>

