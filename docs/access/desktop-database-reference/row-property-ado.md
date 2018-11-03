---
title: Linha de propriedade - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1882486de2a2dfe61b98d4461abeea9cbcc23363
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949310"
---
# <a name="row-property-ado"></a>Propriedade Row (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**. Quando você usa **colocar\_linha** para definir um objeto **Row** , uma linha seja transformada em um objeto **Record** do ADO. Leitura/gravação.

## <a name="syntax"></a>Sintaxe

Get HRESULT\_linha (\[check-out, retval\] IUnknown\* \* ppRow);

Colocar HRESULT\_linha (\[na\] IUnknown\* pRow);

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ppRow* |Ponteiro para um objeto **Row** do OLE DB.|
|*PRow* |Um objeto **Row** do OLE DB.|

## <a name="return-values"></a>Valor de retorno

Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.

## <a name="applies-to"></a>Aplica-se a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

