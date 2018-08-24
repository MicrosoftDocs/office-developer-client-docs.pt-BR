---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580695"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma lista ordenada de identificadores de entrada dos contêineres a serem incluídos no processo de resolução de nome iniciado pelo método [IAddrBook::ResolveName](iaddrbook-resolvename.md) . 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornada no caminho de pesquisa. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppSearchPath_
  
> [out] Um ponteiro para um ponteiro para uma lista ordenada de identificadores de entrada do contêiner. **GetSearchPath** armazena a lista ordenada em uma estrutura [SRowSet](srowset.md) . Se não houver nenhuma contêineres na hierarquia de catálogo de endereços, será retornado zero na estrutura **SRowSet** . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O caminho de pesquisa foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Provedores de serviços e clientes chame o método de **GetSearchPath** para obter o caminho de pesquisa que é usado para resolver nomes com o método **ResolveName** . Normalmente, os clientes chame o método de [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) para estabelecer um caminho de pesquisa do contêiner no perfil antes de que ligarem **GetSearchPath** para recuperá-la. No entanto, chamar **SetSearchPath** é opcional. 
  
Se **SetSearchPath** nunca tiver sido chamado, o **GetSearchPath** cria um caminho ao trabalho por meio do endereço tabelas de hierarquias do livro. O caminho de pesquisa padrão estabelecido pelo **GetSearchPath** consiste nos seguintes contêineres na seguinte ordem: 
  
1. O primeiro recipiente com permissão de leitura/gravação, normalmente o catálogo de endereços pessoal (PAB).
    
2. Cada contêiner que tem sua propriedade **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) definida como DT_GLOBAL. Essa configuração indica que o contêiner retém os destinatários. 
    
3. O contêiner designado como padrão, se não houver nenhuma contêineres que têm o sinalizador DT_GLOBAL definido em sua propriedade **PR_DISPLAY_TYPE** e o contêiner padrão difere do contêiner primeiro com permissão de leitura/gravação. 
    
Se tiver sido chamado **SetSearchPath** , **GetSearchPath** constrói um caminho usando os contêineres do catálogo de endereços que tiverem sido armazenados no perfil. **GetSearchPath** valida esse caminho antes de ele os retorna ao chamador. 
  
Após a primeira chamada para **SetSearchPath**, as chamadas subsequentes **SetSearchPath** devem ser usadas para modificar o caminho de pesquisa retornado por **GetSearchPath**. Em outras palavras, o cliente de chamada ou o provedor não recebe o caminho de pesquisa padrão após a primeira chamada para **SetSearchPath**.
  
## <a name="see-also"></a>Confira também



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

