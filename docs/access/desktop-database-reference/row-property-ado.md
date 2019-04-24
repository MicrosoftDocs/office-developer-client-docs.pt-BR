---
title: Propriedade Row-ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306479"
---
# <a name="row-property-ado"></a>Propriedade Row (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**. Quando você usa **colocar\_linha** para definir um objeto **Row** , uma linha é TransformaDA em um objeto **Record** do ADO. Leitura/gravação.

## <a name="syntax"></a>Sintaxe

HRESULT obter\_linha (\[out, retval\] IUnknown\* \* ppRow);

Linha HRESULT\_put (\[em\] IUnknown\* Prow);

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ppRow* |Ponteiro para um objeto **Row** do OLE DB.|
|*PRow* |Um objeto **Row** do OLE DB.|

## <a name="return-values"></a>Valor de retorno

Este método de propriedade retorna os valores HRESULT padrão, incluindo\_S OK E\_o e falha.

## <a name="applies-to"></a>Aplicável a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

