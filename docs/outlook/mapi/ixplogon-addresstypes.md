---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435373"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna os tipos de destinatários que o provedor de transporte trata.
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [out] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lpcAdrType_
  
> [out] Um ponteiro para a contagem de entradas na matriz apontada pelo parâmetro _lpppszAdrTypeArray._ 
    
 _lpppszAdrTypeArray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de cadeias de caracteres que identificam tipos de destinatários.
    
 _lpcMAPIUID_
  
> [out] Um ponteiro para a contagem de entradas na matriz apontada pelo _parâmetro lpppUIDArray._ 
    
 _lpppUIDArray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de ponteiros para estruturas [MAPIUID](mapiuid.md) que identificam tipos de destinatários. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O provedor de transporte indicou com êxito os tipos de destinatários que ele pode manipular.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

O spooler MAPI chama o método **IXPLogon::AddressTypes** imediatamente depois que um provedor de transporte retorna de uma chamada para o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para que o provedor de transporte possa indicar quais tipos de destinatários ele trata. Para indicar isso, o provedor de transporte deve passar de volta no parâmetro  _lpppszAdrTypeArray_ um ponteiro para uma matriz de ponteiros para cadeias de caracteres ou passar de volta no parâmetro  _lpppUIDArray_ um ponteiro para uma matriz de ponteiros para estruturas **MAPIUID** ou passar valores em ambos os parâmetros. 
  
Essas duas matrizes são usadas para diferentes processos de identificação. MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects. Nem MAPI nem o spooler MAPI expande endereços usando identificadores de entrada contidos em qualquer uma dessas estruturas **MAPIUID;** essas estruturas são usadas somente para identificação de tipo de destinatário. 
  
O spooler MAPI usa cada uma das cadeias de caracteres no parâmetro  _lpppszAdrTypeArray_ para um teste de comparação quando decide qual provedor de transporte deve lidar com quais destinatários para uma mensagem de saída. Se a propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de um destinatário da mensagem corresponde exatamente a uma cadeia de caracteres que identifica um dos tipos de endereço de mensagens que o provedor de transporte fornece, o provedor pode entregar a mensagem a esse destinatário.
  
Se vários provedores de transporte puderem lidar com o mesmo tipo de destinatário, o MAPI selecionará um provedor de transporte com base na ordem de prioridade de transporte indicada no perfil do aplicativo cliente. Para determinar qual provedor de transporte usar, o spooler MAPI examina todas as estruturas **MAPIUID** especificadas pelo provedor em ordem de prioridade e, em seguida, todos os valores de tipo de endereço especificados pelo provedor na ordem de prioridade. O primeiro provedor de transporte a corresponder a um destinatário específico nesta verificação obtém a primeira oportunidade de lidar com esse destinatário. Se esse provedor não manipular o destinatário, o spooler MAPI continuará a verificação para encontrar um provedor de transporte para qualquer destinatário ainda não manipulado. A verificação continua até que nenhuma outra ocorrência seja encontrada, momento em que um relatório de não entrega é gerado para qualquer destinatário que não foi manipulado. 
  
Se o provedor sempre oferece suporte a um conjunto específico de tipos de destinatários, o tipo de endereço e as matrizes **MAPIUID** passadas pelo provedor de transporte podem ser estáticas. Se o provedor de transporte construir dinamicamente essas matrizes, ele poderá alocar memória usando o objeto de suporte que foi passado anteriormente na chamada para **TransportLogon**, embora isso não seja necessário.
  
A memória usada para o tipo de endereço e matrizes **MAPIUID** deve permanecer alocada até a chamada final para o método [IXPLogon::TransportLogoff,](ixplogon-transportlogoff.md) quando o provedor de transporte pode liberar a memória, se necessário. O provedor de transporte não deve alterar o conteúdo dessas matrizes depois de retornar da **chamada TransportLogoff.** 
  
Um provedor de transporte que pode manipular qualquer tipo de destinatário pode retornar NULL no _parâmetro lpppszAdrTypeArray._ Provedores de transporte para sistemas de mensagens baseados em LAN que usam um servidor central para entregar mensagens de saída a vários sistemas de mensagens estrangeiras normalmente fazem isso. Esse tipo de provedor de transporte deve ser instalado por último na ordem de prioridade do spooler MAPI e MAPI dos provedores de transporte no perfil. 
  
Um provedor de transporte que não suporta mensagens de saída enviadas com base no tipo de endereço deve retornar uma única cadeia de caracteres de comprimento zero  _em lpppszAdrTypeArray_. Se um provedor de transporte não oferece suporte a tipos de destinatários, ele deve passar NULL para a estrutura **MAPIUID** e uma cadeia de caracteres vazia para o tipo de endereço. Provedores de transporte desse tipo são mais comumente usados para instalar um pré-processador de mensagem. 
  
## <a name="see-also"></a>Confira também



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

