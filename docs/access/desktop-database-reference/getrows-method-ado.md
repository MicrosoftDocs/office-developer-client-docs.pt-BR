---
title: Método GetRows (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 853f971f68bb0ec4069ba58e04b7cf9d231c6467
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949856"
---
# <a name="getrows-method-ado"></a>Método GetRows (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Recupera vários registros de um objeto [Recordset](recordset-object-ado.md) para dentro de uma matriz.

## <a name="syntax"></a>Sintaxe

*matriz* = *recordset*. GetRows (*linhas*, *Iniciar*, *campos* )

## <a name="return-value"></a>Valor de retorno

Retorna uma **Variant** cujo valor é uma matriz bidimensional.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Rows* |Opcional. Um valor [GetRowsOptionEnum](getrowsoptionenum.md) que indica o número de registros a serem recuperados. O padrão é **adGetRowsRest**.|
|*Start* |Opcional. Um valor **String** ou **Variant** que é avaliado para o indicador de um registro a partir do qual a operação **GetRows** deve começar. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).|
|*Fields* |Opcional. Uma **Variant** que representa um único nome de campo ou posição ordinal, ou uma matriz de nomes de campos ou números de posição ordinal. O ADO retorna apenas os dados nesses campos.|

## <a name="remarks"></a>Comentários

Utilize o método **GetRows** para copiar registros de um **Recordset** para uma matriz bidimensional. O primeiro subscrito identifica o campo e o segundo identifica o número do registro. A *matriz* variável é automaticamente dimensionada até atingir o tamanho correto quando o método **GetRows** retorna os dados.

Se você não especificar um valor para o argumento de *linhas* , o método **GetRows** automaticamente recupera todos os registros no objeto **Recordset** . Se você solicitar mais registros do que os disponíveis, **GetRows** retornará apenas o número de registros disponíveis.

Se o objeto **Recordset** suporta indicadores, você pode especificar em qual registro método **GetRows** deve começar a recuperar dados passando o valor da propriedade de [indicador](bookmark-property-ado.md) do registro no argumento *Iniciar* .

Se você deseja restringir os campos que a chamada a **GetRows** retorna, você poderá passar um número/nome de campo único ou uma matriz de números/nomes de campo no argumento *Fields* .

Depois de chamar **GetRows**, o próximo registro não-lido tornar-se-a o registro atual, ou a propriedade [EOF](bof-eof-properties-ado.md) será definida como **True** se não houver mais registros.

