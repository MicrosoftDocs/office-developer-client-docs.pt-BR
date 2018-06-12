---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Cria um objeto que um cliente pode acessar em um formato de caracteres preferencial.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765811"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Cria um objeto que um cliente pode acessar em um formato de caracteres preferencial.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |Msmapi32  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
   
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

## <a name="parameters"></a>Par�metros

_pvUnwrapped_
  
> [in] O objeto do Outlook desfeito inicial. Deve implementar uma das seguintes interfaces:
    
   - [IMailUser: IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), ou [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Sinalizadores que caracterizam o objeto inicial desfeito. Deve ser um ou mais dos seguintes valores:
    
   - DDLWRAP_FLAG_ANSI — o objeto de Unwrapped é ANSI.
    
   - DDLWRAP_FLAG_UNICODE — o objeto de Unwrapped é UNICODE.
    
_ulWrappedFlags_
  
>  [in] Sinalizadores para o formato de caracteres preferencial. Deve ser um ou mais dos seguintes valores: 
    
   - DDLWRAP_FLAG_ANSI — objeto Wrapped será exposto como ANSI.
    
   - DDLWRAP_FLAG_UNICODE — objeto Wrapped será exposto como UNICODE.
    
_pIID_
  
>  [in] O identificador da interface suportado pelo objeto desfeito; Defina-la como NULL se isso for desconhecido. 
    
_pulReserved_
  
>  [in] Este parâmetro não é usado. Ela deve ser NULL. 
    
_fCheckWrap_
  
>  [in] Defina este parâmetro como **true** se _pvUnwrapped_ devem ser verificadas para seu formato de disposição; Defina-a **false** se o objeto deve ser quebrado sem verificação. 
    
_ppvWrapped_
  
>  [out] Um ponteiro para o objeto solicitado, quebrado automaticamente no formato de caractere solicitada. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Passagem em um objeto com quebra com _fCheckWrap_ definido como **true** resultará em um objeto desfeito. Independentemente de estarem ou não o objeto retornado é disposto, o cliente é responsável por liberando a referência de objeto retornado. 
  
Ao usar o **GetProcAddress** para procurar o endereço desta função no Msmapi32, especifique **HrCreateNewWrappedObject@28** como o nome do procedimento. 
  
## <a name="see-also"></a>Confira também

- [Sobre a camada de redução de dados API](about-the-data-degradation-layer-api.md)
- [Constantes (camada de dados degradação API)](constants-data-degradation-layer-api.md)

