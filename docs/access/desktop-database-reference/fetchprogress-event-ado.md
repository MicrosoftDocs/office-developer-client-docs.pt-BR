---
title: Evento FetchProgress (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d062f4ae7008df787394eeb9253b65d6f5d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886190"
---
# <a name="fetchprogress-event-ado"></a>Evento FetchProgress (ADO)


**Aplica-se a**: Access 2013, o Office 2013


O evento **FetchProgress** é chamado periodicamente durante uma operação assíncrona demorada para relatar quantas linhas adicionais foram recuperadas, no momento, no [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

De*progresso*, *MaxProgress*, de FetchProgress *adStatus*, *pRecordset*

## <a name="parameters"></a>Parâmetros

  - *Progress*

  - Um valor **Long** que indica o número de registros que foram atualmente recuperados pela operação de busca.

  - *MaxProgress*

  - Um valor **Long** que indica o número máximo de registros esperados para recuperação.

  - *adStatus*

  - Um valor de status [EventStatusEnum](eventstatusenum.md).

  - *pRecordset*

  - Um objeto **Recordset** que é aquele para o qual os registros estão sendo recuperados.

## <a name="remarks"></a>Comentários

Ao utilizar o **FetchProgress** com um **Recordset**filho, lembre-se de que os valores de parâmetro de *progresso* e *MaxProgress* são derivados do conjunto de linhas subjacente do [Serviço de Cursor](microsoft-cursor-service-for-ole-db-ado-service-component.md) . Os valores retornados representam o número total de registros no conjunto de linhas base, não apenas o número de registros no capítulo atual.


> [!NOTE]
> [!OBSERVAçãO] Para utilizar o **FetchProgress** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.


