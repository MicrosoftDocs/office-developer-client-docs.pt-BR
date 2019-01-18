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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698208"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="0d9ac-102">Método GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d9ac-102">GetString method (ADO)</span></span>

<span data-ttu-id="0d9ac-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d9ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d9ac-104">Retorna o [Recordset](recordset-object-ado.md) como uma sequência.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9ac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d9ac-105">Syntax</span></span>

<span data-ttu-id="0d9ac-106">*Variant* = *recordset*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="0d9ac-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="0d9ac-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0d9ac-107">Return value</span></span>

<span data-ttu-id="0d9ac-108">Retorna o **Recordset** como uma **Variant** avaliada como sequência (BSTR).</span><span class="sxs-lookup"><span data-stu-id="0d9ac-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="0d9ac-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d9ac-109">Parameters</span></span>

|<span data-ttu-id="0d9ac-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d9ac-110">Parameter</span></span>|<span data-ttu-id="0d9ac-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d9ac-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0d9ac-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="0d9ac-112">*StringFormat*</span></span> |<span data-ttu-id="0d9ac-p101">Um valor [StringFormatEnum](stringformatenum.md) que especifica como o **Recordset** deve ser convertido em uma sequência. Os parâmetros *RowDelimiter*, *ColumnDelimiter* e *NullExpr* são utilizados apenas com um *StringFormat* igual a **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="0d9ac-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="0d9ac-115">*NumRows*</span></span> |<span data-ttu-id="0d9ac-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-116">Optional.</span></span> <span data-ttu-id="0d9ac-117">O número de linhas a ser convertido no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="0d9ac-118">Se *NumRows* não for especificado, ou se ele for maior que o número total de linhas no **conjunto de registros**, todas as linhas no **conjunto de registros** são convertidas.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="0d9ac-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="0d9ac-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="0d9ac-p103">Opcional. Um delimitador utilizado entre colunas, se especificado; caso contrário, o caractere TAB.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="0d9ac-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="0d9ac-122">*RowDelimiter*</span></span> |<span data-ttu-id="0d9ac-p104">Opcional. Um delimitador utilizado entre linhas, se especificado; caso contrário, o caractere CARRIAGE RETURN.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="0d9ac-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="0d9ac-125">*NullExpr*</span></span> |<span data-ttu-id="0d9ac-p105">Opcional. Uma expressão utilizada no lugar de um valor nulo, se especificada; caso contrário, a sequência vazia.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0d9ac-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d9ac-128">Remarks</span></span>

<span data-ttu-id="0d9ac-p106">Dados brutos, mas sem dados de esquema, são salvos na sequência. Portanto, um **Recordset** não pode ser reaberto utilizando-se essa sequência.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="0d9ac-131">Este método é equivalente ao método **GetClipString** do RDO.</span><span class="sxs-lookup"><span data-stu-id="0d9ac-131">This method is equivalent to the RDO **GetClipString** method.</span></span>

