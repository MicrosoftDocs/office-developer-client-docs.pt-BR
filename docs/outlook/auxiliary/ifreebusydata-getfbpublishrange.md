---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtém um intervalo de tempo pré-definido para uma enumeração de blocos de disponibilidade de dados de um usuário.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317525"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Obtém um intervalo de tempo pré-definido para uma enumeração de blocos de disponibilidade de dados de um usuário.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Parâmetros

_prtmStart_
  
> bota Um valor de tempo relativo para o início das informações de disponibilidade. Este valor é o número de minutos desde 1º de janeiro de 1601.
    
_prtmEnd_
  
> bota Um valor de tempo relativo para o final das informações de disponibilidade. Este valor é o número de minutos desde 1º de janeiro de 1601.
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Um provedor de disponibilidade chama [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) para definir o intervalo de tempo para uma enumeração. Se [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) não tiver sido chamado, os valores padrão para **prtmStart** e **PrtmEnd** deverão ser definidos entre 1º de abril de 1601 00:00: e 31 de agosto de 4500 11:59-00Z respectivamente. Além disso, você não deve definir a hora de início como maior do que a hora de término. 
  
**IFreeBusyData:: GetFBPublishRange** deve retornar os valores em cache para o intervalo de tempo definido pela chamada mais recente de **IFreeBusyData:: EnumBlocks** ou **IFreeBusyData:: SetFBRange**. 
  
## <a name="see-also"></a>Confira também

- [Usar o tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

