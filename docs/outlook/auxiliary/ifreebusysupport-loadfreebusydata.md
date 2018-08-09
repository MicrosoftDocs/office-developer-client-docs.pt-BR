---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Retorna, para cada usuário especificado, uma interface para enumerar os blocos de informações de disponibilidade de dados dentro de um intervalo de tempo.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765832"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Retorna, para cada usuário especificado, uma interface para enumerar os blocos de informações de disponibilidade de dados dentro de um intervalo de tempo. 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Parâmetros

_cMax_
  
> [in] O número de interfaces de [IFreeBusyData](ifreebusydata.md) para retornar. 
    
_rgfbuser_
  
> [in] A matriz de usuários de livre/ocupado para recuperar dados para.
    
_prgfbdata_
  
> [in] [out] A matriz de interfaces de **IFreeBusyData** que correspondem à matriz _rgfbuser_ de estruturas de [FBUser](fbuser.md) . 
    
   > [!NOTE]
   > Essa matriz de ponteiros é alocada pelo chamador e liberada pelo chamador. As interfaces reais apontadas para sejam liberadas quando o chamador é feito com eles. 
  
_phrStatus_
  
> [out] A matriz de resultados **HRESULT** para recuperação de cada interface **IFreeBusyData** correspondente. O valor pode ser NULL. Um resultado é definido como S_OK se correspondente _prgfbdata_ é válida. 
    
_pcRead_
  
>  [out] O número real de usuários para o qual uma interface **IFreeBusyData** foi encontrada. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Constantes (API de livre/ocupado)](constants-free-busy-api.md)

