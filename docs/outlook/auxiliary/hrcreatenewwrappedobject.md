---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Cria um objeto que um cliente pode acessar em um formato de caractere preferido.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384189"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Cria um objeto que um cliente pode acessar em um formato de caractere preferido.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a>Parâmetros

_pvUnwrapped_
  
> [in] O objeto inicial não ajustado do Outlook. Deve implementar uma das seguintes interfaces:
    
   - [IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx) ou [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Sinalizadores que caracterizam o objeto inicial não ajustado. Deve ser um ou mais dos seguintes valores:
    
   - DDLWRAP_FLAG_ANSI — O objeto não ajustado é ANSI.
    
   - DDLWRAP_FLAG_UNICODE — O objeto não ajustado é UNICODE.
    
_ulWrappedFlags_
  
>  [in] Sinalizadores para o formato de caractere preferido. Deve ser um ou mais dos seguintes valores: 
    
   - DDLWRAP_FLAG_ANSI – O objeto ajustado será exposto como ANSI.
    
   - DDLWRAP_FLAG_UNICODE– O objeto ajustado será exposto como UNICODE.
    
_pIID_
  
>  [in] O identificador da interface com suporte pelo objeto não ajustado; defina como NULL se for desconhecido. 
    
_pulReserved_
  
>  [in] Este parâmetro não é usado. Ele deve ser NULL. 
    
_fCheckWrap_
  
>  [in] Defina este parâmetro como **true** se _pvUnwrapped_ deve ser verificado em relação a seu formato antes do ajuste; configure-o como **false** se o objeto deve ser ajustado sem verificação. 
    
_ppvWrapped_
  
>  [out] Um apontador para o objeto solicitado, ajustado no formato de caractere solicitado. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Passar um objeto ajustado com _fCheckWrap_ definido como **true** resultará em um objeto não ajustado. Independentemente de o objeto estar ajustado ou não, o cliente é responsável por liberar a referência no objeto retornado. 
  
Ao usar **GetProcAddress** para procurar o endereço dessa função em msmapi32.dll, especifique **HrCreateNewWrappedObject@28** como o nome do procedimento. 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de camada de degradação de dados](about-the-data-degradation-layer-api.md)
- [Constantes (API de camada de degradação de dados)](constants-data-degradation-layer-api.md)

