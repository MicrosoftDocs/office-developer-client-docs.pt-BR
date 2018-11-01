---
title: Método - de clone ActiveX Data Objects (ADO)
TOCTitle: Clone Method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efff94e9f86d1fac7fd8b3716b1df2029bd32eb9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876383"
---
# <a name="clone-method-ado"></a><span data-ttu-id="967e1-102">Método Clone (ADO)</span><span class="sxs-lookup"><span data-stu-id="967e1-102">Clone Method (ADO)</span></span>


<span data-ttu-id="967e1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="967e1-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="967e1-p101">Cria um objeto [Recordset](recordset-object-ado.md) duplicado a partir de um objeto **Recordset** existente. Opcionalmente, especifica que o clone seja somente leitura.</span><span class="sxs-lookup"><span data-stu-id="967e1-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="967e1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="967e1-106">Syntax</span></span>

<span data-ttu-id="967e1-107">**Definir** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="967e1-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="967e1-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="967e1-108">Return value</span></span>

<span data-ttu-id="967e1-109">Retorna uma referência do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="967e1-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="967e1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="967e1-110">Parameters</span></span>

  - <span data-ttu-id="967e1-111">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="967e1-111">*rstDuplicate*</span></span>

  - <span data-ttu-id="967e1-112">Uma variável de objeto que identifica o objeto **Recordset** duplicado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="967e1-112">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

  - <span data-ttu-id="967e1-113">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="967e1-113">*rstOriginal*</span></span>

  - <span data-ttu-id="967e1-114">Uma variável de objeto que identifica o objeto **Recordset** a ser duplicado.</span><span class="sxs-lookup"><span data-stu-id="967e1-114">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

  - <span data-ttu-id="967e1-115">*LockType*</span><span class="sxs-lookup"><span data-stu-id="967e1-115">*LockType*</span></span>

  - <span data-ttu-id="967e1-p102">Opcional. Um valor [LockTypeEnum](locktypeenum.md) que especifica o tipo de bloqueio do **Recordset** original ou um **Recordset** somente leitura. Os valores válidos são **adLockUnspecified** ou **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="967e1-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="967e1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="967e1-119">Remarks</span></span>

<span data-ttu-id="967e1-p103">Utilize o método **Clone** para criar diversos objetos **Recordset** duplicados, especialmente se deseja manter mais de um registro atual em um determinado conjunto de registros. A utilização do método **Clone** é mais eficiente do que a criação e abertura de um novo objeto **Recordset** com a mesma definição que o original.</span><span class="sxs-lookup"><span data-stu-id="967e1-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="967e1-p104">A propriedade [Filter](filter-property-ado.md) do **Recordset** original, se existir, não será aplicada ao clone. Defina a propriedade **Filter** do novo **Recordset** para filtrar os resultados. A forma mais simples de copiar qualquer valor de **Filter** existente é atribuí-lo diretamente, como a seguir:</span><span class="sxs-lookup"><span data-stu-id="967e1-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="967e1-125">O registro atual de um clone recém-criado é definido para o primeiro registro.</span><span class="sxs-lookup"><span data-stu-id="967e1-125">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="967e1-p105">As alterações efetuadas em um objeto **Recordset** são visíveis em todos os seus clones, independentemente do tipo do cursor. No entanto, depois de executar [Requery](requery-method-ado.md) no **Recordset** original, os clones não mais estarão sincronizados com o original.</span><span class="sxs-lookup"><span data-stu-id="967e1-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="967e1-128">Fechar o **Recordset** original não fecha suas cópias, assim como fechar uma cópia não fecha o original e nenhuma das demais cópias.</span><span class="sxs-lookup"><span data-stu-id="967e1-128">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="967e1-p106">É possível clonar apenas um objeto **Recordset** que suporte indicadores. Os valores de indicadores são intercambiáveis; isto é, uma referência de indicador de um objeto **Recordset** se refere ao mesmo registro em qualquer um de seus clones.</span><span class="sxs-lookup"><span data-stu-id="967e1-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="967e1-p107">Alguns eventos **Recordset** que são disparados também o serão em todos os clones do **Recordset**. No entanto, como o registro atual pode ser diferente entre os **Recordsets** clonados, os eventos podem não ser válidos para o clone.</span><span class="sxs-lookup"><span data-stu-id="967e1-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="967e1-133">Por exemplo, se você alterar o valor de um campo, ocorrerá um evento [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) no **Recordset** alterado e em todos os clones.</span><span class="sxs-lookup"><span data-stu-id="967e1-133">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="967e1-134">O parâmetro de *campos* do evento **WillChangeField** de um clonada **Recordset** (onde a alteração não foi realizada) simplesmente fará referência aos campos do registro atual de clone, o que pode ser um registro diferente de formato do registro do original **Recordset** onde a mudança ocorreu.</span><span class="sxs-lookup"><span data-stu-id="967e1-134">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="967e1-135">A tabela a seguir fornece uma lista completa de todos os eventos de **Recordset** e indica se eles são válidos e disparados para quaisquer clones de recordset gerados utilizando-se o método **Clone**.</span><span class="sxs-lookup"><span data-stu-id="967e1-135">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="967e1-136">Evento</span><span class="sxs-lookup"><span data-stu-id="967e1-136">Event</span></span></p></th>
<th><p><span data-ttu-id="967e1-137">Disparado nos clones?</span><span class="sxs-lookup"><span data-stu-id="967e1-137">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="967e1-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="967e1-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-139">Não</span><span class="sxs-lookup"><span data-stu-id="967e1-139">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="967e1-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="967e1-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-141">Não</span><span class="sxs-lookup"><span data-stu-id="967e1-141">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="967e1-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="967e1-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-143">Não</span><span class="sxs-lookup"><span data-stu-id="967e1-143">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="967e1-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="967e1-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-145">Sim</span><span class="sxs-lookup"><span data-stu-id="967e1-145">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="967e1-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="967e1-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-147">Não</span><span class="sxs-lookup"><span data-stu-id="967e1-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="967e1-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="967e1-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-149">Sim</span><span class="sxs-lookup"><span data-stu-id="967e1-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="967e1-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="967e1-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-151">Não</span><span class="sxs-lookup"><span data-stu-id="967e1-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="967e1-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="967e1-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-153">Sim</span><span class="sxs-lookup"><span data-stu-id="967e1-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="967e1-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="967e1-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-155">Sim</span><span class="sxs-lookup"><span data-stu-id="967e1-155">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="967e1-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="967e1-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-157">Não</span><span class="sxs-lookup"><span data-stu-id="967e1-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="967e1-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="967e1-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="967e1-159">Não</span><span class="sxs-lookup"><span data-stu-id="967e1-159">No</span></span></p></td>
</tr>
</tbody>
</table>

