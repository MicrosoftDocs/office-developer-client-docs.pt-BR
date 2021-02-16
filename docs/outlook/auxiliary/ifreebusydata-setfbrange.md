---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Define o intervalo de tempo para uma enumeração de blocos de disponibilidade de dados de um usuário.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421659"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Define o intervalo de tempo para uma enumeração de blocos de disponibilidade de dados de um usuário.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parâmetros

_rtmStart_
  
> [in] Um valor de tempo relativo para o início das informações de livre/ocupado. Esse valor é o número de minutos desde 1º de janeiro de 1601.
    
_rtmEnd_
  
> [in] Um valor de tempo relativo para o final das informações de livre/ocupado. Esse valor é o número de minutos desde 1º de janeiro de 1601.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Esse método é usado para indicar o intervalo de tempo de itens de calendário para os quais recuperar detalhes. Os valores de  *ftmStart*  e  *ftmEnd*  são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>Confira também

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Usar o tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md)

