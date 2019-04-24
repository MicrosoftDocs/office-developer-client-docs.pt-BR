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
# <a name="getrows-method-ado"></a>Método getRows (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Recupera vários registros de um objeto [Recordset](recordset-object-ado.md) para dentro de uma matriz.

## <a name="syntax"></a>Sintaxe

** = *conjunto de registros*de matriz. GetRows (*linhas*, *início*, *campos* )

## <a name="return-value"></a>Valor de retorno

Retorna uma **Variant** cujo valor é uma matriz bidimensional.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Rows* |Opcional. Um valor [GetRowsOptionEnum](getrowsoptionenum.md) que indica o número de registros a serem recuperados. O padrão é **adGetRowsRest**.|
|*Start* |Opcional. Um valor **String** ou **Variant** que é avaliado para o indicador de um registro a partir do qual a operação **GetRows** deve começar. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).|
|*Fields* |Opcional. Uma **Variant** que representa um único nome de campo ou posição ordinal, ou uma matriz de nomes de campos ou números de posição ordinal. O ADO retorna apenas os dados nesses campos.|

## <a name="remarks"></a>Comentários

Utilize o método **GetRows** para copiar registros de um **Recordset** para uma matriz bidimensional. O primeiro subscrito identifica o campo e o segundo identifica o número do registro. A variável *array* é dimensionada automaticamente para o tamanho correto quando o método **GetRows** retorna os dados.

Se você não especificar um valor para o argumento *Rows*, o método **GetRows** recupera automaticamente todos os registros no objeto **Recordset**. Se você solicitar mais registros do que os disponíveis, **GetRows** retornará apenas o número de registros disponíveis.

Se o objeto **Recordset** suportar indicadores, será possível especificar em qual registro o método **GetRows** deve começar a recuperar dados, passando-se o valor da propriedade [Bookmark](bookmark-property-ado.md) desse registro no argumento *Start*.

Se você deseja restringir os campos que a chamada a **GetRows** retorna, poderá passar um único número/nome de campo ou uma matriz de números/nomes de campo no argumento *Fields*.

Depois de chamar **GetRows**, o próximo registro não-lido tornar-se-a o registro atual, ou a propriedade [EOF](bof-eof-properties-ado.md) será definida como **True** se não houver mais registros.

