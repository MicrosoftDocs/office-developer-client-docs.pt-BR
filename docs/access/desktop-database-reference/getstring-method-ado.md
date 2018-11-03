---
title: Método GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b4926b3568d6c7289ca9d3158a8723e016ed344
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949668"
---
# <a name="getstring-method-ado"></a>Método GetString (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Retorna o [Recordset](recordset-object-ado.md) como uma sequência.

## <a name="syntax"></a>Sintaxe

*Variant* = *recordset*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Valor de retorno

Retorna o **Recordset** como uma **Variant** avaliada como sequência (BSTR).

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*StringFormat* |Um valor [StringFormatEnum](stringformatenum.md) que especifica como o **Recordset** deve ser convertido em uma sequência. Os parâmetros *RowDelimiter*, *ColumnDelimiter* e *NullExpr* são utilizados apenas com um *StringFormat* igual a **adClipString**.|
|*NumRows* |Opcional. O número de linhas a ser convertido no **Recordset**. Se *NumRows* não for especificado, ou se ele for maior que o número total de linhas no **conjunto de registros**, todas as linhas no **conjunto de registros** são convertidas.|
|*ColumnDelimiter* |Opcional. Um delimitador utilizado entre colunas, se especificado; caso contrário, o caractere TAB.|
|*RowDelimiter* |Opcional. Um delimitador utilizado entre linhas, se especificado; caso contrário, o caractere CARRIAGE RETURN.|
|*NullExpr* |Opcional. Uma expressão utilizada no lugar de um valor nulo, se especificada; caso contrário, a sequência vazia.|

## <a name="remarks"></a>Comentários

Dados brutos, mas sem dados de esquema, são salvos na sequência. Portanto, um **Recordset** não pode ser reaberto utilizando-se essa sequência.

Este método é equivalente ao método **GetClipString** do RDO.

