---
<span data-ttu-id="ece4e-101"><<<<<<< Título cabeça: BOF e EOF propriedades (ADO) TOCTitle: BOF e EOF propriedades (ADO) === título: BOF, propriedades EOF (ADO) TOCTitle: BOF, propriedades EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="ece4e-101"><<<<<<< HEAD title: BOF, EOF Properties (ADO) TOCTitle: BOF, EOF Properties (ADO) ======= title: BOF, EOF properties (ADO) TOCTitle: BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="ece4e-102">ms:assetid de mestre: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: ms.date 48548768: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ece4e-102">master ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ece4e-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ece4e-103"><<<<<<< HEAD</span></span>
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="ece4e-104">Propriedades BOF, EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="ece4e-104">BOF, EOF Properties (ADO)</span></span>
=======
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="ece4e-105">BOF, propriedades EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="ece4e-105">BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="ece4e-106">mestre</span><span class="sxs-lookup"><span data-stu-id="ece4e-106">master</span></span>


<span data-ttu-id="ece4e-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ece4e-107">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="ece4e-108">**BOF**  Indica que a posição do registro atual é antes do primeiro registro em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ece4e-108">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="ece4e-109">**EOF**  Indica que a posição do registro atual é após o último registro em um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ece4e-109">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

<span data-ttu-id="ece4e-110"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ece4e-110"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="ece4e-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ece4e-111">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="ece4e-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ece4e-112">Return value</span></span>
>>>>>>> <span data-ttu-id="ece4e-113">mestre</span><span class="sxs-lookup"><span data-stu-id="ece4e-113">master</span></span>

<span data-ttu-id="ece4e-114">As propriedades **BOF** e **EOF** retornam valores **booleanos**.</span><span class="sxs-lookup"><span data-stu-id="ece4e-114">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece4e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ece4e-115">Remarks</span></span>

<span data-ttu-id="ece4e-116">Use as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao passar de um registro para outro.</span><span class="sxs-lookup"><span data-stu-id="ece4e-116">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="ece4e-117">A propriedade **BOF** retorna **Verdadeiro** (-1) se a posição do registro atual for antes do primeiro registro e **Falso** (0) se a posição for no primeiro registro ou após ele.</span><span class="sxs-lookup"><span data-stu-id="ece4e-117">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="ece4e-118">A propriedade **EOF** retorna **Verdadeiro** se a posição do registro atual for após o último registro e **Falso** se a posição do registro atual for no último registro ou antes dele.</span><span class="sxs-lookup"><span data-stu-id="ece4e-118">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="ece4e-119">Se tanto a propriedade **BOF** como a **EOF** forem **Verdadeiras**, não existe registro atual.</span><span class="sxs-lookup"><span data-stu-id="ece4e-119">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="ece4e-p101">Se você abrir um objeto **Recordset** sem nenhum registro, as propriedades **BOF** e **EOF** são configuradas como **Verdadeiro** (consulte a propriedade [RecordCount](recordcount-property-ado.md) para obter mais informações sobre esse estado de um **Recordset**). Quando você abre um objeto **Recordset** contendo ao menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** são **Falsas**.</span><span class="sxs-lookup"><span data-stu-id="ece4e-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="ece4e-122">Se você excluir o último registro restante do objeto **Recordset**, as propriedades **BOF** e **EOF** poderão permanecer **Falsas** até que você tente reposicionar o registro atual.</span><span class="sxs-lookup"><span data-stu-id="ece4e-122">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="ece4e-123">Esta tabela mostra quais métodos **Move** são permitidos com diferentes combinações das propriedades **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="ece4e-123">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="ece4e-124">Métodos MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="ece4e-124">MoveFirst,</span></span><br />
<span data-ttu-id="ece4e-125">MoveLast</span><span class="sxs-lookup"><span data-stu-id="ece4e-125">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="ece4e-126">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="ece4e-126">MovePrevious,</span></span><br />
<span data-ttu-id="ece4e-127">Mover &lt; 0</span><span class="sxs-lookup"><span data-stu-id="ece4e-127">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="ece4e-128">Move 0</span><span class="sxs-lookup"><span data-stu-id="ece4e-128">Move 0</span></span></p></th>
<th><p><span data-ttu-id="ece4e-129">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="ece4e-129">MoveNext,</span></span><br />
<span data-ttu-id="ece4e-130">Mover &gt; 0</span><span class="sxs-lookup"><span data-stu-id="ece4e-130">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ece4e-131"><strong>BOF = verdadeiro,</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-131"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="ece4e-132">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-132">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="ece4e-133">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ece4e-134">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-134">Error</span></span></p></td>
<td><p><span data-ttu-id="ece4e-135">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-135">Error</span></span></p></td>
<td><p><span data-ttu-id="ece4e-136">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-136">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ece4e-137"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-137"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="ece4e-138">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-138">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="ece4e-139">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-139">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ece4e-140">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-140">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ece4e-141">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-141">Error</span></span></p></td>
<td><p><span data-ttu-id="ece4e-142">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-142">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ece4e-143">Ambas <strong>Verdadeiras</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-143">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="ece4e-144">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-144">Error</span></span></p></td>
<td><p><span data-ttu-id="ece4e-145">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-145">Error</span></span></p></td>
<td><p><span data-ttu-id="ece4e-146">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-146">Error</span></span></p></td>
<td><p><span data-ttu-id="ece4e-147">Erro</span><span class="sxs-lookup"><span data-stu-id="ece4e-147">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ece4e-148">Ambas <strong>Falsas</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-148">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="ece4e-149">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ece4e-150">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-150">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ece4e-151">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-151">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ece4e-152">Permitido</span><span class="sxs-lookup"><span data-stu-id="ece4e-152">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ece4e-153">A permissão para um método **Move** não garante que o método localizará com sucesso um registro; ela apenas significa que a chamada para o método **Move** especificado não resultará em erro.</span><span class="sxs-lookup"><span data-stu-id="ece4e-153">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="ece4e-154">A tabela a seguir mostra o que acontece às configurações de propriedade de **BOF** e **EOF** quando você chama diversos métodos **Move** mas não consegue localizar com sucesso um registro.</span><span class="sxs-lookup"><span data-stu-id="ece4e-154">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="ece4e-155">BOF</span><span class="sxs-lookup"><span data-stu-id="ece4e-155">BOF</span></span></p></th>
<th><p><span data-ttu-id="ece4e-156">EOF</span><span class="sxs-lookup"><span data-stu-id="ece4e-156">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ece4e-157"><strong>Métodos MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="ece4e-158">Defina como <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-158">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="ece4e-159">Defina como <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-159">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ece4e-160"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="ece4e-160"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="ece4e-161">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="ece4e-161">No change</span></span></p></td>
<td><p><span data-ttu-id="ece4e-162">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="ece4e-162">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ece4e-163"><strong>MovePrevious</strong>, <strong>mova</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="ece4e-163"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="ece4e-164">Configurada como <strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-164">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="ece4e-165">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="ece4e-165">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ece4e-166"><strong>MoveNext</strong>, <strong>mova</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="ece4e-166"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="ece4e-167">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="ece4e-167">No change</span></span></p></td>
<td><p><span data-ttu-id="ece4e-168">Configurada como <strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="ece4e-168">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

