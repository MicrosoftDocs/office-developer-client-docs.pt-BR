---
title: Propriedade RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869068"
---
# <a name="rowposition-property-ado"></a>Propriedade RowPosition (ADO)


**Aplica-se a**: Access 2013, o Office 2013



Obtém ou define um objeto **RowPosition** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**. Quando você usa **colocar\_RowPosition** para definir o objeto **RowPosition** , o objeto **Recordset** resultante usa o objeto **RowPosition** para determinar a linha atual.

Leitura/gravação.

## <a name="syntax"></a>Sintaxe

Get HRESULT\_RowPosition (\[check-out, retval\] IUnknown\* \* ppRowPos);

Colocar HRESULT\_RowPosition (\[na\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parâmetros

  - *ppRowPos*

  - Ponteiro para um objeto **RowPosition** do OLE DB.

  - *PRowPos*

  - Um objeto **RowPosition** do OLE DB.

## <a name="return-values"></a>Valor de retorno

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="remarks"></a>Comentários

Quando esta propriedade for definida, se o objeto **Rowset** no objeto **RowPosition** for diferente do objeto **Rowset** no objeto **Recordset**, o primeiro substituirá o segundo. O mesmo comportamento também se aplicará ao **Charter** atual do **RowPosition**.

## <a name="applies-to"></a>Aplica-se a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

