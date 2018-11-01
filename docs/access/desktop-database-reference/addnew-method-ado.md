---
title: Método AddNew (ADO)
TOCTitle: AddNew Method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 720445d488f70f3e6219db65192946d4056ddfe4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886050"
---
# <a name="addnew-method-ado"></a><span data-ttu-id="3cd97-102">Método AddNew (ADO)</span><span class="sxs-lookup"><span data-stu-id="3cd97-102">AddNew Method (ADO)</span></span>


<span data-ttu-id="3cd97-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cd97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cd97-104">Cria um novo registro para um objeto [Recordset](recordset-object-ado.md) atualizável.</span><span class="sxs-lookup"><span data-stu-id="3cd97-104">Creates a new record for an updatable [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cd97-105">Syntax</span></span>

<span data-ttu-id="3cd97-106">*conjunto de registros*. AddNew *FieldList*, *valores*</span><span class="sxs-lookup"><span data-stu-id="3cd97-106">*recordset*.AddNew *FieldList*, *Values*</span></span>

## <a name="parameters"></a><span data-ttu-id="3cd97-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cd97-107">Parameters</span></span>

  - <span data-ttu-id="3cd97-108">*recordset*</span><span class="sxs-lookup"><span data-stu-id="3cd97-108">*recordset*</span></span>

  - <span data-ttu-id="3cd97-109">Um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3cd97-109">A **Recordset** object.</span></span>

  - <span data-ttu-id="3cd97-110">*FieldList*</span><span class="sxs-lookup"><span data-stu-id="3cd97-110">*FieldList*</span></span>

  - <span data-ttu-id="3cd97-p101">Opcional. Um único nome, ou uma matriz de nomes ou posições ordinais dos campos no novo registro.</span><span class="sxs-lookup"><span data-stu-id="3cd97-p101">Optional. A single name, or an array of names or ordinal positions of the fields in the new record.</span></span>

  - <span data-ttu-id="3cd97-113">*Values*</span><span class="sxs-lookup"><span data-stu-id="3cd97-113">*Values*</span></span>

  - <span data-ttu-id="3cd97-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3cd97-114">Optional.</span></span> <span data-ttu-id="3cd97-115">Um único valor, ou uma matriz de valores para os campos no novo registro.</span><span class="sxs-lookup"><span data-stu-id="3cd97-115">A single value, or an array of values for the fields in the new record.</span></span> <span data-ttu-id="3cd97-116">Se *Fieldlist* é uma matriz, os *valores* também deve ser uma matriz com o mesmo número de membros; Caso contrário, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="3cd97-116">If *Fieldlist* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs.</span></span> <span data-ttu-id="3cd97-117">A ordem dos nomes de campo deve corresponder à ordem dos valores de campo em cada matriz.</span><span class="sxs-lookup"><span data-stu-id="3cd97-117">The order of field names must match the order of field values in each array.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd97-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cd97-118">Remarks</span></span>

<span data-ttu-id="3cd97-p103">Use o método **AddNew** para criar e inicializar um novo registro. Use o método [Supports](supports-method-ado.md) com **adAddNew** (valor [CursorOptionEnum](cursoroptionenum.md)) para verificar se é possível adicionar registros ao objeto **Recordset** atual.</span><span class="sxs-lookup"><span data-stu-id="3cd97-p103">Use the **AddNew** method to create and initialize a new record. Use the [Supports](supports-method-ado.md) method with **adAddNew** (a [CursorOptionEnum](cursoroptionenum.md) value) to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="3cd97-p104">Depois que você chamar o método **AddNew**, o novo registro passará a ser o registro atual e permanecerá atual depois que o método [Update](update-method-ado.md) for chamado. Como o novo registro é acrescentado a **Recordset**, uma chamada para **MoveNext** após Update ultrapassará o fim de **Recordset**, tornando **EOF** True. Se o objeto **Recordset** não oferecer suporte a indicadores, você não poderá acessar o novo registro ao passar para outro. Dependendo do tipo de cursor, talvez seja necessário chamar o método [Requery](requery-method-ado.md) para tornar o novo registro acessível.</span><span class="sxs-lookup"><span data-stu-id="3cd97-p104">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the [Update](update-method-ado.md) method. Since the new record is appended to the **Recordset**, a call to **MoveNext** following the Update will move past the end of the **Recordset**, making **EOF** True. If the **Recordset** object does not support bookmarks, you may not be able to access the new record once you move to another record. Depending on your cursor type, you may need to call the [Requery](requery-method-ado.md) method to make the new record accessible.</span></span>

<span data-ttu-id="3cd97-125">Se você chamar **AddNew** durante a edição do registro atual ou a adição de um novo registro, o ADO chamará o método **Update** para salvar as alterações e, em seguida, criará o novo registro.</span><span class="sxs-lookup"><span data-stu-id="3cd97-125">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="3cd97-126">O comportamento do método **AddNew** depende do modo de atualização do objeto **Recordset** e se serão passados os argumentos *Fieldlist* e *Values* .</span><span class="sxs-lookup"><span data-stu-id="3cd97-126">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *Fieldlist* and *Values* arguments.</span></span>

<span data-ttu-id="3cd97-p105">No *modo de atualização imediato* (em que o provedor grava as alterações na fonte de dados subjacente quando você chama o método **Update**), se você chamar o método **AddNew** sem argumentos, a propriedade [EditMode](editmode-property-ado.md) será definida como **adEditAdd** (valor [EditModeEnum](editmodeenum.md)). O provedor armazena localmente em cache qualquer alteração de valor de campo. A chamada do método **Update** posta o novo registro no banco de dados e redefine a propriedade **EditMode** como  **adEditNone** (valor **EditModeEnum**). Se você passar os argumentos *Fieldlist* e *Values*, o ADO postará o novo registro imediatamente no banco de dados (nenhuma chamada de **Update** é necessária); o valor da propriedade **EditMode** não é alterado (**adEditNone**).</span><span class="sxs-lookup"><span data-stu-id="3cd97-p105">In *immediate update mode* (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the [EditMode](editmode-property-ado.md) property to **adEditAdd** (an [EditModeEnum](editmodeenum.md) value). The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone** (an **EditModeEnum** value). If you pass the *Fieldlist* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="3cd97-131">No *modo de atualização em lotes* (no qual o provedor caches várias alterações e grava-los à fonte de dados subjacente somente quando você chamar o método [UpdateBatch](updatebatch-method-ado.md) ), chamar o método **AddNew** sem argumentos define a **EditMode** propriedade para **adEditAdd**.</span><span class="sxs-lookup"><span data-stu-id="3cd97-131">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="3cd97-132">O provedor armazena no cache local as alterações de valores de campo.</span><span class="sxs-lookup"><span data-stu-id="3cd97-132">The provider caches any field value changes locally.</span></span> <span data-ttu-id="3cd97-133">A chamada do método **Update** adiciona o novo registro ao **Recordset** atual e redefine a propriedade **EditMode** em **adEditNone**, mas o provedor não posta as alterações no banco de dados subjacente até a chamada do método **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="3cd97-133">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="3cd97-134">Se você passar os argumentos *Fieldlist* e *Values* , ADO envia o novo registro para o provedor de armazenamento em cache; Você precisará chamar o método **UpdateBatch** para lançar o novo registro no banco de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="3cd97-134">If you pass the *Fieldlist* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span>

