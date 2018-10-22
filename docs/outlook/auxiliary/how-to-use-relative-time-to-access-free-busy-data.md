---
title: Usar o tempo relativo para acessar dados de disponibilidade
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: A interface IFreeBusyData na API de Disponibilidade usa um conceito de tempo relativo, que é o número de minutos desde 1º de janeiro de 1601, que é expresso em Tempo Universal (UTC) e é um valor do tipo LONG.
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386933"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Usar o tempo relativo para acessar dados de disponibilidade

A interface [IFreeBusyData](ifreebusydata.md) na API de Disponibilidade usa um conceito de tempo relativo, que é o número de minutos desde 1º de janeiro de 1601, que é expresso em Tempo Universal (UTC) e é um valor do tipo **LONG**. 
  
Estes são alguns valores de tempo relativo usados com frequência:
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Use os valores de tempo relativo máximo e mínimo acima para verificar se os valores de tempo relativo são válidos.
  
Como o NTFS registra tempos de arquivo nativamente no formato [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx), pode ser útil usar o exemplo de código a seguir para converter o tempo relativo de e para **FILETIME**. 
  
```cpp
static const LONGLONG UnitsPerMinute = 600000000; 
static const LONGLONG UnitsPerHalfMinute = 300000000; 
void RTimeToFileTime(LONG rtime, FILETIME *pft) 
{ 
    Assert(pft != NULL); 
    ULARGE_INTEGER *puli = (ULARGE_INTEGER *)pft; 
    puli->QuadPart = rtime * UnitsPerMinute; 
} 
  
void FileTimeToRTime(FILETIME *pft, LONG* prtime) 
{ 
    Assert(pft != NULL); 
    Assert(prtime != NULL); 
 
    ULARGE_INTEGER uli = *(ULARGE_INTEGER *)pft; 
  
    uli.QuadPart += UnitsPerHalfMinute; 
    uli.QuadPart /= UnitsPerMinute; 
    *prtime = uli.LowPart; 
} 

```

## <a name="see-also"></a>Confira também

- [Sobre a API do serviço de disponibilidade](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

