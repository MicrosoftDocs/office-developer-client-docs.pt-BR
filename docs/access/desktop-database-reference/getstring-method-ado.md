---
title: Método GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292185"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="53c2c-102">Método GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="53c2c-102">GetString method (ADO)</span></span>

<span data-ttu-id="53c2c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53c2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53c2c-104">Retorna o [Recordset](recordset-object-ado.md) como uma sequência.</span><span class="sxs-lookup"><span data-stu-id="53c2c-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c2c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53c2c-105">Syntax</span></span>

<span data-ttu-id="53c2c-106">\*\* = *Conjunto de registros*Variant. GetString (*StringFormat*, *numrows*, *ColumnDelimiter*, \*\*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="53c2c-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="53c2c-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53c2c-107">Return value</span></span>

<span data-ttu-id="53c2c-108">Retorna o **Recordset** como uma **Variant** avaliada como sequência (BSTR).</span><span class="sxs-lookup"><span data-stu-id="53c2c-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="53c2c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53c2c-109">Parameters</span></span>

|<span data-ttu-id="53c2c-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="53c2c-110">Parameter</span></span>|<span data-ttu-id="53c2c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="53c2c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="53c2c-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="53c2c-112">*StringFormat*</span></span> |<span data-ttu-id="53c2c-p101">Um valor [StringFormatEnum](stringformatenum.md) que especifica como o **Recordset** deve ser convertido em uma sequência. Os parâmetros *RowDelimiter*, *ColumnDelimiter* e *NullExpr* são utilizados apenas com um *StringFormat* igual a **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="53c2c-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="53c2c-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="53c2c-115">*NumRows*</span></span> |<span data-ttu-id="53c2c-p102">Opcional. O número de linhas a ser convertido no **Recordset**. Se *NumRows* não for especificado ou se for maior que o número total de linhas no **Recordset**, todas as linhas no **Recordset** serão convertidas.</span><span class="sxs-lookup"><span data-stu-id="53c2c-p102">Optional. The number of rows to be converted in the **Recordset**. If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="53c2c-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="53c2c-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="53c2c-p103">Opcional. Um delimitador utilizado entre colunas, se especificado; caso contrário, o caractere TAB.</span><span class="sxs-lookup"><span data-stu-id="53c2c-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="53c2c-122">*ObjectDelimiter*</span><span class="sxs-lookup"><span data-stu-id="53c2c-122">*RowDelimiter*</span></span> |<span data-ttu-id="53c2c-p104">Opcional. Um delimitador utilizado entre linhas, se especificado; caso contrário, o caractere CARRIAGE RETURN.</span><span class="sxs-lookup"><span data-stu-id="53c2c-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="53c2c-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="53c2c-125">*NullExpr*</span></span> |<span data-ttu-id="53c2c-p105">Opcional. Uma expressão utilizada no lugar de um valor nulo, se especificada; caso contrário, a sequência vazia.</span><span class="sxs-lookup"><span data-stu-id="53c2c-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="53c2c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="53c2c-128">Remarks</span></span>

<span data-ttu-id="53c2c-p106">Dados brutos, mas sem dados de esquema, são salvos na sequência. Portanto, um **Recordset** não pode ser reaberto utilizando-se essa sequência.</span><span class="sxs-lookup"><span data-stu-id="53c2c-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="53c2c-131">Este método é equivalente ao método **GetClipString** do RDO.</span><span class="sxs-lookup"><span data-stu-id="53c2c-131">This method is equivalent to the RDO **GetClipString** method.</span></span>

