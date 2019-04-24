---
title: Método getRows (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f7ce441eb837b76e824b55393741e0cf821bb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292220"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="56386-102">Método getRows (ADO)</span><span class="sxs-lookup"><span data-stu-id="56386-102">GetRows method (ADO)</span></span>

<span data-ttu-id="56386-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56386-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56386-104">Recupera vários registros de um objeto [Recordset](recordset-object-ado.md) para dentro de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="56386-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="56386-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56386-105">Syntax</span></span>

<span data-ttu-id="56386-106">\*\* = *conjunto de registros*de matriz. GetRows (*linhas*, *início*, *campos* )</span><span class="sxs-lookup"><span data-stu-id="56386-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="56386-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="56386-107">Return value</span></span>

<span data-ttu-id="56386-108">Retorna uma **Variant** cujo valor é uma matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="56386-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="56386-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56386-109">Parameters</span></span>

|<span data-ttu-id="56386-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="56386-110">Parameter</span></span>|<span data-ttu-id="56386-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="56386-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="56386-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="56386-112">*Rows*</span></span> |<span data-ttu-id="56386-p101">Opcional. Um valor [GetRowsOptionEnum](getrowsoptionenum.md) que indica o número de registros a serem recuperados. O padrão é **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="56386-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="56386-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="56386-116">*Start*</span></span> |<span data-ttu-id="56386-p102">Opcional. Um valor **String** ou **Variant** que é avaliado para o indicador de um registro a partir do qual a operação **GetRows** deve começar. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="56386-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="56386-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="56386-120">*Fields*</span></span> |<span data-ttu-id="56386-p103">Opcional. Uma **Variant** que representa um único nome de campo ou posição ordinal, ou uma matriz de nomes de campos ou números de posição ordinal. O ADO retorna apenas os dados nesses campos.</span><span class="sxs-lookup"><span data-stu-id="56386-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="56386-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="56386-124">Remarks</span></span>

<span data-ttu-id="56386-p104">Utilize o método **GetRows** para copiar registros de um **Recordset** para uma matriz bidimensional. O primeiro subscrito identifica o campo e o segundo identifica o número do registro. A variável *array* é dimensionada automaticamente para o tamanho correto quando o método **GetRows** retorna os dados.</span><span class="sxs-lookup"><span data-stu-id="56386-p104">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array. The first subscript identifies the field and the second identifies the record number. The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="56386-p105">Se você não especificar um valor para o argumento *Rows*, o método **GetRows** recupera automaticamente todos os registros no objeto **Recordset**. Se você solicitar mais registros do que os disponíveis, **GetRows** retornará apenas o número de registros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="56386-p105">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object. If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="56386-130">Se o objeto **Recordset** suportar indicadores, será possível especificar em qual registro o método **GetRows** deve começar a recuperar dados, passando-se o valor da propriedade [Bookmark](bookmark-property-ado.md) desse registro no argumento *Start*.</span><span class="sxs-lookup"><span data-stu-id="56386-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="56386-131">Se você deseja restringir os campos que a chamada a **GetRows** retorna, poderá passar um único número/nome de campo ou uma matriz de números/nomes de campo no argumento *Fields*.</span><span class="sxs-lookup"><span data-stu-id="56386-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="56386-132">Depois de chamar **GetRows**, o próximo registro não-lido tornar-se-a o registro atual, ou a propriedade [EOF](bof-eof-properties-ado.md) será definida como **True** se não houver mais registros.</span><span class="sxs-lookup"><span data-stu-id="56386-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

