---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cc71974d841005785932cc9017d44c3c0614687d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563384"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um objeto offline com base em um determinado perfil.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |Msmapi32  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a>Parâmetros

 _ulReserved_
  
> [in] Este parâmetro não é usado. Ela deve ser 0.
    
 _pwszProfileNameIn_
  
> [in] O nome do perfil que o objeto offline se destina. Ele deve ser expresso em Unicode. 
    
 _pGUID_
  
> [in] Ponteiro para um GUID que pode ser usado para identificar exclusivamente esse objeto dentre outros objetos offline. Ela deve ser **GUID_GlobalState**.
    
 _Preservadas_
  
> [in] Este parâmetro não é usado. Ela deve ser **nula**.
    
 _ppOfflineObj_
  
> [out] Um ponteiro para o objeto offline solicitado. O chamador pode usar esse ponteiro para acessar o [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) interface para encontrar os retornos de chamada que ofereça suporte a esse objeto e para configurar os retornos de chamada para ele. 
    
## <a name="return-values"></a>Valores de retorno

S_OK 
  
- A chamada de função é bem-sucedida.
    
E_NOT_FOUND
  
- Falha da chamada de função.
    
## <a name="remarks"></a>Comentários

Esta é a primeira chamada que faz com que um cliente quando o cliente deseja ser notificado sobre qualquer alteração de estado de conexão para um determinado perfil. Após chamar **HrOpenOfflineObj**, o cliente obtém um objeto offline que suporta **IMAPIOfflineMgr**. O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto (usando [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) e, em seguida, configurar retornos de chamada para ele (usando [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).
  
Ao usar o [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) para procurar o endereço desta função no Msmapi32, especifique **HrOpenOfflineObj@20** como o nome do procedimento. 
  
 **HrOpenOfflineObj** funciona apenas para clientes que estão provedores MAPI, suplementos COM e extensões de cliente do Exchange em execução dentro do processo do Outlook. Caso contrário, **HrOpenOfflineObj** retornará **E_NOT_FOUND**. 
  
## <a name="see-also"></a>Confira também



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

