---
title: Método - de clone ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17284fd61c44fe17f1c2661eff204c8827bf8e80
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922339"
---
# <a name="clone-method-ado"></a><span data-ttu-id="a66ca-102">Método Clone (ADO)</span><span class="sxs-lookup"><span data-stu-id="a66ca-102">Clone method (ADO)</span></span>


<span data-ttu-id="a66ca-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a66ca-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="a66ca-p101">Cria um objeto [Recordset](recordset-object-ado.md) duplicado a partir de um objeto **Recordset** existente. Opcionalmente, especifica que o clone seja somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a66ca-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a66ca-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a66ca-106">Syntax</span></span>

<span data-ttu-id="a66ca-107">**Definir** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="a66ca-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="a66ca-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a66ca-108">Return value</span></span>

<span data-ttu-id="a66ca-109">Retorna uma referência do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a66ca-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="a66ca-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a66ca-110">Parameters</span></span>

  - <span data-ttu-id="a66ca-111">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="a66ca-111">*rstDuplicate*</span></span>

  - <span data-ttu-id="a66ca-112">Uma variável de objeto que identifica o objeto **Recordset** duplicado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a66ca-112">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

  - <span data-ttu-id="a66ca-113">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="a66ca-113">*rstOriginal*</span></span>

  - <span data-ttu-id="a66ca-114">Uma variável de objeto que identifica o objeto **Recordset** a ser duplicado.</span><span class="sxs-lookup"><span data-stu-id="a66ca-114">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

  - <span data-ttu-id="a66ca-115">*LockType*</span><span class="sxs-lookup"><span data-stu-id="a66ca-115">*LockType*</span></span>

  - <span data-ttu-id="a66ca-p102">Opcional. Um valor [LockTypeEnum](locktypeenum.md) que especifica o tipo de bloqueio do **Recordset** original ou um **Recordset** somente leitura. Os valores válidos são **adLockUnspecified** ou **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="a66ca-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a66ca-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a66ca-119">Remarks</span></span>

<span data-ttu-id="a66ca-p103">Utilize o método **Clone** para criar diversos objetos **Recordset** duplicados, especialmente se deseja manter mais de um registro atual em um determinado conjunto de registros. A utilização do método **Clone** é mais eficiente do que a criação e abertura de um novo objeto **Recordset** com a mesma definição que o original.</span><span class="sxs-lookup"><span data-stu-id="a66ca-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="a66ca-p104">A propriedade [Filter](filter-property-ado.md) do **Recordset** original, se existir, não será aplicada ao clone. Defina a propriedade **Filter** do novo **Recordset** para filtrar os resultados. A forma mais simples de copiar qualquer valor de **Filter** existente é atribuí-lo diretamente, como a seguir:</span><span class="sxs-lookup"><span data-stu-id="a66ca-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="a66ca-125">O registro atual de um clone recém-criado é definido para o primeiro registro.</span><span class="sxs-lookup"><span data-stu-id="a66ca-125">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="a66ca-p105">As alterações efetuadas em um objeto **Recordset** são visíveis em todos os seus clones, independentemente do tipo do cursor. No entanto, depois de executar [Requery](requery-method-ado.md) no **Recordset** original, os clones não mais estarão sincronizados com o original.</span><span class="sxs-lookup"><span data-stu-id="a66ca-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="a66ca-128">Fechar o **Recordset** original não fecha suas cópias, assim como fechar uma cópia não fecha o original e nenhuma das demais cópias.</span><span class="sxs-lookup"><span data-stu-id="a66ca-128">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="a66ca-p106">É possível clonar apenas um objeto **Recordset** que suporte indicadores. Os valores de indicadores são intercambiáveis; isto é, uma referência de indicador de um objeto **Recordset** se refere ao mesmo registro em qualquer um de seus clones.</span><span class="sxs-lookup"><span data-stu-id="a66ca-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="a66ca-p107">Alguns eventos **Recordset** que são disparados também o serão em todos os clones do **Recordset**. No entanto, como o registro atual pode ser diferente entre os **Recordsets** clonados, os eventos podem não ser válidos para o clone.</span><span class="sxs-lookup"><span data-stu-id="a66ca-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="a66ca-133">Por exemplo, se você alterar o valor de um campo, ocorrerá um evento [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) no **Recordset** alterado e em todos os clones.</span><span class="sxs-lookup"><span data-stu-id="a66ca-133">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="a66ca-134">O parâmetro de *campos* do evento **WillChangeField** de um clonada **Recordset** (onde a alteração não foi realizada) simplesmente fará referência aos campos do registro atual de clone, o que pode ser um registro diferente de formato do registro do original **Recordset** onde a mudança ocorreu.</span><span class="sxs-lookup"><span data-stu-id="a66ca-134">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="a66ca-135">A tabela a seguir fornece uma lista completa de todos os eventos de **Recordset** e indica se eles são válidos e disparados para quaisquer clones de recordset gerados utilizando-se o método **Clone**.</span><span class="sxs-lookup"><span data-stu-id="a66ca-135">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a66ca-136">Evento</span><span class="sxs-lookup"><span data-stu-id="a66ca-136">Event</span></span></p></th>
<th><p><span data-ttu-id="a66ca-137">Disparado nos clones?</span><span class="sxs-lookup"><span data-stu-id="a66ca-137">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a66ca-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-139">Não</span><span class="sxs-lookup"><span data-stu-id="a66ca-139">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a66ca-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-141">Não</span><span class="sxs-lookup"><span data-stu-id="a66ca-141">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a66ca-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-143">Não</span><span class="sxs-lookup"><span data-stu-id="a66ca-143">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a66ca-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-145">Sim</span><span class="sxs-lookup"><span data-stu-id="a66ca-145">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a66ca-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-147">Não</span><span class="sxs-lookup"><span data-stu-id="a66ca-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a66ca-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-149">Sim</span><span class="sxs-lookup"><span data-stu-id="a66ca-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a66ca-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-151">Não</span><span class="sxs-lookup"><span data-stu-id="a66ca-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a66ca-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-153">Sim</span><span class="sxs-lookup"><span data-stu-id="a66ca-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a66ca-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-155">Sim</span><span class="sxs-lookup"><span data-stu-id="a66ca-155">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a66ca-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-157">Não</span><span class="sxs-lookup"><span data-stu-id="a66ca-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a66ca-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="a66ca-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="a66ca-159">Não</span><span class="sxs-lookup"><span data-stu-id="a66ca-159">No</span></span></p></td>
</tr>
</tbody>
</table>

