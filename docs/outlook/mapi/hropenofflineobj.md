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
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347744"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um objeto offline com base em um determinado perfil.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
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
  
> [in] Este parâmetro não é usado. Deve ser 0.
    
 _pwszProfileNameIn_
  
> no O nome do perfil para o qual o objeto offline é. Ele deve ser expresso em Unicode. 
    
 _pGUID_
  
> no Ponteiro para um GUID que pode ser usado para identificar exclusivamente este objeto de outros objetos offline. Deve ser **GUID_GlobalState**.
    
 _Enquanto_
  
> [in] Este parâmetro não é usado. Ele deve ser **nulo**.
    
 _ppOfflineObj_
  
> bota Um ponteiro para o objeto offline solicitado. O chamador pode usar esse ponteiro para acessar a interface [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) para localizar os retornos de chamada que esse objeto suporta e para configurar os retornos de chamada para ele. 
    
## <a name="return-values"></a>Valor de retorno

S_OK 
  
- A chamada de função foi bem-sucedida.
    
MAPI_E_NOT_FOUND
  
- A chamada de função falhou.
    
## <a name="remarks"></a>Comentários

Esta é a primeira chamada que um cliente faz quando o cliente deseja ser notificado de qualquer alteração de estado de conexão para um determinado perfil. Ao chamar **HrOpenOfflineObj**, o cliente obtém um objeto offline que oferece suporte a **IMAPIOfflineMgr**. O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto (usando [IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)) e, em seguida, configurar os retornos de chamada para ele (usando [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)).
  
Ao usar [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) para procurar o endereço dessa função em Msmapi32. dll, especifique **HrOpenOfflineObj @ 20** como o nome do procedimento. 
  
 O **HrOpenOfflineObj** só funciona para clientes que são provedores MAPI, suplementos de com e extensões de cliente do Exchange executando dentro do processo do Outlook. Caso contrário, **HrOpenOfflineObj** retornará **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>Confira também



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes de MAPI](mapi-constants.md)

