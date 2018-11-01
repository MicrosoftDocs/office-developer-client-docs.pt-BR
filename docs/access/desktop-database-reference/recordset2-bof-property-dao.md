---
title: Propriedade Recordset2.BOF (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9e85b86d2ccfeaddd56f5373684e8790ee1ab0b2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876418"
---
# <a name="recordset2bof-property-dao"></a><span data-ttu-id="e252b-102">Propriedade Recordset2.BOF (DAO)</span><span class="sxs-lookup"><span data-stu-id="e252b-102">Recordset2.BOF Property (DAO)</span></span>


<span data-ttu-id="e252b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e252b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e252b-p101">Retorna um valor que indica se a posição do registro atual é antes do primeiro registro em um objeto **Recordset**. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e252b-p101">Returns a value that indicates whether the current record position is before the first record in a **Recordset** object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e252b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e252b-106">Syntax</span></span>

<span data-ttu-id="e252b-107">*expressão* . BOF</span><span class="sxs-lookup"><span data-stu-id="e252b-107">*expression* .BOF</span></span>

<span data-ttu-id="e252b-108">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e252b-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e252b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e252b-109">Remarks</span></span>

<span data-ttu-id="e252b-110">Você pode usar as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao se mover de registro em registro.</span><span class="sxs-lookup"><span data-stu-id="e252b-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="e252b-111">A localização do ponteiro do registro atual determina os valores de retorno de **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="e252b-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="e252b-112">Se a propriedade **BOF** ou **EOF** for **True**, não existirá um registro atual.</span><span class="sxs-lookup"><span data-stu-id="e252b-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="e252b-p102">Se você abrir um objeto **Recordset** que não contenha registros, as propriedades **BOF** e **EOF** estarão definidas como **True** e a propriedade **RecordCount** do objeto **Recordset** estará definida como 0. Quando você abrir um objeto **Recordset** que contenha pelo menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** serão **False**; essas propriedades permanecerão como **False** até que você se mova além do início ou do final do objeto **Recordset** por meio do método **MovePrevious** ou **MoveNext**, respectivamente. Quando você se mover além do início ou do final do conjunto de registros, não existirá nenhum registro incluindo o registro atual .</span><span class="sxs-lookup"><span data-stu-id="e252b-p102">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0. When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively. When you move beyond the beginning or end of the recordset, there is no current record or no record exists.</span></span>

<span data-ttu-id="e252b-116">Se você excluir o último registro do objeto **Recordset**, as propriedades **BOF** e **EOF** permanecerão como **False** até você tentar o reposicionamento do registro atual.</span><span class="sxs-lookup"><span data-stu-id="e252b-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="e252b-p103">Se você usar o método **MoveLast** em um objeto **Recordset** com registros, o último registro se tornará o registro atual; se você então usar o método **MoveNext**, o registro atual se tornará inválido e a propriedade **EOF** será definida como **Verdadeiro**. De modo inverso, se você usar o método **MoveFirst** em um objeto **Recordset** com registros, o primeiro registro se tornará o registro atual; se você então usar o método **MovePrevious**, não haverá registro atual e a propriedade **BOF** será definida como **Verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="e252b-p103">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**. Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="e252b-119">Normalmente, quando você trabalhar com todos os registros em um objeto **Recordset**, seu código fará um loop pelos registros usando o método **MoveNext** até a propriedade **EOF** ser definida como **Verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="e252b-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="e252b-120">Se você usar o método **MoveNext** enquanto a propriedade **EOF** estiver definida como **Verdadeiro** ou o método **MovePrevious** enquanto a propriedade **BOF** estiver definida como **Verdadeiro**, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="e252b-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="e252b-121">Esta tabela mostra quais métodos Move são permitidos com combinações diferentes das propriedades **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="e252b-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="e252b-122">Métodos MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="e252b-122">MoveFirst,</span></span><br />
<span data-ttu-id="e252b-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="e252b-123">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="e252b-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="e252b-124">MovePrevious,</span></span><br />
<span data-ttu-id="e252b-125">Mover &lt; 0</span><span class="sxs-lookup"><span data-stu-id="e252b-125">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="e252b-126">Move 0</span><span class="sxs-lookup"><span data-stu-id="e252b-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="e252b-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="e252b-127">MoveNext,</span></span><br />
<span data-ttu-id="e252b-128">Mover &gt; 0</span><span class="sxs-lookup"><span data-stu-id="e252b-128">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e252b-129"><strong>BOF = verdadeiro,</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-129"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="e252b-130">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-130">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="e252b-131">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="e252b-132">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-132">Error</span></span></p></td>
<td><p><span data-ttu-id="e252b-133">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-133">Error</span></span></p></td>
<td><p><span data-ttu-id="e252b-134">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e252b-135"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-135"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="e252b-136">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-136">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="e252b-137">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="e252b-138">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="e252b-139">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-139">Error</span></span></p></td>
<td><p><span data-ttu-id="e252b-140">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e252b-141">Ambas <strong>Verdadeiras</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="e252b-142">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-142">Error</span></span></p></td>
<td><p><span data-ttu-id="e252b-143">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-143">Error</span></span></p></td>
<td><p><span data-ttu-id="e252b-144">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-144">Error</span></span></p></td>
<td><p><span data-ttu-id="e252b-145">Erro</span><span class="sxs-lookup"><span data-stu-id="e252b-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e252b-146">Ambas <strong>Falsas</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="e252b-147">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="e252b-148">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="e252b-149">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="e252b-150">Permitido</span><span class="sxs-lookup"><span data-stu-id="e252b-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e252b-p104">Permitir um método Move significa que o método localizará com êxito um registro. Ele simplesmente indica que uma tentativa de executar o método Move especificado é permitida e não gerará um erro. O estado das propriedades **BOF** e **EOF** pode ser alterado como resultado da tentativa de Move.</span><span class="sxs-lookup"><span data-stu-id="e252b-p104">Allowing a Move method doesn't mean that the method will successfully locate a record. It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error. The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="e252b-p105">Um método **OpenRecordset** invoca internamente um método **MoveFirst**. Portanto, usar um método **OpenRecordset** em um conjunto de registros vazio define as propriedades **BOF** e **EOF** como **Verdadeiras** (consulte a tabela a seguir par obter o comportamento de um método **MoveFirst** com falha).</span><span class="sxs-lookup"><span data-stu-id="e252b-p105">An **OpenRecordset** method internally invokes a **MoveFirst** method. Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**. (See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="e252b-157">Todos os métodos Move localizados com sucesso em um registro definirão as propriedades **BOF** e **EOF** como **False**.</span><span class="sxs-lookup"><span data-stu-id="e252b-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="e252b-158">Em umespaço de trabalho do Microsoft Access, se você adicionar um registro a um conjunto de registros vazio, **BOF** se tornará **False**, mas **EOF** permanecerá **True**, indicando que a posição atual é o final do conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="e252b-158">In a Microsoft Access workspace, if you add a record to an empty recordset, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of recordset.</span></span>

<span data-ttu-id="e252b-159">Qualquer método **Delete**, mesmo que remova somente o registro restante de um conjunto de registros, não alterará a definição da propriedade **BOF** ou **EOF**.</span><span class="sxs-lookup"><span data-stu-id="e252b-159">Any **Delete** method, even if it removes the only remaining record from a recordset, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="e252b-160">A tabela a seguir mostra como os métodos Move que não localizam um registro afetam as definições das propriedades **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="e252b-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="e252b-161">BOF</span><span class="sxs-lookup"><span data-stu-id="e252b-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="e252b-162">EOF</span><span class="sxs-lookup"><span data-stu-id="e252b-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e252b-163"><strong>Métodos MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="e252b-164"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="e252b-165"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e252b-166"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="e252b-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="e252b-167">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="e252b-167">No change</span></span></p></td>
<td><p><span data-ttu-id="e252b-168">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="e252b-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e252b-169"><strong>MovePrevious</strong>, <strong>mova</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="e252b-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="e252b-170"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="e252b-171">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="e252b-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e252b-172"><strong>MoveNext</strong>, <strong>mova</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="e252b-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="e252b-173">Nenhuma alteração</span><span class="sxs-lookup"><span data-stu-id="e252b-173">No change</span></span></p></td>
<td><p><span data-ttu-id="e252b-174"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="e252b-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

