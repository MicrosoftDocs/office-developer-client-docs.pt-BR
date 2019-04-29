---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425873"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de repositório de mensagens. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _And_
  
> no Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior para o objeto do repositório de mensagens.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _lppMAPIError_
  
> bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém a versão, o componente e informações de contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhum **MAPIERROR** a ser retornado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
## <a name="remarks"></a>Comentários

Use o método **IMSLogon:: GetLastError** para recuperar informações a serem exibidas em uma mensagem para o usuário sobre o último erro retornado de uma chamada de método para o objeto do repositório de mensagens. 
  
Para liberar todas as memórias alocadas por MAPI para a estrutura **MAPIERROR** retornada, os aplicativos clientes precisam chamar somente a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
O valor de retorno **** de GetLastError deve ser S_OK para que um aplicativo use o **MAPIERROR**. Mesmo que o valor de retorno seja S_OK, um **MAPIERROR** pode não ser retornado. Se a implementação não puder determinar o último erro, ou se um **MAPIERROR** não estiver disponível para esse erro, GetLastError retornará um ponteiro para NULL em _lppMAPIError_ em vez disso. **** 
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

