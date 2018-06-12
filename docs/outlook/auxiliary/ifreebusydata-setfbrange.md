---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Define o intervalo de tempo para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765847"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Define o intervalo de tempo para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Par�metros

_rtmStart_
  
> [in] Um valor de tempo relativo para o início das informações de livre/ocupado. Esse valor é o número de minutos desde 1 de janeiro de 1601.
    
_rtmEnd_
  
> [in] Um valor de tempo relativo para o fim das informações de livre/ocupado. Esse valor é o número de minutos desde 1 de janeiro de 1601.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Este método é usado para indicar o intervalo de tempo de itens de calendário para o qual recuperar detalhes. Os valores de *ftmStart* e *ftmEnd* são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>Confira também

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Use o tempo relativo para acessar dados do tipo disponível/ocupado](how-to-use-relative-time-to-access-free-busy-data.md)

