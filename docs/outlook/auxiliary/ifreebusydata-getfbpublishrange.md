---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtém um intervalo de tempo predefinido para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765829"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Obtém um intervalo de tempo predefinido para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Par�metros

_prtmStart_
  
> [out] Um valor de tempo relativo para o início das informações de livre/ocupado. Esse valor é o número de minutos desde 1 de janeiro de 1601.
    
_prtmEnd_
  
> [out] Um valor de tempo relativo para o fim das informações de livre/ocupado. Esse valor é o número de minutos desde 1 de janeiro de 1601.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Um provedor de livre/ocupado chama [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) para definir o intervalo de tempo para uma enumeração. Se não tiver sido chamado [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , os valores padrão para **prtmStart** e **prtmEnd** devem ser definidos entre 1º de abril de 1601 00:00:00Z e 31 de agosto de 4500 11:59:59Z respectivamente. Além disso, você não deve definir a hora de início para ser maior do que a hora de término. 
  
**IFreeBusyData::GetFBPublishRange** deve retornar que os valores armazenados em cache para o intervalo de tempo definido pela chamada mais recente para **IFreeBusyData::EnumBlocks** ou **IFreeBusyData::SetFBRange**. 
  
## <a name="see-also"></a>Confira também

- [Use o tempo relativo para acessar dados do tipo disponível/ocupado](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

