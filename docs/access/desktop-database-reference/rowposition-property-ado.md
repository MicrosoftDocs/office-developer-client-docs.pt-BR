---
title: Propriedade RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306857"
---
# <a name="rowposition-property-ado"></a>Propriedade RowPosition (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Obtém ou define um objeto **RowPosition** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**. Quando você usa **colocar \_ RowPosition** para definir o objeto **RowPosition,** o objeto **Recordset** resultante usa o objeto **RowPosition** para determinar a linha atual.

Leitura/gravação.

## <a name="syntax"></a>Sintaxe

HRESULT get \_ RowPosition( \[ out, retval \] IUnknown \* \* ppRowPos);

HRESULT put \_ RowPosition( \[ in \] IUnknown \* pRowPos);

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ppRowPos* |Ponteiro para um objeto **RowPosition** do OLE DB.|
|*PRowPos* |Um objeto **RowPosition** do OLE DB.|

## <a name="return-values"></a>Valor de retorno

Esse método de propriedade retorna os valores HRESULT padrão, incluindo S \_ OK e E \_ FAIL.

## <a name="remarks"></a>Comentários

Quando esta propriedade for definida, se o objeto  **Rowset** no objeto **RowPosition** for diferente do objeto **Rowset** no objeto **Recordset**, o primeiro substituirá o segundo. O mesmo comportamento também se aplicará ao **Charter** atual do **RowPosition**.

## <a name="applies-to"></a>Aplicável a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

