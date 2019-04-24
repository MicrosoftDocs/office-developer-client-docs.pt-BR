---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: É uma interface que enumera blocos de disponibilidade de dados de um usuário em um intervalo de tempo específico.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317553"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

É uma interface que enumera blocos de disponibilidade de dados de um usuário em um intervalo de tempo específico.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parâmetros

_ppenumfb_
  
> [out] Uma interface para enumerar blocos de disponibilidade.
    
_ftmStart_
  
> [in] A hora de início da enumeração. É expressa em [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [in] A hora de término da enumeração. É expressa em **FILETIME**. 
    
## <a name="return-values"></a>Valor de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Esse método é usado para indicar o intervalo de tempo de itens de calendário para os quais recuperar detalhes. Os valores de *ftmStart* e *ftmEnd* são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Um provedor de disponibilidade posteriormente também pode usar a interface [IEnumFBBlock](ienumfbblock.md) retornada para acessar a enumeração. 
  
## <a name="see-also"></a>Confira também

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Usar o tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md)

