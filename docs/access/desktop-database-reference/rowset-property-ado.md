---
title: Propriedade Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306738"
---
# <a name="rowset-property-ado"></a>Propriedade Rowset (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**. Quando você usa o\_conjunto de linhas, o conjunto de linhas é transformado em um objeto **Recordset** do ADO.

Leitura/gravação.

## <a name="syntax"></a>Sintaxe

HRESULT get\_Rowset (\[out, retval\] IUnknown\* \* ppRowset);

HRESULT colocar\_Rowset (\[em\] IUnknown\* pRowset);

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ppRowset* |Ponteiro para um objeto **Rowset** do OLE DB.|
|*PRowset* |Um objeto **Rowset** do OLE DB.|

## <a name="return-values"></a>Valor de retorno

Este método de propriedade retorna os valores HRESULT padrão, incluindo\_S OK E\_o e falha.

## <a name="applies-to"></a>Aplicável a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

