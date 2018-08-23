---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1d486344ab20ef49488dbb911f3dd7000d64942e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571756"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define um novo caminho de pesquisa no perfil que é usado para o processo de resolução de nome. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpSearchPath_
  
> [in] Um ponteiro para a estrutura de [SRowSet](srowset.md) usada para armazenar o caminho de pesquisa. A primeira propriedade para cada membro **aRow** em **SRowSet** deve ser **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O caminho de pesquisa foi definido com êxito.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Um dos contêineres descritos na estrutura de **SRowSet** não incluiu sua propriedade **PR_ENTRYID** . 
    
## <a name="remarks"></a>Comentários

Provedores de serviços e clientes chame o método de **SetSearchPath** para salvar as alterações feitas na ordem de pesquisa do contêiner que é usado para resolver nomes com o método [IAddrBook::ResolveName](iaddrbook-resolvename.md) . O caminho de pesquisa é salvo entre instâncias de uma sessão. 
  
Clientes e provedores não precisará chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que as alterações de caminho de pesquisa permanente. 
  
## <a name="see-also"></a>Confira também



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

