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
# <a name="getrows-method-ado"></a>Método GetRows (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Recupera vários registros de um objeto [Recordset](recordset-object-ado.md) para dentro de uma matriz.

## <a name="syntax"></a>Sintaxe

*matriz* = *recordset*. GetRows (*linhas*, *Iniciar*, *campos* )

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna uma **Variant** cujo valor é uma matriz bidimensional.

## <a name="parameters"></a>Parâmetros

  - *Rows*

  - Opcional. Um valor [GetRowsOptionEnum](getrowsoptionenum.md) que indica o número de registros a serem recuperados. O padrão é **adGetRowsRest**.

  - *Start*

  - Opcional. Um valor **String** ou **Variant** que é avaliado para o indicador de um registro a partir do qual a operação **GetRows** deve começar. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).

  - *Fields*

  - Opcional. Uma **Variant** que representa um único nome de campo ou posição ordinal, ou uma matriz de nomes de campos ou números de posição ordinal. O ADO retorna apenas os dados nesses campos.

## <a name="remarks"></a>Comentários

Utilize o método **GetRows** para copiar registros de um **Recordset** para uma matriz bidimensional. O primeiro subscrito identifica o campo e o segundo identifica o número do registro. A *matriz* variável é automaticamente dimensionada até atingir o tamanho correto quando o método **GetRows** retorna os dados.

Se você não especificar um valor para o argumento de *linhas* , o método **GetRows** automaticamente recupera todos os registros no objeto **Recordset** . Se você solicitar mais registros do que os disponíveis, **GetRows** retornará apenas o número de registros disponíveis.

Se o objeto **Recordset** suporta indicadores, você pode especificar em qual registro método **GetRows** deve começar a recuperar dados passando o valor da propriedade de [indicador](bookmark-property-ado.md) do registro no argumento *Iniciar* .

Se você deseja restringir os campos que a chamada a **GetRows** retorna, você poderá passar um número/nome de campo único ou uma matriz de números/nomes de campo no argumento *Fields* .

Depois de chamar **GetRows**, o próximo registro não-lido tornar-se-a o registro atual, ou a propriedade [EOF](bof-eof-properties-ado.md) será definida como **True** se não houver mais registros.

