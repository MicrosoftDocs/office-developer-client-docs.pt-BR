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
description: 'Última modificação: 1 de fevereiro de 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434162"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parâmetros

_cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
_lpEntryID_
  
> no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.
    
_lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) da interface a ser usado para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, é [IDistList: IMAPIContainer](idistlistimapicontainer.md) e para contêiners, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
_ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a entrada é aberta. Os seguintes sinalizadores podem ser definidos.
    
MAPI_BEST_ACCESS 
  
> Solicita que a entrada seja aberta com o máximo permitido de rede e permissões de cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o provedor de catálogo de endereços deverá tentar abrir a entrada com permissão de leitura/gravação. O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps da entrada aberta e recuperando a propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Abre uma entrada do catálogo de endereços e a acessa somente do cache. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que a chamada seja bem-sucedida, possivelmente antes que a entrada esteja totalmente aberta e disponível, o que significa que chamadas posteriores à entrada podem retornar um erro.
    
MAPI_GAL_ONLY
  
> Use somente a GAL para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
  > [!NOTE]
  > O _parâmetroulflags_ MAPI_GAL_ONLY pode não estar definido no arquivo de cabeçalho baixável que você tem atualmente, e, nesse caso, você pode adicioná-lo ao seu código usando o seguinte valor: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Solicita que a entrada seja aberta com permissão de leitura/gravação. Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem supor que a permissão de leitura/gravação tenha sido concedida independentemente de o MAPI_MODIFY ser definido.
    
MAPI_NO_CACHE
  
> Não use o catálogo de endereços offline para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
_lpulObjType_
  
> bota Um ponteiro para o tipo de entrada aberta.
    
_lppUnk_
  
> bota Um ponteiro para um ponteiro para a entrada aberta.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A entrada foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de abrir uma entrada para a qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> A entrada representada por _lpEntryID_ não existe. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada especificado em _lpEntryID_ não é reconhecido. Esse valor normalmente é retornado se o provedor de catálogo de endereços responsável pela entrada correspondente não estiver aberto. 
    
## <a name="remarks"></a>Comentários

Os clientes e os provedores de serviços chamam o método **IAddrBook:: OpenEntry** para abrir uma entrada do catálogo de endereços. O MAPI encaminha a chamada para o provedor de catálogo de endereços apropriado, com base na estrutura [MAPIUID](mapiuid.md) incluída no identificador de entrada passado no parâmetro _lpEntryID_ . O provedor de catálogo de endereços abre a entrada como somente leitura, a menos que o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ seja definido. No enTanto, esses sinalizadores são sugestões. Se o provedor de catálogo de endereços não permitir a modificação da entrada solicitada, ele retornará MAPI_E_NO_ACCESS. 
  
O parâmetro _lpInterface_ indica qual interface deve ser usada para acessar a entrada aberta. Passar NULL no _lpInterface_ indica que a interface MAPI padrão para esse tipo de entrada deve ser usada. Como o provedor de catálogo de endereços pode retornar uma interface diferente da sugerida pelo parâmetro _lpInterface_ , o chamador deve verificar o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é o que era esperado. Se o tipo de objeto não for do tipo esperado, o chamador poderá converter o parâmetro _lppUnk_ para um tipo mais apropriado. 
  
## <a name="see-also"></a>Confira também

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

