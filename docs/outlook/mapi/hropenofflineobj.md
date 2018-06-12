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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ac6584819b5dfa96a5f7816f1d77b89323e3eaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766824"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

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
    
## <a name="remarks"></a>Coment�rios

Esta é a primeira chamada que faz com que um cliente quando o cliente deseja ser notificado sobre qualquer alteração de estado de conexão para um determinado perfil. Após chamar **HrOpenOfflineObj**, o cliente obtém um objeto offline que suporta **IMAPIOfflineMgr**. O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto (usando [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) e, em seguida, configurar retornos de chamada para ele (usando [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).
  
Ao usar o [GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx) para procurar o endereço desta função no Msmapi32, especifique **HrOpenOfflineObj@20** como o nome do procedimento. 
  
 **HrOpenOfflineObj** funciona apenas para clientes que estão provedores MAPI, suplementos COM e extensões de cliente do Exchange em execução dentro do processo do Outlook. Caso contrário, **HrOpenOfflineObj** retornará **E_NOT_FOUND**. 
  
## <a name="see-also"></a>Confira também



[IMAPIOffline: IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)


[Sobre a API de estado Offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)

