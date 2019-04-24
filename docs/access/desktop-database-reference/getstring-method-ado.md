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
# <a name="getstring-method-ado"></a>Método GetString (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Retorna o [Recordset](recordset-object-ado.md) como uma sequência.

## <a name="syntax"></a>Sintaxe

** = *Conjunto de registros*Variant. GetString (*StringFormat*, *numrows*, *ColumnDelimiter*, **, *NullExpr*)

## <a name="return-value"></a>Valor de retorno

Retorna o **Recordset** como uma **Variant** avaliada como sequência (BSTR).

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*StringFormat* |Um valor [StringFormatEnum](stringformatenum.md) que especifica como o **Recordset** deve ser convertido em uma sequência. Os parâmetros *RowDelimiter*, *ColumnDelimiter* e *NullExpr* são utilizados apenas com um *StringFormat* igual a **adClipString**.|
|*NumRows* |Opcional. O número de linhas a ser convertido no **Recordset**. Se *NumRows* não for especificado ou se for maior que o número total de linhas no **Recordset**, todas as linhas no **Recordset** serão convertidas.|
|*ColumnDelimiter* |Opcional. Um delimitador utilizado entre colunas, se especificado; caso contrário, o caractere TAB.|
|*ObjectDelimiter* |Opcional. Um delimitador utilizado entre linhas, se especificado; caso contrário, o caractere CARRIAGE RETURN.|
|*NullExpr* |Opcional. Uma expressão utilizada no lugar de um valor nulo, se especificada; caso contrário, a sequência vazia.|

## <a name="remarks"></a>Comentários

Dados brutos, mas sem dados de esquema, são salvos na sequência. Portanto, um **Recordset** não pode ser reaberto utilizando-se essa sequência.

Este método é equivalente ao método **GetClipString** do RDO.

