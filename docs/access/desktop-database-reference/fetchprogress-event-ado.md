---
title: Evento FetchProgress (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293179"
---
# <a name="fetchprogress-event-ado"></a>Evento FetchProgress (ADO)

**Aplica-se ao:** Access 2013, Office 2013

O evento **FetchProgress** é chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas adicionais foram recuperadas, no momento, no [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Progress* |Um valor **Long** que indica o número de registros que foram atualmente recuperados pela operação de busca.|
|*MaxProgress* |Um valor **Long** que indica o número máximo de registros esperados para recuperação.|
|*adStatus* |Um valor de status [EventStatusEnum](eventstatusenum.md).|
|*pRecordset* |Um objeto **Recordset** que é aquele para o qual os registros estão sendo recuperados.|

## <a name="remarks"></a>Comentários

Ao utilizar o **FetchProgress** com um **Recordset** filho, esteja ciente de que os valores de parâmetro *Progress* e *MaxProgress* são derivados do [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset base. Os valores retornados representam o número total de registros no conjunto de linhas base, não apenas o número de registros no capítulo atual.

> [!NOTE]
> [!OBSERVAçãO] Para utilizar o **FetchProgress** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.


