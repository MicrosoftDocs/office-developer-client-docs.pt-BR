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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412979"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma lista ordenada de identificadores de entrada dos contêineres a serem incluídos no processo de resolução de nomes iniciado pelo método [IAddrBook::ResolveName.](iaddrbook-resolvename.md) 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o tipo das cadeias de caracteres retornadas no caminho de pesquisa. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppSearchPath_
  
> [out] Um ponteiro para um ponteiro para uma lista ordenada de identificadores de entrada de contêiner. **GetSearchPath** armazena a lista ordenada em uma [estrutura SRowSet.](srowset.md) Se não houver contêineres na hierarquia do address book, zero será retornado na **estrutura SRowSet.** 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O caminho de pesquisa foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes e provedores de serviços chamam o **método GetSearchPath** para obter o caminho de pesquisa usado para resolver nomes com o **método ResolveName.** Normalmente, os clientes chamam o método [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) para estabelecer um caminho de pesquisa de contêiner no perfil antes de **chamarEm GetSearchPath** para recuperá-lo. No entanto, **chamar SetSearchPath** é opcional. 
  
Se **SetSearchPath** nunca tiver sido chamado, **GetSearchPath** criará um caminho trabalhando nas tabelas de hierarquia do livro de endereços. O caminho de pesquisa padrão estabelecido **pelo GetSearchPath** consiste nos seguintes contêineres na seguinte ordem: 
  
1. O primeiro contêiner com permissão de leitura/gravação, geralmente o pab (lista de endereços pessoal).
    
2. Cada contêiner que tem sua **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) definida como DT_GLOBAL. Essa configuração indica que o contêiner contém destinatários. 
    
3. O contêiner designado como padrão, se não houver contêineres com o sinalizador DT_GLOBAL definido em sua propriedade **PR_DISPLAY_TYPE** e o contêiner padrão for diferente do primeiro contêiner com permissão de leitura/gravação. 
    
Se **SetSearchPath** tiver sido chamado, **GetSearchPath** criará um caminho usando os contêineres de agendas que foram armazenados no perfil. **GetSearchPath** valida esse caminho antes de retorá-lo ao chamador. 
  
Após a primeira chamada para **SetSearchPath**, as chamadas subsequentes para **SetSearchPath** devem ser usadas para modificar o caminho de pesquisa retornado por **GetSearchPath**. Em outras palavras, o cliente ou provedor de chamada não recebe o caminho de pesquisa padrão após a primeira chamada para **SetSearchPath**.
  
## <a name="see-also"></a>Confira também



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

