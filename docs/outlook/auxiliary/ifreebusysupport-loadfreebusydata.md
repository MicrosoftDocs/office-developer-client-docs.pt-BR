---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Retorna, para cada usuário específico, uma interface para enumerar blocos de disponibilidade de dados em um intervalo de tempo.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319401"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Retorna, para cada usuário específico, uma interface para enumerar blocos de disponibilidade de dados em um intervalo de tempo. 
  
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
  
> no O número de interfaces [IFreeBusyData](ifreebusydata.md) a serem retornadas. 
    
_rgfbuser_
  
> no A matriz de usuários de disponibilidade para os quais recuperar dados.
    
_prgfbdata_
  
> no bota A matriz de interfaces **IFreeBusyData** que correspondem à matriz _Rgfbuser_ de estruturas [FBUser](fbuser.md) . 
    
   > [!NOTE]
   > Essa matriz de ponteiros é alocada pelo chamador e liberada pelo chamador. As interfaces reais apontadas são lançadas quando o chamador é feito com elas. 
  
_phrStatus_
  
> bota A matriz de resultados **HRESULT** para recuperar cada interface **IFreeBusyData** correspondente. O valor pode ser nulo. Um resultado é definido como S_OK se _prgfbdata_ correspondente for válido. 
    
_pcRead_
  
>  bota O número real de usuários para os quais uma interface **IFreeBusyData** foi encontrada. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Constantes (API do serviço de disponibilidade)](constants-free-busy-api.md)

