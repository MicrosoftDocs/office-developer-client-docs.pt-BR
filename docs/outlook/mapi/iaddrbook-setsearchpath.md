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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426202"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define um novo caminho de pesquisa no perfil usado para o processo de resolução de nomes. 
  
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
  
> [in] Um ponteiro para a [estrutura SRowSet](srowset.md) usada para manter o caminho de pesquisa. A primeira propriedade para cada **membro aRow** em **SRowSet** deve ser **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O caminho de pesquisa foi definido com êxito.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Um dos contêineres descritos na estrutura **SRowSet** não incluiu sua **PR_ENTRYID** propriedade. 
    
## <a name="remarks"></a>Comentários

Os clientes e provedores de serviços chamam o método **SetSearchPath** para salvar as alterações feitas na ordem de pesquisa do contêiner usada para resolver nomes com o método [IAddrBook::ResolveName.](iaddrbook-resolvename.md) O caminho de pesquisa é salvo entre instâncias de uma sessão. 
  
Os clientes e provedores não têm que chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para tornar o caminho de pesquisa permanente. 
  
## <a name="see-also"></a>Confira também



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

