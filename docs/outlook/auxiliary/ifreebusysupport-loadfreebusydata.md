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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411229"
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
  
> [in] O número de interfaces [IFreeBusyData](ifreebusydata.md) a retornar. 
    
_rgfbuser_
  
> [in] A matriz de usuários de livre/ocupado para recuperar dados.
    
_prgfbdata_
  
> [in] [out] A matriz de interfaces **IFreeBusyData** que correspondem à matriz _rgfbuser_ de [estruturas FBUser.](fbuser.md) 
    
   > [!NOTE]
   > Essa matriz de ponteiros é alocada pelo chamador e liberada pelo chamador. As interfaces reais apontadas são liberadas quando o chamador é feito com eles. 
  
_phrStatus_
  
> [out] A matriz de **resultados HRESULT** para recuperar cada interface **IFreeBusyData** correspondente. O valor pode ser NULL. Um resultado será definido como S_OK se  _prgfbdata correspondente_ for válido. 
    
_pcRead_
  
>  [out] O número real de usuários para os quais uma interface **IFreeBusyData** foi encontrada. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Constantes (API do serviço de disponibilidade)](constants-free-busy-api.md)

