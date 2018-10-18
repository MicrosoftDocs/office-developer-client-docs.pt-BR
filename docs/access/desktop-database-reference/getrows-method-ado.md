---
title: Método GetRows (ADO)
TOCTitle: GetRows Method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0f7f38e44e26238e5a55feaaad302bbf427d678
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606147"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="b6352-102">Método GetRows (ADO)</span><span class="sxs-lookup"><span data-stu-id="b6352-102">GetRows Method (ADO)</span></span>


<span data-ttu-id="b6352-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6352-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="b6352-104">Recupera vários registros de um objeto [Recordset](recordset-object-ado.md) para dentro de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b6352-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6352-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6352-105">Syntax</span></span>

<span data-ttu-id="b6352-106">*matriz* = *recordset*. GetRows (*linhas*, *Iniciar*, *campos* )</span><span class="sxs-lookup"><span data-stu-id="b6352-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

<span data-ttu-id="b6352-107"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="b6352-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="b6352-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b6352-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="b6352-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b6352-109">Return value</span></span>
>>>>>>> <span data-ttu-id="b6352-110">mestre</span><span class="sxs-lookup"><span data-stu-id="b6352-110">master</span></span>

<span data-ttu-id="b6352-111">Retorna uma **Variant** cujo valor é uma matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="b6352-111">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6352-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6352-112">Parameters</span></span>

  - <span data-ttu-id="b6352-113">*Rows*</span><span class="sxs-lookup"><span data-stu-id="b6352-113">*Rows*</span></span>

  - <span data-ttu-id="b6352-p101">Opcional. Um valor [GetRowsOptionEnum](getrowsoptionenum.md) que indica o número de registros a serem recuperados. O padrão é **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="b6352-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>

  - <span data-ttu-id="b6352-117">*Start*</span><span class="sxs-lookup"><span data-stu-id="b6352-117">*Start*</span></span>

  - <span data-ttu-id="b6352-p102">Opcional. Um valor **String** ou **Variant** que é avaliado para o indicador de um registro a partir do qual a operação **GetRows** deve começar. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="b6352-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

  - <span data-ttu-id="b6352-121">*Fields*</span><span class="sxs-lookup"><span data-stu-id="b6352-121">*Fields*</span></span>

  - <span data-ttu-id="b6352-p103">Opcional. Uma **Variant** que representa um único nome de campo ou posição ordinal, ou uma matriz de nomes de campos ou números de posição ordinal. O ADO retorna apenas os dados nesses campos.</span><span class="sxs-lookup"><span data-stu-id="b6352-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6352-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6352-125">Remarks</span></span>

<span data-ttu-id="b6352-126">Utilize o método **GetRows** para copiar registros de um **Recordset** para uma matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="b6352-126">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="b6352-127">O primeiro subscrito identifica o campo e o segundo identifica o número do registro.</span><span class="sxs-lookup"><span data-stu-id="b6352-127">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="b6352-128">A *matriz* variável é automaticamente dimensionada até atingir o tamanho correto quando o método **GetRows** retorna os dados.</span><span class="sxs-lookup"><span data-stu-id="b6352-128">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="b6352-129">Se você não especificar um valor para o argumento de *linhas* , o método **GetRows** automaticamente recupera todos os registros no objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b6352-129">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="b6352-130">Se você solicitar mais registros do que os disponíveis, **GetRows** retornará apenas o número de registros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b6352-130">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="b6352-131">Se o objeto **Recordset** suporta indicadores, você pode especificar em qual registro método **GetRows** deve começar a recuperar dados passando o valor da propriedade de [indicador](bookmark-property-ado.md) do registro no argumento *Iniciar* .</span><span class="sxs-lookup"><span data-stu-id="b6352-131">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="b6352-132">Se você deseja restringir os campos que a chamada a **GetRows** retorna, você poderá passar um número/nome de campo único ou uma matriz de números/nomes de campo no argumento *Fields* .</span><span class="sxs-lookup"><span data-stu-id="b6352-132">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="b6352-133">Depois de chamar **GetRows**, o próximo registro não-lido tornar-se-a o registro atual, ou a propriedade [EOF](bof-eof-properties-ado.md) será definida como **True** se não houver mais registros.</span><span class="sxs-lookup"><span data-stu-id="b6352-133">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

