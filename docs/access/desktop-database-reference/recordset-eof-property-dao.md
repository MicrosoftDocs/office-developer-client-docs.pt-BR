---
title: Propriedade Recordset.EOF (DAO)
TOCTitle: EOF Property
ms:assetid: aa82c6f9-89da-1061-437c-8ffb000744b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821459(v=office.15)
ms:contentKeyID: 48546950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 931de7dfc2cfb80726aafe7077c6107ec65d2f40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300606"
---
# <a name="recordseteof-property-dao"></a><span data-ttu-id="2cf9f-102">Propriedade Recordset.EOF (DAO)</span><span class="sxs-lookup"><span data-stu-id="2cf9f-102">Recordset.EOF Property (DAO)</span></span>


<span data-ttu-id="2cf9f-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cf9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2cf9f-104">Retorna um valor que indica se a posição do registro atual será depois do último registro em um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-104">Returns a value that indicates whether the current record position is after the last record in a **Recordset** object.</span></span> <span data-ttu-id="2cf9f-105">**Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf9f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cf9f-106">Syntax</span></span>

<span data-ttu-id="2cf9f-107">*expressão* .EOF</span><span class="sxs-lookup"><span data-stu-id="2cf9f-107">expression  . EOF</span></span>

<span data-ttu-id="2cf9f-108">*expressão* Uma variável que representa um objeto **Conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-108">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf9f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cf9f-109">Remarks</span></span>

<span data-ttu-id="2cf9f-110">Você pode usar as propriedades **BOF** e **EOF** para determinar se um objeto **Recordset** contém registros ou se você foi além dos limites de um objeto **Recordset** ao se mover de registro em registro.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="2cf9f-111">O local do ponteiro do registro atual determina os valores de retorno **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="2cf9f-112">Se a propriedade **BOF** ou **EOF** for **True**, não existirá um registro atual.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="2cf9f-p102">Se você abrir um objeto **Recordset** que não contenha registros, as propriedades **BOF** e **EOF** estarão definidas como **True** e a definição da propriedade **RecordCount** do objeto **Recordset** será 0. Quando você abrir um objeto **Recordset** que contenha pelo menos um registro, o primeiro registro será o registro atual e as propriedades **BOF** e **EOF** serão **False**. Essas propriedades permanecerão como **False** até que você se mova além do início ou do final do objeto **Recordset** por meio do método **MovePrevious** ou **MoveNext**, respectivamente. Quando você se mover além do início ou do final do **Recordset**, não existirá nenhum registro, incluindo o registro atual .</span><span class="sxs-lookup"><span data-stu-id="2cf9f-p102">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0. When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively. When you move beyond the beginning or end of the **Recordset**, there is no current record or no record exists.</span></span>

<span data-ttu-id="2cf9f-116">Se você excluir o último registro do objeto **Recordset**, as propriedades **BOF** e **EOF** permanecerão como **False** até você tentar o reposicionamento do registro atual.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="2cf9f-p103">Se você usar o método **MoveLast** em um objeto **Recordset** que contenha registros, o último registro se tornará o registro atual; mais tarde, se você usar o método **MoveNext**, o registro atual se tornará inválido e a propriedade **EOF** será definida como **True**. De modo inverso, se você usar o método **MoveFirst** em um objeto **Recordset** que contenha registros, o primeiro registro se tornará o registro atual; mais tarde, se você usar o método **MovePrevious**, não existirá nenhum registro atual e a propriedade **BOF** será definida como **True**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-p103">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**. Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="2cf9f-119">De um modo geral, quando você trabalhar com todos os registros em um objeto **Recordset**, o código fará um loop pelos registros usando o método **MoveNext** até que a propriedade **EOF** seja definida como **True**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="2cf9f-120">Se você usar o método **MoveNext** enquanto a propriedade **EOF** estiver definida como **True** ou o método **MovePrevious** enquanto a propriedade **BOF** estiver definida como **True**, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="2cf9f-121">Esta tabela mostra quais métodos Move são permitidos com diferentes combinações das propriedades **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="2cf9f-122">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="2cf9f-122">MoveFirst method</span></span><br />
<span data-ttu-id="2cf9f-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="2cf9f-123">MoveLast method</span></span></p></th>
<th><p><span data-ttu-id="2cf9f-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="2cf9f-124">MovePrevious method</span></span><br />
<span data-ttu-id="2cf9f-125">Move &lt; 0</span><span class="sxs-lookup"><span data-stu-id="2cf9f-125">&lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="2cf9f-126">Move 0</span><span class="sxs-lookup"><span data-stu-id="2cf9f-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="2cf9f-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="2cf9f-127">MoveNext method</span></span><br />
<span data-ttu-id="2cf9f-128">Move &gt; 0</span><span class="sxs-lookup"><span data-stu-id="2cf9f-128">&gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cf9f-129"><strong>BOF=True,</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-129"><strong>BOF=True,EOF=False</strong></span></span><br /><span data-ttu-id="2cf9f-130">
<strong>EOF=False</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-130">
<strong>BOF=True,EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf9f-131">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-132">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-132">Error</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-133">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-133">Error</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-134">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cf9f-135"><strong>BOF=False,</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-135"><strong>BOF=False,EOF=True</strong></span></span><br /><span data-ttu-id="2cf9f-136">
<strong>EOF=True</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-136">
<strong>BOF=False,EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf9f-137">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-138">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-139">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-139">Error</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-140">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cf9f-141">Ambas <strong>Verdadeiras</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf9f-142">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-142">Error</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-143">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-143">Error</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-144">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-144">Error</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-145">Erro</span><span class="sxs-lookup"><span data-stu-id="2cf9f-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cf9f-146">Ambas <strong>Falsas</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf9f-147">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-148">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-149">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-150">Permitido</span><span class="sxs-lookup"><span data-stu-id="2cf9f-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2cf9f-p104">Permitir um método Move significa que o método localizará com êxito um registro. Ele simplesmente indica que uma tentativa de executar o método Move especificado é permitida e não gerará um erro. O estado das propriedades **BOF** e **EOF** pode ser alterado como resultado da tentativa de Move.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-p104">Allowing a Move method doesn't mean that the method will successfully locate a record. It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error. The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="2cf9f-p105">Um método **OpenRecordset** chama internamente um método **MoveFirst**. Por esse motivo, o uso de um método **OpenRecordset** em um conjunto de registros vazio definirá as propriedades **BOF** e **EOF** como **True**. (Consulte a tabela a seguir para conhecer o comportamento de um método **MoveFirst** com falha.)</span><span class="sxs-lookup"><span data-stu-id="2cf9f-p105">An **OpenRecordset** method internally invokes a **MoveFirst** method. Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**. (See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="2cf9f-157">Todos os métodos Move localizados com sucesso em um registro definirão as propriedades **BOF** e **EOF** como **False**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="2cf9f-158">Em um espaço de trabalho do Microsoft Access, se você adicionar um registro a um **Recordset** vazio, **BOF** se tornará **False**, mas **EOF** permanecerá **True**, indicando que a posição atual está no final do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-158">In a Microsoft Access workspace, if you add a record to an empty **Recordset**, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of **Recordset**.</span></span>

<span data-ttu-id="2cf9f-159">Qualquer método **Delete**, mesmo que remova somente o registro restante de um **Recordset**, não alterará a definição da propriedade **BOF** ou **EOF**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-159">Any **Delete** method, even if it removes the only remaining record from a **Recordset**, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="2cf9f-160">A tabela a seguir mostra como os métodos Move que não localizam um registro afetam as configurações das propriedades **BOF** e **EOF**.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="2cf9f-161">BOF</span><span class="sxs-lookup"><span data-stu-id="2cf9f-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="2cf9f-162">EOF</span><span class="sxs-lookup"><span data-stu-id="2cf9f-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cf9f-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf9f-164"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf9f-165"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cf9f-166"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="2cf9f-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-167">Sem alteração</span><span class="sxs-lookup"><span data-stu-id="2cf9f-167">No change</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-168">Sem alteração</span><span class="sxs-lookup"><span data-stu-id="2cf9f-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cf9f-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="2cf9f-169">MovePrevious, Move < 0</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-170"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="2cf9f-171">Sem alteração</span><span class="sxs-lookup"><span data-stu-id="2cf9f-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cf9f-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="2cf9f-172">MoveNext, Move > 0</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-173">Sem alteração</span><span class="sxs-lookup"><span data-stu-id="2cf9f-173">No change</span></span></p></td>
<td><p><span data-ttu-id="2cf9f-174"><strong>Verdadeiro</strong></span><span class="sxs-lookup"><span data-stu-id="2cf9f-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

