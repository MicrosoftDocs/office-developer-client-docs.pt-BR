---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423633"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um objeto no contêiner, retornando um ponteiro de interface para acesso adicional.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do objeto a ser aberto. Se _lpEntryID_ estiver definido como nulo, o contêiner de nível superior na hierarquia do contêiner será aberto. 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto. Passar resultados nulos no identificador para a interface padrão do objeto que está sendo retornada. Para mensagens, a interface padrão é [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); para pastas, é [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). As interfaces padrão para os objetos do catálogo de endereços são [IDistList: IMAPIContainer](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser: IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto é aberto. Os seguintes sinalizadores podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto será aberto com as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver acesso somente leitura, o objeto deverá ser aberto com acesso somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o cliente de chamada. Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida. 
    
SHOW_SOFT_DELETES
  
> Mostra os itens atualmente marcados como excluídos por software, ou seja, estão na fase de tempo de retenção de item excluído.
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> bota Um ponteiro para um ponteiro para a implementação da interface a ser usada para acessar o objeto Open.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto somente leitura com permissão de leitura/gravação.
    
MAPI_E_NOT_FOUND 
  
> O identificador de entrada especificado por _lpEntryID_ não representa um objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada no parâmetro _lpEntryID_ não é de um formato reconhecido pelo contêiner. 
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer:: OpenEntry** abre um objeto em um contêiner e retorna um ponteiro para uma implementação de interface a ser usada para obter mais acesso. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como os provedores de serviço não precisam retornar uma implementação de interface do tipo especificado pelo identificador de interface no parâmetro _lpInterface_ , verifique o valor apontado pelo parâmetro _lpulObjType_ . Se necessário, converta o ponteiro retornado em _lppUnk_ para um ponteiro do tipo apropriado. 
  
Por padrão, os provedores de serviços abrem objetos com acesso somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS. Quando um desses sinalizadores é definido, os provedores de serviços tentam retornar um objeto modificável. No enTanto, não presuma que porque você solicitou um objeto modificável que o objeto aberto tem permissão de leitura/gravação. Planeje a chance de uma modificação subsequente falhar ou recuperar a propriedade **PR_ACCESS_LEVEL** do objeto para determinar o nível de acesso concedido pelo **OpenEntry**.
  
## <a name="see-also"></a>Confira também



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

