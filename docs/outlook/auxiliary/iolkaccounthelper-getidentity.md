---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtém o nome do perfil de uma conta.
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765960"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Obtém o nome do perfil de uma conta.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Parâmetros

_pwszIdentity_
  
> [in] [out] O nome do perfil.
    
_pcch_
  
> [in] [out] Após chamar este método, contém o tamanho (em número de caracteres) da _pwszIdentity_ que foi alocado. Após retornar, contém o tamanho real, incluindo o caractere de terminação de 0, o nome do perfil retornado. 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_OUTOFMEMORY  <br/> |O nome do perfil retornado é maior que o tamanho da _pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ é nulo.  <br/> |
   
## <a name="remarks"></a>Comentários

Se _pwszIdentity_ for muito pequeno para conter o nome do perfil, ela não será definida no retorno e _pcch_ irá apontar para o tamanho necessário para _pwszIdentity_.
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)
- [PidTagProfileName](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

