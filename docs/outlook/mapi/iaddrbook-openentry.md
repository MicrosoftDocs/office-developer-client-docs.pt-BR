---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: '�ltima altera��o: sexta-feira, 1 de fevereiro de 2013'
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766886"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**Aplica-se a**: Outlook 
  
Abre uma entrada do catálogo de endereços e retorna um ponteiro para uma interface que pode ser usada para acessar a entrada.
  
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

## <a name="parameters"></a>Par�metros

_cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
_lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.
    
_lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) da interface a ser usada para acessar a entrada aberta. Passar NULL retorna a interface de padrão do objeto. Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, ele é [IDistList: IMAPIContainer](idistlistimapicontainer.md) e para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
_ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a entrada é aberta. Sinalizadores a seguir podem ser definidos.
    
MAPI_BEST_ACCESS 
  
> Solicita que a entrada seja aberto com as permissões de rede e cliente máxima permitidas. Por exemplo, se o cliente tem a permissão de leitura/gravação, o provedor de catálogo de endereços deve tentar abrir a entrada com permissão de leitura/gravação. O cliente pode recuperar o nível de acesso que foi concedido chamando o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Abre uma entrada do catálogo de endereços e acessa-lo apenas do cache. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que a chamada tiver êxito, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas posteriores à entrada podem retornar um erro.
    
MAPI_GAL_ONLY
  
> Use somente a GAL para executar a resolução de nomes. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
  > [!NOTE]
  > _UlFlags_ MAPI_GAL_ONLY não podem ser definidos no arquivo de cabeçalho para download que você possui atualmente, nesse caso, você pode adicioná-lo para seu código usando o seguinte valor: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Permissão de leitura/gravação que a entrada ser aberto com solicitações. Porque entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que a permissão de leitura/gravação concedeu independentemente MAPI_MODIFY é definida.
    
MAPI_NO_CACHE
  
> Não use o catálogo de endereços offline para executar a resolução de nome. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
_lpulObjType_
  
> [out] Um ponteiro para o tipo da entrada aberta.
    
_lppUnk_
  
> [out] Um ponteiro para um ponteiro para a entrada aberta.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A entrada foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para abrir uma entrada para o qual o usuário tem permissões insuficientes.
    
E_NOT_FOUND 
  
> A entrada representada por _lpEntryID_ não existe. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada especificado em _lpEntryID_ não é reconhecido. Esse valor geralmente será retornado se o provedor de catálogo de endereços responsável por na entrada correspondente não está aberto. 
    
## <a name="remarks"></a>Coment�rios

Provedores de serviços e clientes chame o método de **IAddrBook::OpenEntry** para abrir uma entrada do catálogo de endereços. MAPI encaminha a chamada para o provedor de catálogo de endereço apropriado, com base na estrutura [MAPIUID](mapiuid.md) incluída no passado no parâmetro _lpEntryID_ o identificador de entrada. O provedor de catálogo de endereços a entrada é aberta como somente leitura, a menos que o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _ulFlags_ está definido. No entanto, esses sinalizadores são sugestões. Se o provedor de catálogo de endereços não permite a modificação da entrada solicitada, ele retornará MAPI_E_NO_ACCESS. 
  
O parâmetro _lpInterface_ indica qual interface deve ser usada para acessar a entrada aberta. Passar NULL _lpInterface_ indica que a interface MAPI padrão para aquele tipo de entrada deve ser usada. Porque o provedor de catálogo de endereços pode retornar uma interface diferente daquela sugerido pelo parâmetro _lpInterface_ , o chamador deve verificar o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é o que era esperado. Se o tipo de objeto não é do tipo esperado, o chamador pode converter o parâmetro _lppUnk_ para um tipo que é mais apropriado. 
  
## <a name="see-also"></a>Confira também

- [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

