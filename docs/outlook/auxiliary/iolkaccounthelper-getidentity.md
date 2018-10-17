---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtém o nome de um perfil de conta.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400135"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Obtém o nome de um perfil de conta.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Parâmetros

_pwszIdentity_
  
> [in][out] O nome do perfil.
    
_pcch_
  
> [in] [out] Na chamada desse método, contém o tamanho (em número de caracteres) de _pwszIdentity_ que foi alocada. No retorno, contém o tamanho real, incluindo o caractere 0 de encerramento, do nome de perfil retornado. 
    
## <a name="return-values"></a>Valor de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_OUTOFMEMORY  <br/> |O nome de perfil retornado é maior do que _pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ é NULL.  <br/> |
   
## <a name="remarks"></a>Comentários

Se _pwszIdentity_ for muito pequeno para armazenar o nome de perfil, ele não será definido no retorno, e _pcch_ apontará para o tamanho obrigatório para _pwszIdentity_.
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

