---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414715"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Informa ao conector de cluster que um cálculo do Excel foi cancelado e, portanto, todas as chamadas de função pendentes nessa sessão também podem ser canceladas (e que o Excel não espera retornos de chamada com seus resultados).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parâmetros

_SessionID_
  
> A ID da sessão usada pelo cálculo cancelado. Esse valor corresponde ao valor retornado por [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor de retorno

**xlHpcRetSuccess** se o  _argumento SessionId_ for válido; **xlHpcRetInvalidSessionId** se o  _argumento SessionId_ for inválido; **xlHpcRetCallFailed** em outras falhas. 
  
## <a name="remarks"></a>Comentários

Os implementadores devem interromper todos os processos da sessão para melhorar o desempenho, pois os resultados recebidos após essa chamada serão descartados pelo Excel.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

