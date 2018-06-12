---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765257"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Informa o conector de cluster que um cálculo do Excel foi cancelado e, portanto, todos os pendentes chamadas de função dentro dessa sessão poderão ser cancelados também (e que o Excel não espera retornos de chamada por seus resultados).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Par�metros

_SessionID_
  
> A identificação da sessão usada pelo cálculo cancelado. Esse valor compara o valor retornado pela [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor retornado

**xlHpcRetSuccess** se o argumento _SessionId_ é válido. **xlHpcRetInvalidSessionId** se o argumento _SessionId_ é inválido; **xlHpcRetCallFailed** em outras falhas. 
  
## <a name="remarks"></a>Coment�rios

Implementadores devem parar todos os processos para a sessão para melhorar o desempenho, como o retorno de algum resultado recebido após essa chamada será descartada pelo Excel.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de Cluster do Excel](excel-cluster-connector-functions.md)

