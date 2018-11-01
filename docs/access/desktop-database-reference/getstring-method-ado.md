---
title: Método GetString (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6c4de1278a093a1b0d4493c5dd994afe6a5d1b8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879869"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="140f3-102">Método GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="140f3-102">GetString Method (ADO)</span></span>


<span data-ttu-id="140f3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="140f3-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="140f3-104">Retorna o [Recordset](recordset-object-ado.md) como uma sequência.</span><span class="sxs-lookup"><span data-stu-id="140f3-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="140f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="140f3-105">Syntax</span></span>

<span data-ttu-id="140f3-106">*Variant* = *recordset*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="140f3-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="140f3-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="140f3-107">Return value</span></span>

<span data-ttu-id="140f3-108">Retorna o **Recordset** como uma **Variant** avaliada como sequência (BSTR).</span><span class="sxs-lookup"><span data-stu-id="140f3-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="140f3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="140f3-109">Parameters</span></span>

  - <span data-ttu-id="140f3-110">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="140f3-110">*StringFormat*</span></span>

  - <span data-ttu-id="140f3-p101">Um valor [StringFormatEnum](stringformatenum.md) que especifica como o **Recordset** deve ser convertido em uma sequência. Os parâmetros *RowDelimiter*, *ColumnDelimiter* e *NullExpr* são utilizados apenas com um *StringFormat* igual a **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="140f3-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="140f3-113">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="140f3-113">*NumRows*</span></span>

  - <span data-ttu-id="140f3-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="140f3-114">Optional.</span></span> <span data-ttu-id="140f3-115">O número de linhas a ser convertido no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="140f3-115">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="140f3-116">Se *NumRows* não for especificado, ou se ele for maior que o número total de linhas no **conjunto de registros**, todas as linhas no **conjunto de registros** são convertidas.</span><span class="sxs-lookup"><span data-stu-id="140f3-116">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="140f3-117">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="140f3-117">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="140f3-p103">Opcional. Um delimitador utilizado entre colunas, se especificado; caso contrário, o caractere TAB.</span><span class="sxs-lookup"><span data-stu-id="140f3-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="140f3-120">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="140f3-120">*RowDelimiter*</span></span>

  - <span data-ttu-id="140f3-p104">Opcional. Um delimitador utilizado entre linhas, se especificado; caso contrário, o caractere CARRIAGE RETURN.</span><span class="sxs-lookup"><span data-stu-id="140f3-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="140f3-123">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="140f3-123">*NullExpr*</span></span>

  - <span data-ttu-id="140f3-p105">Opcional. Uma expressão utilizada no lugar de um valor nulo, se especificada; caso contrário, a sequência vazia.</span><span class="sxs-lookup"><span data-stu-id="140f3-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="140f3-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="140f3-126">Remarks</span></span>

<span data-ttu-id="140f3-p106">Dados brutos, mas sem dados de esquema, são salvos na sequência. Portanto, um **Recordset** não pode ser reaberto utilizando-se essa sequência.</span><span class="sxs-lookup"><span data-stu-id="140f3-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="140f3-129">Este método é equivalente ao método **GetClipString** do RDO.</span><span class="sxs-lookup"><span data-stu-id="140f3-129">This method is equivalent to the RDO **GetClipString** method.</span></span>

