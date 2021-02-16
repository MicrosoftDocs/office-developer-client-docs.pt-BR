---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417004"
---
# <a name="imapiformfactorygetlasterror"></a>IMAPIFormFactory::GetLastError

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior ocorrendo no objeto de fábrica de formulário. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] Um tipo de dados HRESULT que contém o valor de erro gerado na chamada do método anterior.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada. O sinalizador a seguir pode ser definido: 
    
MAPI_UNICODE 
  
> As cadeias de caracteres na **estrutura MAPIERROR** retornadas no parâmetro  _lppMAPIError_ estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada que contém informações de versão, componente e contexto para o erro. Esse parâmetro pode ser definido como NULL se não houver **estrutura MAPIERROR** a ser retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e **GetLastError** não dá suporte a Unicode ou MAPI_UNICODE não foi definido e **GetLastError** dá suporte apenas a Unicode. 
    
## <a name="remarks"></a>Comentários

O **método IMAPIFormFactory::GetLastError** fornece informações sobre uma chamada de método anterior que falhou. Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da **estrutura MAPIERROR** em uma caixa de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar a estrutura **MAPIERROR** apontada pelo parâmetro  _lppMAPIError_ se MAPI fornece um somente se **GetLastError** retornar S_OK. Às vezes, o MAPI não pode determinar qual foi o último erro ou não tem mais nada a relatar sobre o erro. Nessa situação, um ponteiro para NULL é retornado em _lppMAPIError._ 
  
Para obter mais informações sobre **o método GetLastError,** consulte [Usando erros estendidos.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Confira também



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

