---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtém uma interface que enumera blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo especificado.
ms.openlocfilehash: ab377b1029296b6b4bac68d7169dcf7b8dcd8b87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765834"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Obtém uma interface que enumera blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo especificado.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Par�metros

_ppenumfb_
  
> [out] Uma interface para enumerar os blocos de livre/ocupado.
    
_ftmStart_
  
> [in] A hora de início para a enumeração. Ele é expresso em [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [in] A hora de término para a enumeração. Ele é expresso em **FILETIME**. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Este método é usado para indicar o intervalo de tempo de itens de calendário para o qual recuperar detalhes. Os valores de *ftmStart* e *ftmEnd* são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Um provedor de livre/ocupado também subsequentemente pode usar a interface de [IEnumFBBlock](ienumfbblock.md) retornada para acessar a enumeração. 
  
## <a name="see-also"></a>Confira também

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Use o tempo relativo para acessar dados do tipo disponível/ocupado](how-to-use-relative-time-to-access-free-busy-data.md)

