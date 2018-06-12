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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767559"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de repositório de mensagem. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Par�metros

 _hResult_
  
> [in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior para o objeto de repositório de mensagem.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres na estrutura **MAPIERROR** retornado no parâmetro _lppMAPIError_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado que contém informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhum **MAPIERROR** para retornar. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="remarks"></a>Coment�rios

Use o método **IMSLogon::GetLastError** para recuperar informações a serem exibidas em uma mensagem ao usuário sobre o último erro retornado de uma chamada de método do objeto de repositório de mensagem. 
  
Para liberar toda a memória alocada pelo MAPI para a estrutura **MAPIERROR** retornada, aplicativos cliente precisará chamar apenas a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
O valor de retorno de **GetLastError** deve ser S_OK para um aplicativo para usar o **MAPIERROR**. Mesmo se o valor de retorno é S_OK, um **MAPIERROR** não pode ser retornado. Se a implementação não puder determinar qual foi o último erro, ou se um **MAPIERROR** não está disponível para que o erro, **GetLastError** retorna um ponteiro como NULL em _lppMAPIError_ em vez disso. 
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon: IUnknown](imslogoniunknown.md)

