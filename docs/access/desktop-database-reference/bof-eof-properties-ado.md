---
title: Propriedades BOF, EOF (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d36a65ce8a6808f2128749bd7fbc6e468acbd279
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296784"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="df910-102">Propriedades BOF, EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="df910-102">BOF, EOF properties (ADO)</span></span>


<span data-ttu-id="df910-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df910-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df910-104">**BOF**  Indica que a posição do registro atual é antes do primeiro registro em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="df910-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="df910-105">**EOF**  Indica que a posição do registro atual é após o último registro em um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="df910-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="df910-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="df910-106">Return value</span></span>

<span data-ttu-id="df910-107">As propriedades **BOF** e **EOF** retornam valores **booleanos**.</span><span class="sxs-lookup"><span data-stu-id="df910-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="df910-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="df910-108">Remarks</span></span>

<span data-ttu-id="df910-109">Use as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao passar de um registro para outro.</span><span class="sxs-lookup"><span data-stu-id="df910-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="df910-110">A propriedade **BOF** retorna **Verdadeiro** (-1) se a posição do registro atual for antes do primeiro registro e **Falso** (0) se a posição for no primeiro registro ou após ele.</span><span class="sxs-lookup"><span data-stu-id="df910-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="df910-111">A propriedade **EOF** retorna **Verdadeiro** se a posição do registro atual for após o último registro e **Falso** se a posição do registro atual for no último registro ou antes dele.</span><span class="sxs-lookup"><span data-stu-id="df910-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="df910-112">Se tanto a propriedade **BOF** como a **EOF** forem **Verdadeiras**, não existe registro atual.</span><span class="sxs-lookup"><span data-stu-id="df910-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="df910-p101">Se você abrir um objeto **Recordset** sem nenhum registro, as propriedades **BOF** e **EOF** são configuradas como **Verdadeiro** (consulte a propriedade [RecordCount](recordcount-property-ado.md) para obter mais informações sobre esse estado de um **Recordset**). Quando você abre um objeto **Recordset** contendo ao menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** são **Falsas**.</span><span class="sxs-lookup"><span data-stu-id="df910-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="df910-115">Se você excluir o último registro restante do objeto **Recordset**, as propriedades **BOF** e **EOF** poderão permanecer **Falsas** até que você tente reposicionar o registro atual.</span><span class="sxs-lookup"><span data-stu-id="df910-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="df910-116">Esta tabela mostra quais métodos **Move** são permitidos com diferentes combinações das propriedades **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="df910-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="df910-117">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="df910-117">MoveFirst,</span></span><br />
<span data-ttu-id="df910-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="df910-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="df910-119">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="df910-119">MovePrevious,</span></span><br />
<span data-ttu-id="df910-120">Mover &lt; 0</span><span class="sxs-lookup"><span data-stu-id="df910-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="df910-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="df910-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="df910-122">MoveNext</span><span class="sxs-lookup"><span data-stu-id="df910-122">MoveNext,</span></span><br />
<span data-ttu-id="df910-123">Mover &gt; 0</span><span class="sxs-lookup"><span data-stu-id="df910-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df910-124"><strong>BOF = true,</strong></span><span class="sxs-lookup"><span data-stu-id="df910-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="df910-125">
<strong>EOF = falso</strong></span><span class="sxs-lookup"><span data-stu-id="df910-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="df910-126">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="df910-127">Error</span><span class="sxs-lookup"><span data-stu-id="df910-127">Error</span></span></p></td>
<td><p><span data-ttu-id="df910-128">Error</span><span class="sxs-lookup"><span data-stu-id="df910-128">Error</span></span></p></td>
<td><p><span data-ttu-id="df910-129">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df910-130"><strong>BOF = false,</strong></span><span class="sxs-lookup"><span data-stu-id="df910-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="df910-131">
<strong>EOF = true</strong></span><span class="sxs-lookup"><span data-stu-id="df910-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="df910-132">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="df910-133">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="df910-134">Error</span><span class="sxs-lookup"><span data-stu-id="df910-134">Error</span></span></p></td>
<td><p><span data-ttu-id="df910-135">Error</span><span class="sxs-lookup"><span data-stu-id="df910-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df910-136">Ambas <strong>Verdadeiras</strong></span><span class="sxs-lookup"><span data-stu-id="df910-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="df910-137">Erro</span><span class="sxs-lookup"><span data-stu-id="df910-137">Error</span></span></p></td>
<td><p><span data-ttu-id="df910-138">Error</span><span class="sxs-lookup"><span data-stu-id="df910-138">Error</span></span></p></td>
<td><p><span data-ttu-id="df910-139">Error</span><span class="sxs-lookup"><span data-stu-id="df910-139">Error</span></span></p></td>
<td><p><span data-ttu-id="df910-140">Erro</span><span class="sxs-lookup"><span data-stu-id="df910-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df910-141">Ambas <strong>Falsas</strong></span><span class="sxs-lookup"><span data-stu-id="df910-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="df910-142">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="df910-143">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="df910-144">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="df910-145">Permitido</span><span class="sxs-lookup"><span data-stu-id="df910-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="df910-146">A permissão para um método **Move** não garante que o método localizará com sucesso um registro; ela apenas significa que a chamada para o método **Move** especificado não resultará em erro.</span><span class="sxs-lookup"><span data-stu-id="df910-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="df910-147">A tabela a seguir mostra o que acontece às configurações de propriedade de **BOF** e **EOF** quando você chama diversos métodos **Move** mas não consegue localizar com sucesso um registro.</span><span class="sxs-lookup"><span data-stu-id="df910-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="df910-148">BOF</span><span class="sxs-lookup"><span data-stu-id="df910-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="df910-149">EOF</span><span class="sxs-lookup"><span data-stu-id="df910-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df910-150"><strong>MoveFirst</strong>, <strong></strong> MoveLast</span><span class="sxs-lookup"><span data-stu-id="df910-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="df910-151">Configurada como <strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="df910-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="df910-152">Configurada como <strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="df910-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df910-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="df910-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="df910-154">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="df910-154">No change</span></span></p></td>
<td><p><span data-ttu-id="df910-155">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="df910-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df910-156"><strong>MovePrevious</strong>, <strong>mover</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="df910-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="df910-157">Configurada como <strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="df910-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="df910-158">Sem alteração</span><span class="sxs-lookup"><span data-stu-id="df910-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df910-159"><strong>MoveNext</strong>, <strong>mover</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="df910-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="df910-160">Sem alteração</span><span class="sxs-lookup"><span data-stu-id="df910-160">No change</span></span></p></td>
<td><p><span data-ttu-id="df910-161">Configurada como <strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="df910-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

