---
title: Use o tempo relativo para acessar dados do tipo disponível/ocupado
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: A interface de IFreeBusyData na API Free/Busy usa um conceito de tempo relativo, que é o número de minutos desde 1 de janeiro de 1601, expressado em UTC (Tempo Universal), e é um valor do tipo LONG.
ms.openlocfilehash: b83cd46cfcc4d84d4fc3bf000dd8b0acdda545dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765815"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Use o tempo relativo para acessar dados do tipo disponível/ocupado

A interface de [IFreeBusyData](ifreebusydata.md) na API Free/Busy usa um conceito de tempo relativo, que é o número de minutos desde 1 de janeiro de 1601, expressado em UTC (Tempo Universal) e é um valor de tipo **LONG**. 
  
Estes são alguns valores de tempo relativo comumente usadas:
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Use os valores máximo e mínimo de tempo relativo anterior para ajudar a verificar se os seus valores de tempo relativo são válidos.
  
Porque NTFS registra os tempos de arquivo nativamente no formato [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , talvez seja conveniente usar o exemplo de código a seguir para converter o tempo relativo de e **FILETIME**. 
  
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

